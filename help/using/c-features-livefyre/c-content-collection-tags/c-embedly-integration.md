---
description: Use embed.ly para exibir vários formatos de mídia, diretamente no aplicativo.
title: Integração do Embedly
exl-id: 859fe306-367e-4207-b9f7-c730ba0cd24d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 11%

---

# Integração do Embedly {#embedly-integration}

Use `embed.ly` para exibir vários formatos de mídia, diretamente no aplicativo.

Para melhor habilitar o conteúdo de mídia inserido de várias fontes, incluindo Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify e Tumblr, os aplicativos do Livefyre usam o Embedly como provedor terceirizado para expansão de URL. Se um usuário ou moderador incluir um link compatível em uma publicação, a mídia incluída no link será expandida quando for publicada na Coleção.

Isso fornece aos aplicativos Livefyre acesso às mais de 250 opções de mídia incorporada diferentes compatíveis com Embedly.

>[!NOTE]
>
>O Livefyre expande apenas um subconjunto da lista completa de provedores do Embedly. Imagens incorporadas serão expandidas em páginas HTTPS somente se o provedor for Twitter, YouTube, Imgur, Vine, Wikipédia ou SoundCloud. Entre em contato com o Gerente de conta técnica para dúvidas sobre a expansão ou fontes de links.

Esta página lista exemplos de alguns tipos populares de mídia incorporada e seus padrões aceitáveis de URL. `Embed.ly` O está adicionando continuamente novas fontes. Para obter uma lista completa de provedores, vá para `https://embed.ly/embed/features/providers`.

>[!NOTE]
>
>A formatação Embedly requer um permalink completo. Links encurtados não funcionarão.

Somente o conteúdo visualizável publicamente pode ser incorporado. Se você tentar incorporar um conteúdo que não é público, o link para o conteúdo será exibido na publicação do blog e um ícone de espaço reservado o acompanhará. Quando clicado, o link direcionará o leitor a uma mensagem de erro do serviço em que o conteúdo está hospedado, como uma mensagem Facebook para uma foto de apenas amigos. Entre em contato com o Gerente de conta se você notar que a mídia não é expandida conforme esperado.

## Exemplos de URLs do Email

| Tipo | Provedor | URLs |
|--- |--- |--- |
| Mapas | Mapas do Google | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Observação**: O URL deve começar com  `http` e não  `https.` |
| Redes sociais | Google+ | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Vídeo | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Fotos | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Serviço de upload de conteúdo do conjunto de hosts) | `https://ow.ly/i/*` |
| Pesquisas | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Áudio | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Aplicativos que usam este recurso:

* [Carrossel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comentários](/help/using/c-about-apps/c-comments/c-comments.md)
* [Placa de recurso](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Mural de mídia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaico](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Pesquisas](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Resenhas](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Observações](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Tendência](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Botão Upload](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
