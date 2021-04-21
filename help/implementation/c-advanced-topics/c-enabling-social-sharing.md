---
description: Configure as credenciais que permitem que os usuários compartilhem conteúdo em várias redes sociais.
title: Ativar o compartilhamento em redes sociais
exl-id: 08ac9766-52ea-432f-8b4f-bf68cb8b62bc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Ativar o compartilhamento em redes sociais {#enabling-social-sharing}

Configure as credenciais que permitem que os usuários compartilhem conteúdo em várias redes sociais.

Para permitir que os usuários compartilhem conteúdo em sites de mídia social, implemente o recurso Compartilhamento em redes sociais do Livefyre e crie um sistema OAuth para fornecer a autenticação adequada a esses sites. Com esse sistema, o Livefyre age em nome do usuário quando ele opta por compartilhar conteúdo por meio das redes sociais.

>[!NOTE]
>
>Diferentes provedores têm requisitos OAuth diferentes. Consulte seus provedores para adquirir as informações associadas à implementação do OAuth.

## Credenciais sociais necessárias {#section_gff_cjm_b1b}

Se você usar um sistema de identidade de usuário personalizado, deverá fornecer suas credenciais sociais para permitir que os usuários compartilhem com a Twitter, Facebook ou LinkedIn a partir de um aplicativo Livefyre.

>[!NOTE]
>
>Os clientes que usam o Janrain Engage só precisam fornecer o domínio Engage e a chave de API Engage.

Use o painel Configurações de integração do Admin Console para inserir ou atualizar as seguintes credenciais sociais.

### Credenciais Necessárias:

* **** Redirecionamento de proxy OAuth secreto do cliente da ID do FacebookClient
* **** Segredo da API da chave LinkedInAPI
* **** Segredo da API da chave de acesso ao token de acesso ao token do TwitterAccess

## Twitter {#section_qp5_1yl_b1b}

As credenciais do twitter estão disponíveis no Painel de aplicativos do Twitter. Para localizar essas credenciais:

* Abra [Página de Desenvolvimento de Aplicativo da Twitter](https://dev.twitter.com/apps) como o proprietário do Aplicativo, encontre seu aplicativo e clique no título.
* Role para baixo até &quot;Seu token de acesso&quot; e capture os valores de &quot;Token de acesso&quot; e &quot;Segredo do token de acesso&quot;.

Você deve:

* Insira um valor para o campo Callback URL no aplicativo do Twitter. Embora esse campo possa ser um espaço reservado simples, ele não pode ser deixado em branco.
* Defina o Tipo de aplicativo para ter acesso a **read** e **write**.
* Confirme se o URL do site do aplicativo Twitter está no mesmo domínio de host que o aplicativo principal do Livefyre.

>[!NOTE]
>
>Todos os aplicativos que exibem conteúdo Twitter devem seguir os requisitos de exibição. Consulte as [Diretrizes de exibição do Twitter](https://dev.twitter.com/terms/display-requirements) para obter mais informações.

## LinkedIn {#section_lfz_zxl_b1b}

As credenciais do linkedIn estão disponíveis na seção Chaves de OAuth das Chaves de API do seu aplicativo LinkedIn.

* Faça logon em sua conta na página de desenvolvedores do LinkedIn [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Passe o mouse sobre o seu nome no canto superior direito e selecione Chaves de API no menu suspenso.
* Clique no título do Aplicativo.
* Obtenha os valores Chave da API e Chave secreta na seção Chaves OAuth

## Facebook {#section_zyb_gpl_b1b}

As credenciais do facebook estão disponíveis na página Aplicativos do desenvolvedor .

* Abra [Página de aplicativos do desenvolvedor da Facebook](https://developers.facebook.com/apps) como proprietário do aplicativo, localize seu aplicativo e clique no título.
* Obtenha os valores para ID do aplicativo e Segredo do aplicativo. Para o Segredo do aplicativo, talvez seja necessário clicar no botão Mostrar para exibi-lo.

O compartilhamento no Facebook requer a configuração de uma página de redirecionamento para atender às solicitações do Facebook e às práticas de domínio exigidas pelo [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). A página deve ser hospedada em seu domínio para que a Facebook possa verificar se a solicitação veio de uma fonte legítima.

### Redirecionamento facebook

A página hospedada deve incluir o seguinte código:

### Ruby

Este é um exemplo de uso de Ruby e Rails para fazer o redirecionamento do Facebook OAuth.

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### Python

Este é um exemplo de uso de Python e Django para fazer o redirecionamento OAuth do Facebook.

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

Este é um exemplo de uso de NodeJS e Sail/Express para fazer o redirecionamento OAuth do Facebook.

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

Este é um exemplo de uso de controladores Java e Spring para fazer o redirecionamento OAuth do Facebook.

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## Configurando provedores de &quot;postagem para&quot; {#section_rdk_dpl_b1b}

Por padrão, os botões &quot;Publicar em&quot; do Facebook, LinkedIn e Twitter são exibidos nos aplicativos principais do Livefyre. Use o parâmetro postToButtons para configurar quais provedores aparecerão ao incorporar o aplicativo Livefyre.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` é uma matriz com qualquer subconjunto das seguintes opções:

* tw: Twitter
* fb: Facebook
* li: linkedIn
