---
description: Configure credenciais que permitem aos usuários compartilhar conteúdo
  em várias redes sociais.
seo-description: Configure credenciais que permitem aos usuários compartilhar conteúdo
  em várias redes sociais.
seo-title: Ativar compartilhamento em redes sociais
solution: Experience Manager
title: Ativar compartilhamento em redes sociais
uuid: f 584 a 0 ae -46 c 7-48 c 1-aea 4-36 da 9 f 1 e 259 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Ativar compartilhamento em redes sociais {#enabling-social-sharing}

Configure credenciais que permitem aos usuários compartilhar conteúdo em várias redes sociais.

Para permitir que os usuários compartilhem conteúdo em sites de mídia social, implemente o recurso Compartilhamento em redes sociais do Livefyre e crie um sistema oauth para fornecer a autenticação correta nesses sites. Com esse sistema, o Livefyre atua sobre o nome do usuário quando ele escolhe compartilhar conteúdo por meio de mídia social.

>[!NOTE]
>
>Diferentes provedores têm requisitos diferentes do oauth. Consulte os seus provedores para adquirir as informações associadas à implementação do oauth.

## Credenciais sociais necessárias {#section_gff_cjm_b1b}

Se você usar um sistema de identidade de usuário personalizado, você deve fornecer suas credenciais sociais para permitir que os usuários compartilhem com Twitter, Facebook ou linkedin a partir de um aplicativo Livefyre.

>[!NOTE]
>
>Os clientes que usam Janrain Mobilizar precisam fornecer somente seu Domínio Mobilizar e Mobilizar a chave de API.

Use o painel Configurações de integração do Admin Console para inserir ou atualizar as seguintes credenciais sociais.

### Credenciais obrigatórias:

* **Redirecionamento de proxy de oauth do cliente do Facebook** Client ID
* **Segredo da API** da API do linkedin
* **Twitter** Access Token Token API Key API Key API

## Twitter {#section_qp5_1yl_b1b}

As credenciais do Twitter estão disponíveis no Painel do aplicativo do Twitter. Para encontrar essas credenciais:

* Abra [a Página de desenvolvimento do aplicativo do Twitter](https://dev.twitter.com/apps) como proprietário do aplicativo, encontre seu aplicativo e clique no título.
* Role para baixo até «Seu token de acesso» e capture os valores de «Token de acesso» e «Acesso a token de acesso». »

Você deve:

* Digite um valor para o campo URL de retorno de chamada no aplicativo do Twitter. Embora esse campo possa ser um espaço reservado simples, ele não pode ser deixado em branco.
* Defina o Tipo de aplicativo para ter acesso **de leitura** e **gravação** .
* Confirme se o URL do site do aplicativo do Twitter está no mesmo domínio host do aplicativo Livefyre Core.

>[!NOTE]
>
>Todos os aplicativos que exibem conteúdo do Twitter devem seguir seus requisitos de exibição. Consulte as Diretrizes de exibição [do Twitter](https://dev.twitter.com/terms/display-requirements) para obter mais informações.

## Linkedin {#section_lfz_zxl_b1b}

As credenciais do linkedin estão disponíveis na seção Chaves oauth das Chaves de API do aplicativo do linkedin.

* Faça logon na sua conta a partir da página de desenvolvedores do linkedin [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Passe o mouse sobre o seu nome na parte superior direita e selecione Chaves de API no menu suspenso.
* Clique no título do aplicativo.
* Captura a chave da API e os valores de chave secreta na seção Atalhos de oauth

## Facebook {#section_zyb_gpl_b1b}

As credenciais do Facebook estão disponíveis na sua página de Aplicativos do desenvolvedor.

* Abra [a Página de aplicativos do Facebook](https://developers.facebook.com/apps) do Facebook como proprietário do aplicativo, encontre seu aplicativo e clique no título.
* Capture os valores para ID do aplicativo e segredo do aplicativo. Para o Segredo do aplicativo, talvez seja necessário clicar no botão Mostrar para exibi-lo.

O compartilhamento no Facebook requer que você configure uma página de redirecionamento para fazer solicitações do Facebook e seguir as práticas de domínio exigidas pelo [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). A página deve ser hospedada em seu domínio para que o Facebook possa verificar se a solicitação veio de uma fonte legítima.

### Redirecionamento do Facebook

A página hospedada deve incluir o seguinte código:

### Ruby

Este é um exemplo que usa Ruby e Rails para fazer o redirecionamento do Facebook oauth.

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

Este é um exemplo que usa Python e Django para fazer o redirecionamento do Facebook oauth.

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

### Nodejs

Este é um exemplo que usa nodejs e Sail/Express para fazer o redirecionamento do Facebook oauth.

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

Este é um exemplo que usa controladores Java e primavera para fazer o redirecionamento do Facebook oauth.

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

## Configuração de provedores de «Publicação» {#section_rdk_dpl_b1b}

Por padrão, os botões Facebook, linkedin e Twitter «Postar em» são mostrados nos aplicativos do Livefyre Core. Use o parâmetro posttobuttons para configurar quais provedores serão exibidos ao incorporar o Aplicativo Livefyre.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` é uma matriz com qualquer subconjunto das seguintes opções:

* tw: Twitter
* fb: Facebook
* li: Linkedin
