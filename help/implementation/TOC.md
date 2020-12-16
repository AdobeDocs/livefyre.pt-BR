---
product: livefyre
audience: end-user
user-guide-title: Guia de implementação do Livefyre
translation-type: tm+mt
source-git-commit: 3664bc1c51d2b372c358385127a1ca9c2f0cfef8
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 4%

---


# Guia de implementação do Livefyre {#implementation}

+ [Guia de implementação do Livefyre](home.md)
+ Introdução {#getting-started}
   + [Introdução à integração do Livefyre](c-getting-started/c-getting-started.md)
   + Processo de implementação {#implementation-process}
      + [Processo de implementação](c-getting-started/c-implementation-process/c-implementation-process.md)
      + [Tipos de integração de aplicativo](c-getting-started/c-implementation-process/c-app-integration-types.md)
      + [Implementação do aplicativo](c-getting-started/designer-app-implementation.md)
      + [Implementação do Livefyre com integração de terceiros](c-app-integrations/implement-livefyre-3rd-party.md)
      + [Arquitetura](c-getting-started/c-implementation-process/c-architecture.md)
      + [Incorporar um aplicativo](c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)
      + [Adicionar autenticação a um aplicativo usando Livefyre.js](c-getting-started/c-implementation-process/c-add-authetication-to-an-app-using-livefyre.js.md)
      + [Criar tokens do lado do servidor](c-getting-started/c-implementation-process/c-build-server-side-tokens.md)
      + [CollectionMeta Token](c-getting-started/c-implementation-process/c-collectionmeta-tokent.md)
      + [Token de autenticação do usuário](c-getting-started/c-implementation-process/c-user-auth-token.md)
      + [Criar uma coleção usando o CollectionMeta Token](t-create-a-collectionmeta-token.md)
      + [Criação de uma soma de verificação](c-creating-a-checksum.md)
+ Integração de identidade {#identity-integration}
   + [Integração de identidade](t-about-identity-integration/t-about-identity-integration.md)
   + [Pacote de autenticação](t-about-identity-integration/c-authorization-package.md)
   + [Objeto AuthDelegate](t-about-identity-integration/c-building-an-auth-delegate.md)
   + [Contabilização de permissões de usuário para sistemas externos (opcional)](t-about-identity-integration/c-posting-user-permissions-to-external-systems.md)
   + Implementar SSO {#implementing-sso}
      + [Implementação do SSO](t-about-identity-integration/c-implementing-sso/c-implementing-sso.md)
      + [Depuração do delegado de autenticação](t-about-identity-integration/c-implementing-sso/c-debugging-auth.md)
   + Sincronizar com Livefyre {#sync-ping-for-pull}
      + [Sincronizar com o Livefyre usando o Ping para puxar](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)
      + [Criar o ponto de extremidade de puxamento](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-pull-endpoint.md)
      + [Registrar o Ponto de Extremidade no Studio](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-register-the-endpoint-with-studio.md)
      + [Criar o ping](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-ping.md)
      + [Estrutura de solicitação de puxamento](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-pull-request-structure.md)
      + [Criar o Ping para Resposta de Puxo](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-build-the-ping-for-pull-response.md)
+ Livefyre Identity {#livefyre-identity}
   + [Identidade do Livefyre](c-livefyre-identity-comp/c-livefyre-identity-comp.md)
   + [Ativar a identidade do Livefyre](c-livefyre-identity-comp/t-enable-livefyre-identity.md)
   + Usar aplicativos do Social com identificação do Livefyre {#use-social-apps-with-livefyre-identity}
      + [Criar seus aplicativos sociais](c-livefyre-identity-comp/t-create-your-social-apps.md)
      + [Criar um aplicativo do Facebook para uso com a Livefyre Identity](c-livefyre-identity-comp/t-create-a-facebook-app-for-use-with-livefyre-identity.md)
      + [Criar um aplicativo do Twitter para uso com a Livefyre Identity](c-livefyre-identity-comp/t-create-a-twitter-app-for-use-with-livefyre-identity.md)
      + [Crie um Yahoo! Aplicativo para uso com Livefyre Identity](c-livefyre-identity-comp/t-create-a-yahoo-app-for-use-with-livefyre-identity.md)
      + [Criar um aplicativo Microsoft Live Identity para uso com a Livefyre Identity](c-livefyre-identity-comp/t-create-a-microsoft-live-id-app-for-use-with-livefyre-identity.md)
      + [Criar um aplicativo do LinkedIn para uso com a Livefyre Identity](c-livefyre-identity-comp/t-create-a-linkedin-app-for-use-with-livefyre-identity.md)
      + [Criar um aplicativo de identidade GitHub para uso com a identidade do Livefyre](c-livefyre-identity-comp/c-create-a-github-identity.md)
      + [Uso do Studio para conectar seus aplicativos sociais à implementação do Livefyre](c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)
   + [Adicionar Livefyre.js à página](c-livefyre-identity-comp/t-add-livefyre.js-to-the-page.md)
   + [Inicializar a identidade do Livefyre](c-livefyre-identity-comp/t-initialize-livefyre-identity.md)
   + [Emails para a identidade do Livefyre](c-livefyre-identity-comp/c-emails-for-livefyre-identity.md)
   + [Captura de Janrain/Backplane](c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)
   + Instalação {#installation}
      + [Instalação de bibliotecas](c-installing-libraries/c-installing-libraries.md)
      + [Classes e métodos](c-installing-libraries/c-methods-livefyre.md)
      + [Métodos de rede](c-installing-libraries/c-network-methods.md)
      + [método de rede setSSL](c-installing-libraries/r-setssl-method.md)
      + [método de rede buildLivefyreToken](c-installing-libraries/r-buildlivefyretoken-method.md)
      + [método de rede buildUserAuthToken](c-installing-libraries/r-builduserauthtoken-method.md)
      + [Método de Rede validateLivefyreToken](c-installing-libraries/c-validatelivefyretoken-network-method.md)
      + [método de rede setUserSyncUrl](c-installing-libraries/r-setusersyncurl-method.md)
      + [método de rede syncUser](c-installing-libraries/r-syncuser-method.md)
      + [Método de rede getUrn](c-installing-libraries/r-geturn-method.md)
      + [Método de Rede getUrnForUser](c-installing-libraries/r-geturnforuser-method.md)
      + [Método de Rede getNetworkName](c-installing-libraries/r-getnetworkname-method.md)
      + [Método de rede getSite](c-installing-libraries/r-getsite-method.md)
      + [Métodos de classe de rede](c-installing-libraries/c-network-class-methods.md)
      + [Métodos de classe de coleção](c-installing-libraries/c-collection-methods.md)
      + [método de coleta createOrUpdate](c-installing-libraries/r-createorupdate-collection-method.md)
      + [método de coleta buildCollectionMetaToken](c-installing-libraries/r-buildcollectionmetatoken-collection-method.md)
      + [método de coleta buildChecksum](c-installing-libraries/r-buildchecksum-collection-method.md)
      + [Método de coleta getCollectionContent](c-installing-libraries/t-getcollectioncontent-collection-method.md)
      + [Método de Coleção getUrn](c-installing-libraries/r-geturn-collection-method.md)
      + [Métodos de classe do site](c-installing-libraries/c-site-methods.md)
      + [método de site buildBlogCollection](c-installing-libraries/r-buildblogcollection-site-method.md)
      + [método de site buildChatCollection](c-installing-libraries/r-buildchatcollection-site-method.md)
      + [método de site buildCommentsCollection](c-installing-libraries/r-buildcommentscollection-site-method.md)
      + [método de site buildCountingCollection](c-installing-libraries/r-buildcountingcollection-site-method.md)
      + [método de site buildRatingsCollection](c-installing-libraries/r-buildratingscollection-site-method.md)
      + [método de site buildReviewsCollection](c-installing-libraries/r-buildreviewscollection-site-method.md)
      + [método de site buildSitenotesCollection](c-installing-libraries/r-buildsitenotescollection-site-method.md)
      + [método de site buildCollection](c-installing-libraries/r-buildcollection-site-method.md)
      + [Método do site getUrn](c-installing-libraries/r-geturn-site-method.md)
      + [Exemplos](c-installing-libraries/c-libraries-examples.md)
   + SDKs móveis {#mobile-sdks}
      + [SDKs móveis](c-mobile-sdks/c-mobile-sdks.md)
      + [Livefyre iOS SDK](c-mobile-sdks/c-livefyre-ios-sdk.md)
      + [Android SDK](c-mobile-sdks/c-android-sdk.md)
+ [Livefyre.js](c-livefyre.js.md)
+ [Criando Tokens Livefyre C#](c-creating-livefyre-tokens-c-.md)
+ Integrações de aplicativos {#app-integrations}
   + [Bate-papo](c-app-integrations/c-app-integratios-chat.md)
   + Comentários {#comments}
      + [Comentários](c-app-integrations/c-comments-integration/c-comments-integration.md)
   + [Blog ao vivo](c-app-integrations/c-live-blog-integration.md)
   + [Resenhas](c-app-integrations/c-reviews-integration.md)
   + Sidenotes {#sidenotes}
      + [Integração com Sidenotes](c-app-integrations/c-sidenotes-integration/r-sidenotes-integration.md)
      + [Adicionar notas de identidade a uma página](c-app-integrations/c-sidenotes-integration/r-adding-sidenotes-to-a-page.md)
      + [Eventos do aplicativo Sidenotes](c-app-integrations/c-sidenotes-integration/r-app-events.md)
      + [Opções de configuração do Sidenotes](c-app-integrations/c-sidenotes-integration/r-configuration-options.md)
      + [Estilos Personalizados de Sidenotes](c-app-integrations/c-sidenotes-integration/r-custom-styles.md)
      + [Separa strings personalizadas](c-app-integrations/c-sidenotes-integration/r-custom-strings.md)
      + [Implementação de Sidenotes](c-app-integrations/c-sidenotes-integration/r-sidenotes-implementation.md)
      + [método updateAnchors](c-app-integrations/c-sidenotes-integration/update-anchors-method.md)
   + [Mapa](c-app-integrations/c-map-integration.md)
   + [Mídia](c-app-integrations/c-media-wall-integration.md)
   + [Tendência](c-app-integrations/c-trending-integration.md)
+ Personalizações do aplicativo {#app-customizations}
   + [Personalizações do aplicativo](c-app-customizations/c-app-customizations.md)
   + [Alterar opções de exibição](c-app-customizations/c-change-display-options.md)
   + [Classes CSS](c-app-customizations/c-css-classes.md)
   + [Storify CSS Classes](c-app-customizations/c-storify-css-classes.md)
   + [Conjuntos de Tradução](c-app-customizations/c-translation-sets.md)
   + [Mova o logotipo Livefyre](c-app-customizations/c-move-the-livefyre-logo.md)
   + [Restringir mídia](c-app-customizations/c-restrict-media.md)
   + [Ocultar elementos do aplicativo](c-app-customizations/c-hide-app-elements.md)
   + [Alterar ícone de @mention](c-app-customizations/c-change-mention-icon.md)
   + [Realçar conteúdo](c-app-customizations/c-highlight-content.md)
   + [Personalizar o carimbo de data e hora](c-app-customizations/c-date-time-stamp.md)
   + Conteúdo do recurso {#feature-content}
      + [Conteúdo do recurso](c-app-customizations/t-feature-content.md)
      + [Habilitar conteúdo em destaque no Studio](c-app-customizations/t-enable-featuring-content-in-studio.md)
      + [Selecionar conteúdo para recurso de um aplicativo](c-app-customizations/t-select-content-to-feature.md)
      + [Selecionar conteúdo para o recurso do Studio](c-app-customizations/t-select-content-to-feature-from-studio.md)
      + [Usar CSS para estilos de conteúdo em destaque](c-app-customizations/c-use-css-to-style-featured-content.md)
      + [APIs de recursos](c-app-customizations/c-feature-apis.md)
   + [Conectando Janrain ao Livefyre usando AuthDelegate](c-app-customizations/c-connecting-janrain-to-livefyre-using-authdelegate.md)
   + [Conteúdo agregado em destaque usando as APIs em destaque](c-app-customizations/c-aggregated-featured-content-using-the-featured-apis.md)
   + Conteúdo do estilo {#style-content}
      + [Estilo de conteúdo do grupo de usuários](c-app-customizations/c-style-user-group-content.md)
      + [Adicionar usuários a grupos](c-app-customizations/c-adding-users-to-groups.md)
   + Aplicar estilos personalizados {#apply-custom-styles}
      + [Aplicação de estilos personalizados](c-app-customizations/c-applying-custom-styles-.md)
      + [Adicionar botões personalizados](c-app-customizations/t-add-custom-buttons.md)
   + Eventos Javascript {#javascript-events}
      + [Definições e exemplos de Eventos JavaScript](c-app-customizations/c-javascript-events.md)
      + [Eventos Javascript para aplicativos de visualização](c-app-customizations/c-javascript-events-for-visualization-apps.md)
      + [Eventos Javascript para Media Wall](c-app-customizations/c-javascript-events-media-wall.md)
      + [Eventos Javascript para aplicativos de conversa](c-app-customizations/c-javascript-events-for-conversation-apps.md)
   + [Incorporar um aplicativo de comentários](c-app-customizations/c-embed-a-comments-app.md)
   + [Rastreamento de referência](c-app-customizations/c-referral-tracking.md)
   + [Suporte a dispositivos e navegadores](c-app-customizations/c-device-and-browser-support.md)
   + [Requisitos de exibição do Twitter](c-app-customizations/c-twitter-display-requirements.md)
+ [Política de teste de stress](c-stress-test-policy.md)
+ Analytics {#analytics}
   + [Analytics](livefyre-analytics/livefyre-analytics.md)
   + [Use o Livefyre com Adobe Analytics e o Gerenciador dinâmico de tags (DTM)](livefyre-analytics/c-use-livefyre-with-adobe-analytics.md)
   + [Usar o Livefyre com outra ferramenta do Analytics](livefyre-analytics/c-livefyre-analytics.md)
   + [Eventos do Livefyre Analytics](livefyre-analytics/c-livefyre-analytics-events.md)
+ [Integração do Livefyre com AEM](c-livefyre-aem-integration.md)
+ Tópicos avançados {#advanced-topics}
   + [Exibir contagem de comentários](c-advanced-topics/t-display-comment-count.md)
   + [Habilitar compartilhamento em redes sociais](c-advanced-topics/c-enabling-social-sharing.md)
   + [Fluxo de atividade](c-advanced-topics/c-activity-stream.md)
   + [HTML do Bootstrap](c-advanced-topics/c-bootstrap-html.md)
   + [Alterar coleção](c-advanced-topics/c-change-collection.md)
   + [Várias coleções](c-advanced-topics/c-multiple-collections.md)
   + [Alternar entre os principais tipos de aplicativos](c-advanced-topics/c-switch-core-app-types.md)
   + [Contador social](c-advanced-topics/c-social-counter.md)
   + [Usar a Bootsrap e a Stream API com aplicativos Livefyre](c-advanced-topics/bootstrap-stream-api.md)
