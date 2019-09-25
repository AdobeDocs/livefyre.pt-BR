---
description: Crie aplicativos Livefyre do zero para criar experiências e visualizações de dados personalizadas.
seo-description: Crie aplicativos Livefyre do zero para criar experiências e visualizações de dados personalizadas.
seo-title: Integrar o Livefyre à integração de terceiros
solution: Experience Manager
title: Integre o Livefyre em um CMS
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 40cd8c2c89c17134bfcda510527dd6fff41400b5

---


# Implementação do Livefyre com integração de terceiros

Crie aplicativos Livefyre do zero para criar experiências e visualizações de dados personalizadas.

Você pode criar um aplicativo Livefyre do zero, usando o Livefyre e os dados sociais usando a Bootstrap e a Stream API.

Para aplicativos Livefyre que exigem autenticação, consulte Integração de identidade para obter informações sobre plataformas de autenticação de terceiros suportadas.

Para implementar aplicativos de conversa (Comentários, bate-papo, Blog ao vivo, Sidenotes):

1. Execute a integração do aplicativo.
a. Crie uma coleção usando o CollectionMeta Token.
b. Integre aplicativos Livefyre a sites usando a estrutura de código incorporada do Livefyre.js.

   * Para obter mais informações sobre como usar a estrutura de código incorporado Livefyre.js, consulte [Incorporar um aplicativo](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obter informações sobre como integrar o aplicativo Comentários, consulte [Comentários](/help/using/c-about-apps/c-comments/c-comments.md).

   * Para obter informações sobre como integrar o aplicativo de bate-papo, consulte [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Para obter informações sobre como integrar o aplicativo Live Blog, consulte [Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md)ao vivo.

   * Para obter informações sobre como integrar o aplicativo Sidenotes, consulte [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Realize a integração de autenticação.
a. Crie tokens de autenticação de usuário para transmitir e armazenar dados de usuário no Livefyre.
b. Integre plataformas de autenticação e de usuário de terceiros. Para obter uma lista das plataformas compatíveis, consulte Integração [de](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)identidade.

1. Execute personalizações do aplicativo. Opções de personalização do aplicativo para corresponder à sua marca e estilo e adicionar funcionalidade personalizada.

Para criar um aplicativo de visualização (Mapa, Mídia, Mural, Tendência, Carrossel, Película fotográfica, Storify, Cartão de recurso, Mosaico, Pesquisas):

1. Execute a integração do aplicativo.
a. Crie uma coleção usando o CollectionMeta Token.
b. Integre aplicativos Livefyre a sites usando a estrutura de código incorporada do Livefyre.js. Para obter mais informações sobre como usar a estrutura de código incorporado Livefyre.js, consulte [Incorporar um aplicativo](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obter informações sobre como integrar o aplicativo Mapa, consulte [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Para obter informações sobre como integrar o aplicativo Media Wall, consulte [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Para obter informações sobre como integrar o aplicativo de tendência, consulte [Tendências](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Realize a integração de autenticação.
a. Crie tokens de autenticação de usuário para enviar e armazenar dados de usuário no Livefyre.
b. Integre plataformas de autenticação e de usuário de terceiros. Para obter uma lista das plataformas compatíveis, consulte Integração [de](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)identidade.

>[!NOTE]
>
>O Livefyre não é compatível com os aplicativos Carousel, Filmstrip, Storify, Feature Card, Mosaic e Polls usando o Livefyre.js.
Integre esses aplicativos usando o processo [Criar um aplicativo](/help/using/c-about-apps/c-create-an-app.md) .