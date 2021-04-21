---
description: Você pode adicionar o domínio de vídeo à lista de permissões.
title: userPrivacyVideoWhitelist
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Se você usa seus próprios vídeos e players personalizados como parte dos vídeos exibidos em um aplicativo de visualização do Livefyre, é possível adicionar o domínio do vídeo à lista de permissões. A listagem de permissões do domínio de vídeo remove a máscara de vídeo dos vídeos e reprodutores personalizados.

>[!NOTE]
>
>Use caminhos específicos para garantir que apenas os vídeos seguros sejam incluídos na lista de permissões. Se você colocar um caminho amplo (por exemplo, sampledomain.com), poderá incluir vídeos não seguros na lista de permissões.

* Adicione `userPrivacyVideoWhitelist` depois de `userPrivacyOptOut`. Você pode adicionar todos os sinalizadores de privacidade do Livefyre de uma só vez como parte de um objeto do Livefyre.
* `userPrivacyVideoWhitelist` se aplica somente ao conteúdo que não está incorporado nas redes sociais.

No exemplo a seguir, vídeos exibidos em aplicativos com o caminho `sampledomain.com/cdn/videos` são permitidos:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
