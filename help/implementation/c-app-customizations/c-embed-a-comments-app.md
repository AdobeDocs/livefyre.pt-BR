---
description: Incorporar o aplicativo de comentários segue o processo de incorporação
  de um aplicativo principal.
seo-description: Incorporar o aplicativo de comentários segue o processo de incorporação
  de um aplicativo principal.
seo-title: Incorporar um aplicativo de comentários
solution: Experience Manager
title: Incorporar um aplicativo de comentários
uuid: e 4982 ad 3-cab 1-4805-a 55 c -594 cca 3 b 7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e

---


# Incorporar um aplicativo de comentários{#embed-a-comments-app}

Incorporar o aplicativo de comentários segue o processo de incorporação de um aplicativo principal.

A incorporação do aplicativo de comentários segue o processo de incorporação de um aplicativo principal descrito em [Incorporar um aplicativo](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

## Exemplo

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Como observado na seção Building collectionmeta, collectionmeta é um objeto JSON codificado. No exemplo acima, o objeto JSON pega o seguinte formato antes de ser codificado em JWT:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

