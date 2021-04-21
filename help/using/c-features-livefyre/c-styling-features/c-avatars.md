---
description: Permitir que os usuários personalizem a imagem exibida com seu conteúdo.
title: Avatares
exl-id: cff7f6be-3660-4d71-949b-6ac04379d68d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---

# Avatars{#avatars}

Permitir que os usuários personalizem a imagem exibida com seu conteúdo.

Os avatares do usuário são exibidos (por padrão) ao lado do conteúdo em todos os aplicativos e são obtidos do sistema de perfil de identidade usado na implementação. Esses avatars variam de tamanho, de acordo com o aplicativo no qual são exibidos.

(O Livefyre permite desativar avatars se você não quiser exibi-los em seus aplicativos.)

>[!NOTE]
>
>Os avatars são exibidos em 25p x 25p para Chat e 50p x 50p na maioria dos outros aplicativos.

## Armazenamento de avatar {#section_zbh_x1f_wy}

Os avatars são carregados de forma assíncrona no Livefyre. Quando um usuário entra no aplicativo pela primeira vez ou altera seu arquivo de imagem de avatar associado, a imagem do perfil é adicionada a uma fila de tarefas. (Um avatar padrão é exibido temporariamente enquanto o do usuário é carregado no local de armazenamento do avatar do Livefyre.)

## Gravatares {#section_mqh_p1f_wy}

Livefyre suporta o uso de Gravatars. Se um usuário não tiver um avatar personalizado como parte de seu perfil de usuário, o Livefyre verificará se há um Gravatar para esse usuário. Se não houver Gravatar, o avatar padrão será usado.


Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Placa de recurso](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mural de mídia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Resenhas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
