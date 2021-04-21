---
description: Adicione ações personalizadas aos aplicativos do Livefyre.
title: Adicionar botões personalizados
exl-id: a62d8605-59c2-4214-af26-805c1989aca1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# Adicionar botões personalizados{#add-custom-buttons}

Adicione ações personalizadas aos aplicativos do Livefyre.

O Livefyre permite adicionar botões personalizados ao lado dos botões de ação existentes (como **[!UICONTROL Share]** e **[!UICONTROL Flag]**) em um conteúdo.

Use o argumento para dispositivos móveis para definir se o botão será exibido em dispositivos móveis.

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

1. Passe um argumento adicional em seu objeto ConvConfig chamado actionButtons, contendo uma matriz de objetos descrevendo cada botão que você deseja adicionar.
1. Defina uma chave para o texto a ser exibido para cada botão.
1. Adicione um retorno de chamada que será chamado em um evento de clique para cada botão.

O retorno de chamada é chamado com um objeto com duas chaves: `authorId` e `contentId`.
