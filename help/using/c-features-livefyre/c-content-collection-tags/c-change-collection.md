---
description: Permite que os usuários cliquem em Coleções de um único layout de página e URL.
title: Alterar coleção
exl-id: 5cfae2c6-e328-4d2c-b08b-709be94e4c54
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Alterar coleção{#change-collection}

Permite que os usuários cliquem em Coleções de um único layout de página e URL.

Use Alterar delegado da coleção para alterar a coleção mostrada em uma página, sem alterar o URL, enquanto um aplicativo Livefyre já está carregado. Use esse recurso para exibir galerias de fotos ou vídeos ou outros aplicativos, onde a Coleção exibida deve ser alterada após uma ação do usuário.

Por exemplo, clicar em um vídeo ou foto em uma galeria carregará uma Coleção específica para essa seleção, enquanto o URL da página não será alterado.

Para carregar uma das três Coleções de uma única página [comment count](/help/implementation/c-advanced-topics/t-display-comment-count.md):

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
