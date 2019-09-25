---
description: Adicione ações personalizadas aos aplicativos do Livefyre.
seo-description: Adicione ações personalizadas aos aplicativos do Livefyre.
seo-title: Adicionar botões personalizados
solution: Experience Manager
title: Adicionar botões personalizados
uuid: 27d24c21-d83f-49df-9b3f-15d7abbd2bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Adicionar botões personalizados{#add-custom-buttons}

Adicione ações personalizadas aos aplicativos do Livefyre.

O Livefyre permite que você adicione botões personalizados ao lado dos botões de ação existentes (como **[!UICONTROL Share]**, e **[!UICONTROL Flag]**) em um conteúdo.

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

1. Passe um argumento adicional em seu objeto ConvConfig chamado actionButtons, contendo uma matriz de objetos descrevendo cada botão que você gostaria de adicionar.
1. Defina uma tecla para o texto a ser exibido para cada botão.
1. Adicione um retorno de chamada que será chamado em um evento de clique para cada botão.

O retorno de chamada é chamado com um objeto com duas chaves: `authorId` e `contentId`.
