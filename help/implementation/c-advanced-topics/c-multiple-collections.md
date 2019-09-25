---
description: Mostre várias coleções em uma única página.
seo-description: Mostre várias coleções em uma única página.
seo-title: Várias coleções
solution: Experience Manager
title: Várias coleções
uuid: 9675ffd7-1a59-42a1-b3ba-40af1744cfd1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Várias coleções {#multiple-collections}

Mostre várias coleções em uma única página.

Você pode incluir várias coleções em uma única página do site. Por exemplo, para publicar um evento, é possível que você tenha uma discussão de Blog ao vivo ou Bate-papo durante o evento, com um aplicativo separado na lateral da página, exibindo o Conteúdo curado relacionado na Web social. Ou você pode incluir um aplicativo de comentários abaixo de um artigo, com um bate-papo ao lado.

Para obter várias conversas em uma página, adicione uma ou mais configurações em um storage e passe o storage para a chamada de carregamento. Por exemplo.

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
