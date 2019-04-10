---
description: Mostre várias coleções em uma única página.
seo-description: Mostre várias coleções em uma única página.
seo-title: Várias coleções
solution: Experience Manager
title: Várias coleções
uuid: 9675 ffd 7-1 a 59-42 a 1-b 3 ba -40 af 1744 cfd 1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Várias coleções {#multiple-collections}

Mostre várias coleções em uma única página.

Você pode incluir várias Coleções em uma única página do site. Por exemplo, para publicar um evento, você pode ter uma discussão do Live Blog ou Bate-papo durante o evento, com um Aplicativo separado na lateral da página, exibindo Conteúdo preparado relacionado em torno da Web social. Ou você pode incluir um Aplicativo de comentários abaixo de um artigo, com um bate-papo para a lateral.

Para obter várias conversas em uma página, adicione uma ou mais configurações em uma matriz e passe a matriz para a chamada de carregamento. Por exemplo.

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
