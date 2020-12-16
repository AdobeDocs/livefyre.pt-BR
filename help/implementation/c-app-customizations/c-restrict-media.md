---
description: Limite o tipo de mídia que entra no fluxo do aplicativo.
seo-description: Limite o tipo de mídia que entra no fluxo do aplicativo.
seo-title: Restringir mídia
solution: Experience Manager
title: Restringir mídia
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Restringir mídia{#restrict-media}

Limite o tipo de mídia que entra no fluxo do aplicativo.

Por padrão, todos os anexos de mídia podem ser incorporados aos aplicativos. O Livefyre permite alterar essa opção para impedir que os usuários postem tipos de anexos selecionados em seus aplicativos.

>[!NOTE]
>
>Livefyre faz parceria com Embeely para integração de mídia. Para obter mais informações, consulte Integração de conteúdo > Integração integrada. Entre em contato com seu Gerente de conta técnico para obter informações sobre a expansão ou as fontes do link.

Este exemplo bloqueia a incorporação do YouTube e do Vimeo ao seu fluxo de comentários:

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

