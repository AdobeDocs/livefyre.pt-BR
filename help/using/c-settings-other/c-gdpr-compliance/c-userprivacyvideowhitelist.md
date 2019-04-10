---
description: É possível adicionar o domínio de vídeo à lista de permissão.
seo-description: É possível adicionar o domínio de vídeo à lista de permissão.
seo-title: Userprivacyvideowhitelist
solution: Experience Manager
title: Userprivacyvideowhitelist
uuid: adfead 18-b 73 b -4 ac 4-97 a 0-d 39 f 528 b 7606
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyvideowhitelist{#userprivacyvideowhitelist}

Se você usar seus próprios vídeos e players personalizados como parte dos vídeos exibidos em um aplicativo de visualização do Livefyre, é possível adicionar o seu domínio de vídeo à lista de permissão. A lista de permissões do seu domínio de vídeo remove a máscara de vídeo dos seus vídeos e players personalizados.

>[!NOTE]
>
>Use caminhos específicos para garantir que apenas os vídeos que são seguros são autorizados. Se você colocar um caminho amplo (por exemplo, sampledomain.com), poderá usar vídeos não seguros de lista de permissões.

* Adicionar `userPrivacyVideoWhitelist` depois `userPrivacyOptOut`. Você pode adicionar todos os sinalizadores de privacidade do Livefyre simultaneamente como parte de um objeto do Livefyre.
* `userPrivacyVideoWhitelist` se aplica somente ao conteúdo que não está incorporado a mídia social.

No exemplo a seguir, os vídeos exibidos em Aplicativos com `sampledomain.com/cdn/videos` o caminho são autorizados:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
