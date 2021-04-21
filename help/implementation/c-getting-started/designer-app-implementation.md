---
description: Use a API de fluxo e do Bootstrap com os aplicativos Livefyre.
title: Implementação do aplicativo
uuid: null
exl-id: f1edef86-491d-4f8e-8ce5-f6e019d057ec
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Implementação do aplicativo {#appimplementation}

Caso de uso: Como cliente, desejo integrar o Livefyre ao meu CMS de terceiros usando o método Livefyre.js.

Há três maneiras de implementar o Livefyre em um componente de AEM personalizado ou em outros CMS, como WordPress, Sitecore ou DemandWare: Implementação do aplicativo Designer, API, Implementação e Integração de autenticação de terceiros.

## Implementação do aplicativo Designer {#designerapp}

O que: A maneira mais fácil e rápida de integrar um aplicativo Livefyre. Você pode projetar, configurar e gerar um código incorporado Javascript personalizado para integrar um aplicativo Liveyfre em uma página em minutos.

Como: [Criar, Visualizar, Publicar e Incorporar um aplicativo Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Exemplo: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementação do Livefyre.js {#livefyrejsimp}

O que: [Livefyre.js](/help/implementation/c-livefyre.js.md) é a biblioteca principal que alimenta os aplicativos e o Auth em um site. Ela define o objeto global `window.Livefyre` e um único método público, Livefyre.require, que pode ser usado para carregar outras bibliotecas JavaScript do Livefyre que ajudam a incorporar os aplicativos do Livefyre e a integrar com plataformas de autenticação de usuário de terceiros.

Como:

* [Criar uma coleção usando o token CollectionMeta](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrar aplicativos a CMS de terceiros usando integrações de aplicativos

Exemplos:

* Aplicativo de comentários: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Aplicativo de revisões: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Mural de mídia: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Para personalizações avançadas usando o SDK, consulte SDKs do StreamHub.

## Implementação da API {#apiimplementation}

Para criar experiências personalizadas e visualizações de dados, os aplicativos do Livefyre podem ser criados do zero ao consumir o Livefyre e os dados sociais usando a API de fluxo e o Bootstrap.

## Integração de autenticação de terceiros {#thirdpartyauth}

Para aplicativos Livefyre que exigem autenticação, consulte [Integração de identidade](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) para plataformas de autenticação de terceiros.

## Exemplos de cliente {#customerexamples}

Os seguintes clientes implementaram o Livefyre com integrações de CMS de terceiros:

* [Mural de mídia de turnê PGA](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
