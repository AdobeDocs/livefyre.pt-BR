---
description: Limite o tipo de mídia que entra no fluxo do aplicativo.
title: Restringir mídia
exl-id: ae09a058-41de-4b63-8654-cc82f5abad14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Restringir mídia{#restrict-media}

Limite o tipo de mídia que entra no fluxo do aplicativo.

Por padrão, todos os anexos de mídia podem ser incorporados aos aplicativos. O Livefyre permite alterar essa opção para impedir que os usuários publiquem tipos de anexos selecionados em seus aplicativos.

>[!NOTE]
>
>A Livefyre faz parceria com a Embedly para integração de mídia. Para obter mais informações, consulte Integração de conteúdo > Integração do Embedly . Entre em contato com seu Gerente de conta técnico para dúvidas sobre a expansão ou fontes de links.

Esse exemplo bloqueia a incorporação do YouTube e do Vimeo ao seu fluxo de comentários:

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

Ao carregar a conversa:

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```
