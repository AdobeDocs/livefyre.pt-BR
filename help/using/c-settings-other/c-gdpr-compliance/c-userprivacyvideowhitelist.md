---
description: Você pode permitir a lista de seu domínio de vídeo.
seo-description: Você pode permitir a lista de seu domínio de vídeo.
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Se você usar seus próprios vídeos e players personalizados como parte dos vídeos exibidos em um aplicativo de visualização do Livefyre, poderá permitir a listagem do seu domínio de vídeo. Permitir a listagem de seu domínio de vídeo remove a máscara de vídeo para seus vídeos e players personalizados.

>[!NOTE]
>
>Use caminhos específicos para garantir que somente os vídeos que são seguros sejam listados com permissão. Se você colocar um caminho amplo (por exemplo, sampledomain.com), poderá permitir a lista de vídeos não seguros.

* Adicione `userPrivacyVideoWhitelist` depois de `userPrivacyOptOut`. Você pode adicionar todos os sinalizadores de privacidade do Livefyre todos de uma só vez como parte de um objeto do Livefyre.
* `userPrivacyVideoWhitelist` aplica-se somente ao conteúdo que não está incorporado nas mídias sociais.

No exemplo a seguir, os vídeos exibidos em Aplicativos com o caminho `sampledomain.com/cdn/videos` são listados com permissão:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
