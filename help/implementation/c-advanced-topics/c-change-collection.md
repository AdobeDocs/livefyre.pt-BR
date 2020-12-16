---
description: Permite que os usuários cliquem em Coleções de um único layout de página e URL.
seo-description: Permite que os usuários cliquem em Coleções de um único layout de página e URL.
seo-title: Alterar coleção
solution: Experience Manager
title: Alterar coleção
uuid: 81c8a554-375f-4659-9e25-5b3618824633
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Alterar coleção {#change-collection}

Permite que os usuários cliquem em Coleções de um único layout de página e URL.

Use o delegado Alterar coleção para alterar a coleção exibida em uma página, sem alterar o URL, enquanto um aplicativo Livefyre já estiver carregado. Use esse recurso para exibir galerias de fotos ou vídeos ou outros aplicativos nos quais a coleção exibida deve mudar após uma ação do usuário.

Por exemplo, clicar em um vídeo ou foto em uma galeria carregará uma coleção específica para essa seleção, enquanto o URL da página não será alterado.

Para [carregar uma das três coleções de uma única página](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count):

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
