---
description: Use embed.ly para exibir vários formatos de mídia, diretamente no aplicativo.
seo-description: Use embed.ly para exibir vários formatos de mídia, diretamente no aplicativo.
seo-title: Integração do Embedly
solution: Experience Manager
title: Integração do Embedly
uuid: 1 f 27 e 32 c-c 2 c 3-4 f 7 c -93 de-c 9 c 7 bf 783 d 6 a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Integração do Embedly {#embedly-integration}

Use `embed.ly` para exibir vários formatos de mídia, diretamente no aplicativo.

Para habilitar melhor o conteúdo de mídia incorporado de uma variedade de fontes, incluindo o Google Maps, o youtube, o Flickr, o Facebook, o Instagram, o Spotify e o Tumblr, os aplicativos Livefyre usam Incorporados como um provedor de terceiros para a expansão de URL. Se um usuário ou moderador incluir um link suportado em uma publicação, a mídia incluída no link será expandida quando publicada para a Coleção.

Isso fornece aplicativos do Livefyre com acesso a mais de 250 opções de mídia incorporadas diferentes que são suportadas por inteiro.

>[!NOTE]
>
>O Livefyre expande apenas um subconjunto da lista completa de provedor de provedores. As imagens incorporadas serão expandidas em páginas HTTPS somente se o provedor for Twitter, youtube, Imgur, Vinho, Wikipedia ou soundcloud. Entre em contato com o Gerente de conta técnico para obter mais perguntas sobre a expansão de links ou as fontes.

Esta página lista exemplos de alguns tipos de mídia incorporados populares e seus padrões aceitáveis de URL. `Embed.ly` está adicionando novas fontes continuamente. Para obter uma lista completa dos provedores, `https://embed.ly/embed/features/providers`acesse.

>[!NOTE]
>
>A formatação Incorporar requer um permalink completo. Links encurtados não funcionarão.

Somente o conteúdo visível publicamente pode ser incorporado. Se você tentar incorporar um conteúdo que não seja público, o link para o conteúdo aparecerá na postagem do blog e um ícone de espaço reservado acompanhará-o. Quando clicado, o link levará o leitor para uma mensagem de erro do serviço em que o conteúdo está hospedado, como uma mensagem do Facebook para uma foto somente de amigos. Entre em contato com seu Gerente de contas se perceber que a mídia não é expandida como esperado.

## Amostra de urls incorporados

| Tipo | Provedor | Urls |
|--- |--- |--- |
| Mapas | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Observação**: O URL deve começar `http` com e não `https.` |
| Redes sociais | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Vídeo | Youtube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Fotos | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | Twitpic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Serviço de carregamento de conteúdo do Hootsuite) | `https://ow.ly/i/*` |
| Pesquisas | Gopollgo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Áudio | Soundcloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Cartão de recursos](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Pesquisas](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Revisões](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Auxiliares](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Tendência](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Botão Upload](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

