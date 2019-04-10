---
description: Crie aplicativos do Livefyre do zero para criar experiências personalizadas
  e visualizações de dados.
seo-description: Crie aplicativos do Livefyre do zero para criar experiências personalizadas
  e visualizações de dados.
seo-title: Integrar Livefyre com integração de terceiros
solution: Experience Manager
title: Integrar o Livefyre em um CMS
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Implementar o Livefyre com integração de terceiros

Crie aplicativos do Livefyre do zero para criar experiências personalizadas e visualizações de dados.

Você pode criar um aplicativo do Livefyre do zero, consumindo o Livefyre e os dados sociais usando a API de bootstrap e de fluxo.

Para aplicativos do Livefyre que exigem autenticação, consulte Integração de identidade para obter informações sobre plataformas de autenticação de terceiros suportadas.

Para implementar Aplicativos de conversa (Comentários, Bate-papo, Blog ativo, Sidenotes):

1. Execute a integração do aplicativo.
a. Criar uma coleção usando o collectionmeta Token.
b. Integrar aplicativos do Livefyre a sites usando a estrutura de código incorporado do Livefyre. js.

   * Para obter mais informações sobre como usar a estrutura de código incorporado do Livefyre. js, consulte [Incorporar um aplicativo](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obter informações sobre como integrar o Aplicativo de comentários, consulte [Comentários](/help/using/c-about-apps/c-comments/c-comments.md).

   * Para obter informações sobre como integrar o aplicativo de bate-papo, consulte [Bate-papo](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Para obter informações sobre como integrar o aplicativo de blog ao vivo, consulte [Blog online](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Para obter informações sobre como integrar o aplicativo de sidenotes, consulte [Auxiliar](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Realizar integração de autenticação.
a. Criar tokens de autenticação do usuário para transmitir e armazenar dados do usuário no Livefyre.
b. Integrar plataformas de usuário e autenticação de terceiros. Para obter uma lista das plataformas compatíveis, consulte [Integração de identidade](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Executar personalizações do aplicativo. As opções de Personalização do aplicativo correspondem à marca e ao estilo e adicionam funcionalidades personalizadas.

Para criar um Aplicativo de visualização (Mapa, Media Wall, Trending, Carousel, Filmstrip, Storify, Feature Card, Mosaic, Survey):

1. Execute a integração do aplicativo.
a. Criar uma coleção usando o collectionmeta Token.
b. Integrar aplicativos do Livefyre a sites usando a estrutura de código incorporado do Livefyre. js. Para obter mais informações sobre como usar a estrutura de código incorporado do Livefyre. js, consulte [Incorporar um aplicativo](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obter informações sobre como integrar o aplicativo Mapa, consulte [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Para obter informações sobre como integrar o aplicativo de mídia de mídia, consulte [o Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Para obter informações sobre como integrar o Aplicativo de tendência, consulte [Tendência](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Realizar integração de autenticação.
a. Criar tokens de autenticação do usuário para transmitir e armazenar dados do usuário no Livefyre.
b. Integrar plataformas de usuário e autenticação de terceiros. Para obter uma lista das plataformas compatíveis, consulte [Integração de identidade](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>O Livefyre não é compatível com Carrossel, Película fotográfica, Storify, Cartão de recursos, Mosaico e Aplicativos de pesquisas usando o Livefyre. js.
Integre esses aplicativos usando o [processo Criar um aplicativo](/help/using/c-about-apps/c-create-an-app.md) .