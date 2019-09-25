---
description: Você pode adicionar o domínio de vídeo à lista de permissões usando .
seo-description: Você pode adicionar o domínio de vídeo à lista de permissões usando .
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Se você usar seus próprios vídeos e players personalizados como parte dos vídeos exibidos em um aplicativo de visualização Livefyre, poderá adicionar o domínio de vídeo à lista de permissões. A lista de permissões de seu domínio de vídeo remove a máscara de vídeo para seus vídeos e players personalizados.

>[!NOTE]
>
>Use caminhos específicos para garantir que somente os vídeos que são seguros estejam na lista de permissões. Se você colocar um caminho amplo (por exemplo, sampledomain.com), poderá adicionar vídeos não seguros à lista de permissões.

* Adicionar `userPrivacyVideoWhitelist` depois `userPrivacyOptOut`. Você pode adicionar todos os sinalizadores de privacidade do Livefyre todos de uma só vez como parte de um objeto do Livefyre.
* `userPrivacyVideoWhitelist` aplica-se somente ao conteúdo que não está incorporado nas redes sociais.

No exemplo a seguir, os vídeos exibidos em Aplicativos com o `sampledomain.com/cdn/videos` caminho são exibidos na lista de permissões:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
