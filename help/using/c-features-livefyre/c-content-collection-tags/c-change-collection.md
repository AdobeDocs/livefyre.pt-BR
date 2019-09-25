---
description: Permite que os usuários cliquem em Coleções de um único layout de página e URL.
seo-description: Permite que os usuários cliquem em Coleções de um único layout de página e URL.
seo-title: Alterar coleção
solution: Experience Manager
title: Alterar coleção
uuid: 69bafcc7-c55e-47d6-bc79-b0db80fdf138
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Alterar coleção{#change-collection}

Permite que os usuários cliquem em Coleções de um único layout de página e URL.

Use o delegado Alterar coleção para alterar a coleção exibida em uma página, sem alterar o URL, enquanto um aplicativo Livefyre já estiver carregado. Use esse recurso para exibir galerias de fotos ou vídeos ou outros aplicativos nos quais a coleção exibida deve mudar após uma ação do usuário.

Por exemplo, clicar em um vídeo ou foto em uma galeria carregará uma coleção específica para essa seleção, enquanto o URL da página não será alterado.

Para carregar uma das três coleções de uma única página de contagem [de](/help/implementation/c-advanced-topics/t-display-comment-count.md) comentários:

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

