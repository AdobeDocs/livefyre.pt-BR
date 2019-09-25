---
description: Configure credenciais que permitam aos usuários compartilhar conteúdo em várias redes sociais.
seo-description: Configure credenciais que permitam aos usuários compartilhar conteúdo em várias redes sociais.
seo-title: Enabling Social Sharing
solution: Experience Manager
title: Habilitar compartilhamento em redes sociais
uuid: f584a0ae-46c7-48c1-aea4-36da9f1e259b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830

---


# Enabling Social Sharing {#enabling-social-sharing}

Set up credentials that allow your users to share content to various social networks.

To allow users to share content across social media sites, implement Livefyre’s Social Sharing feature, and create an OAuth system to provide proper authentication to these sites. With this system, Livefyre acts upon the user’s behalf when they choose to share content through social media.

>[!NOTE]
>
>Different providers have different OAuth requirements. Please consult with your providers to acquire the information associated with their implementation of OAuth.

## Required Social Credentials {#section_gff_cjm_b1b}

If you use a custom user identity system, you must provide your social credentials to enable users to share to Twitter, Facebook, or LinkedIn from a Livefyre App.

>[!NOTE]
>
>Customers using Janrain Engage need only provide their Engage Domain and Engage API Key.

Use the Admin Console’s Integration Settings panel to enter or update the following social credentials.

### Required Credentials:

* **Redirecionamento de Proxy OAuth Secreto do Cliente de ID do Cliente do Facebook**
* **LinkedIn API Key API Secret**
* **API de chave secreta do token de acesso ao token do Twitter** Access

## Twitter {#section_qp5_1yl_b1b}

As credenciais do Twitter estão disponíveis no Painel de aplicativos do Twitter. Para localizar essas credenciais:

* Abra a Página [de desenvolvedor de aplicativos do](https://dev.twitter.com/apps) Twitter como o proprietário do aplicativo, localize seu aplicativo e clique no título.
* Role para baixo até "Your access token" (Seu token de acesso) e capture os valores de "Access token" (Token de acesso) e "Access token secret" (Acessar segredo do token).

Você deve:

* Insira um valor para o campo URL de retorno de chamada no aplicativo do Twitter. Embora esse campo possa ser um espaço reservado simples, ele não pode ser deixado em branco.
* Defina o Tipo de aplicativo para ter acesso de **leitura** e **gravação** .
* Confirme se o URL do site do aplicativo do Twitter está no mesmo domínio de host do aplicativo Livefyre Core.

>[!NOTE]
>
>Todos os aplicativos que exibem conteúdo do Twitter são necessários para seguir seus requisitos de exibição. Consulte as Diretrizes [de exibição do](https://dev.twitter.com/terms/display-requirements) Twitter para obter mais informações.

## LinkedIn {#section_lfz_zxl_b1b}

As credenciais do LinkedIn estão disponíveis na seção Chaves OAuth das Chaves de API do aplicativo do LinkedIn.

* Faça logon em sua conta na página de desenvolvedores do LinkedIn [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Passe o mouse sobre seu nome na parte superior direita e selecione Chaves de API no menu suspenso.
* Clique no título Aplicativo.
* Obtenha os valores da chave da API e da chave secreta na seção Chaves OAuth

## Facebook {#section_zyb_gpl_b1b}

As credenciais do Facebook estão disponíveis na página Aplicativos do desenvolvedor.

* Abra a página [Aplicativos para desenvolvedores do](https://developers.facebook.com/apps) Facebook como o proprietário do aplicativo, localize seu aplicativo e clique no título.
* Obtenha os valores para ID do aplicativo e segredo do aplicativo. Para o segredo do aplicativo, talvez seja necessário clicar no botão Mostrar para exibi-lo.

O compartilhamento no Facebook requer a configuração de uma página de redirecionamento para atender às solicitações do Facebook e às práticas de domínio exigidas pelo [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). A página deve ser hospedada em seu domínio para que o Facebook possa verificar se a solicitação veio de uma fonte legítima.

### Redirecionamento do Facebook

A página hospedada deve incluir o seguinte código:

### Ruby

Este é um exemplo de uso de Ruby e Rails para fazer o redirecionamento OAuth do Facebook.

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

This is an example using NodeJS and Sail/Express to do the Facebook OAuth redirect.

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

This is an example using Java and Spring controllers to do the Facebook OAuth redirect.

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

## Configuring “Post to” Providers {#section_rdk_dpl_b1b}

By default, Facebook, LinkedIn, and Twitter “Post to” buttons are shown on Livefyre Core applications. Use the postToButtons parameter to configure which providers will appear when embedding the Livefyre App.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` is an array with any subset of the following options:

* tw: Twitter
* fb: Facebook
* li: LinkedIn
