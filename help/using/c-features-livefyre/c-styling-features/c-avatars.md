---
description: Permita que os usuários personalizem a imagem exibida com seu conteúdo.
seo-description: Permita que os usuários personalizem a imagem exibida com seu conteúdo.
seo-title: Avatars
title: Avatars
uuid: bf 20 f 3 bc -3 dcc -4 e 16-a 629-3380 d 1 a 7 a 3 f 2
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Avatars{#avatars}

Permita que os usuários personalizem a imagem exibida com seu conteúdo.

Os avatars do usuário são exibidos (por padrão) ao lado do conteúdo em todos os aplicativos e são obtidos do sistema de perfil de identidade usado na implementação. Esses avulars variam de acordo com o aplicativo em que são exibidos.

(O Livefyre permite desativar Avatars se você não quiser exibi-los em seus Aplicativos.)

>[!NOTE]
>
>Os Avatars são exibidos em 25 p x 25 p para Chat e 50 p x 50 p na maioria dos outros aplicativos.

## Armazenamento avatar {#section_zbh_x1f_wy}

Os Avatars são carregados de maneira assíncrona no Livefyre. Quando um usuário faz logon pela primeira vez no aplicativo ou altera o arquivo associado de imagem de avatar, a imagem do perfil é adicionada a uma fila de tarefas. (Um avatar padrão é exibido temporariamente enquanto o usuário é carregado no local do armazenamento avatar do Livefyre.)

## Gravatários {#section_mqh_p1f_wy}

O Livefyre é compatível com o uso de Gravatars. Se um usuário não tiver um avatar personalizado como parte de seu perfil de usuário, o Livefyre verificará se há um registro desse usuário. Se nenhum registro existir, o avatar padrão será usado.

Se os Comentários tiverem sido incorporados usando o plug-in do Livefyre wordpress, o Registro de registro do usuário será usado se as seguintes condições forem atendidas:

* O registro de registro foi ativado no painel de administração do wordpress e
* o usuário tem uma conta de Registro e
* um avatar personalizado não é fornecido.

Para obter mais informações, consulte a documentação do wordpress Registatar.



Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Cartão de recursos](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Revisões](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

