---
description: Adicione ações personalizadas aos seus aplicativos do Livefyre.
seo-description: Adicione ações personalizadas aos seus aplicativos do Livefyre.
seo-title: Adicionar botões personalizados
solution: Experience Manager
title: Adicionar botões personalizados
uuid: 27 d 24 c 21-d 83 f -49 df -9 b 3 f 3 f -15 d 7 abbd 2 bd 7
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Adicionar botões personalizados{#add-custom-buttons}

Adicione ações personalizadas aos seus aplicativos do Livefyre.

O Livefyre permite adicionar botões personalizados ao lado dos botões de ação existentes (como **[!UICONTROL Share]**e **[!UICONTROL Flag]**) em um conteúdo.

Use o argumento móvel para definir se o botão será exibido em dispositivos móveis.

Por exemplo, para adicionar um botão de ação personalizado para a interface do dispositivo móvel:

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. Passe um argumento adicional no objeto convconfig chamado actionbuttons, contendo uma matriz de objetos que descrevem cada botão que você gostaria de adicionar.
1. Defina uma chave para que o texto seja exibido para cada botão.
1. Adicione um retorno de chamada que será invocado em um evento click para cada botão.

O retorno de chamada é chamado com um objeto com duas chaves: `authorId` e `contentId`.
