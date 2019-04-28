---
description: Limite o tipo de mídia que entra no fluxo do aplicativo.
seo-description: Limite o tipo de mídia que entra no fluxo do aplicativo.
seo-title: Restringir mídia
solution: Experience Manager
title: Restringir mídia
uuid: c 470 c 985-d 221-4 f 39-8 bd 4-4 e 44 ec 14 db 95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Restringir mídia{#restrict-media}

Limite o tipo de mídia que entra no fluxo do aplicativo.

Por padrão, todos os anexos de mídia podem ser incorporados em Aplicativos. O Livefyre permite alterar essa opção para impedir que os usuários postem tipos de anexos selecionados nos seus aplicativos.

>[!NOTE]
>
>Parceiros do Livefyre com integração de mídia. Para obter mais informações, consulte Integração de conteúdo &gt; Integração de integração. Entre em contato com seu Gerente de conta técnico para obter perguntas sobre expansão de links ou fontes.

Este exemplo bloqueia a incorporação do youtube e do Vimeo a partir do seu fluxo de comentário:

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

