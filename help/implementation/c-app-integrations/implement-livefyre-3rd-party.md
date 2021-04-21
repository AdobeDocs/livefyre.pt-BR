---
description: Crie aplicativos do Livefyre do zero para criar experiências e visualizações de dados personalizadas.
title: Integre o Livefyre em um CMS
exl-id: 05d85792-de97-47b1-90cc-ad7e841754b5
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Implementar o Livefyre com integração de terceiros

Crie aplicativos do Livefyre do zero para criar experiências e visualizações de dados personalizadas.

Você pode criar um aplicativo Livefyre do zero, consumindo o Livefyre e os dados sociais usando a API Bootstrap e Stream.

Para aplicativos do Livefyre que exigem autenticação, consulte Integração de identidade para obter informações sobre plataformas de autenticação de terceiros compatíveis.

Para implementar Aplicativos de Conversação (Comentários, Chat, Blog Ao Vivo, Observações):

1. Realize a integração do aplicativo.
a. Crie uma coleção usando o token CollectionMeta.
b. Integre os aplicativos do Livefyre a sites usando a estrutura de código de inserção do Livefyre.js.

   * Para obter mais informações sobre como usar a estrutura do código incorporado Livefyre.js, consulte [Incorporar um aplicativo](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obter informações sobre como integrar o aplicativo Comentários, consulte [Comentários](/help/using/c-about-apps/c-comments/c-comments.md).

   * Para obter informações sobre como integrar o Aplicativo de Chat, consulte [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Para obter informações sobre como integrar o aplicativo Live Blog, consulte [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Para obter informações sobre como integrar o aplicativo Sidenotes, consulte [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Realize a integração de autenticação.
a. Crie tokens de Auth do usuário para enviar e armazenar dados do usuário no Livefyre.
b. Integre plataformas de autenticação e de usuário de terceiros. Para obter uma lista de plataformas compatíveis, consulte [Integração de identidade](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Execute personalizações do aplicativo. Opções de Personalizações de aplicativo para corresponder à sua marca e estilo e adicionar funcionalidade personalizada.

Para criar um aplicativo de visualização (Mapa, Mural de mídia, Tendência, Carrossel, Tira de filme, Storify, Cartão de recursos, Mosaic, Pesquisas):

1. Realize a integração do aplicativo.
a. Crie uma coleção usando o token CollectionMeta.
b. Integre os aplicativos do Livefyre a sites usando a estrutura de código de inserção do Livefyre.js. Para obter mais informações sobre como usar a estrutura do código incorporado Livefyre.js, consulte [Incorporar um aplicativo](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Para obter informações sobre como integrar o Aplicativo de mapa, consulte [Mapa](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Para obter informações sobre como integrar o Aplicativo de mural de mídia, consulte [Mural de mídia](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Para obter informações sobre como integrar o Aplicativo de tendência, consulte [Tendência](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Realize a integração de autenticação.
a. Crie tokens de Auth do usuário para transmitir e armazenar dados do usuário no Livefyre.
b. Integre plataformas de autenticação e de usuário de terceiros. Para obter uma lista de plataformas compatíveis, consulte [Integração de identidade](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>O Livefyre não é compatível com os aplicativos Carrossel, FilmStrip, Storify, Feature Card, Mosaic e Polls usando Livefyre.js.

Integre esses aplicativos usando o processo [Criar um aplicativo](/help/using/c-about-apps/c-create-an-app.md) .
