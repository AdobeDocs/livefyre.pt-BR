---
description: Use o Bootstrap e a API de fluxo com aplicativos do Livefyre.
seo-description: Use o Bootstrap e a API de fluxo com aplicativos do Livefyre.
seo-title: Implementação do aplicativo
solution: Experience Manager
title: Implementação do aplicativo
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---

# Implementação do aplicativo {#appimplementation}

Caso de uso: Como cliente, quero integrar o Livefyre ao CMS de terceiros usando o método Livefyre. js.

Há três maneiras de implementar o Livefyre em um componente AEM personalizado ou em outro CMS, como wordpress, Sitecore ou demandware: Implementação de aplicativos do Designer, API, implementação e integração de autenticação de terceiros.

## Implementação de aplicativos do Designer {#designerapp}

O que: Maneira mais simples e rápida de integrar um aplicativo do Livefyre. Você pode criar, configurar e gerar um código incorporado personalizado do Javascript para integrar um Aplicativo do Liveyfre em uma página em minutos.

Como: [Criar, visualizar, publicar e incorporar um aplicativo do Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Exemplo: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementação do Livefyre. js {#livefyrejsimp}

O que: [Livefyre. js](/help/implementation/c-livefyre.js.md) é a biblioteca principal que capacita Aplicativos e Auth em um site. Ele define o objeto global `window.Livefyre` e um único método público, Livefyre. exigir, que pode ser usado para carregar outras bibliotecas do Livefyre javascript que ajudam a incorporar aplicativos do Livefyre e a integração com plataformas de autenticação de usuário de terceiros.

Como:

* [Criar uma coleção usando o collectionmeta token](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrar aplicativos em CMS de terceiros usando Integrações de aplicativo

Exemplos:

* Aplicativo de comentários: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Aplicativo app: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Media Wall: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Para personalizações avançadas usando o SDK, consulte sdks do streamhub.

## Implementação da API {#apiimplementation}

Para criar experiências personalizadas e visualizações de dados, os Aplicativos do Livefyre podem ser criados do zero lendo o Livefyre e os dados sociais usando a API de bootstrap e de fluxo.

## Integração de autenticação de terceiros {#thirdpartyauth}

Para aplicativos do Livefyre que exigem autenticação, consulte [Integração de identidade](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) para plataformas de autenticação de terceiros.

## Exemplos do cliente {#customerexamples}

Os seguintes clientes implementaram o Livefyre com Integrações CMS de terceiros:

* [PGA Tour Media Wall](https://www.pgatour.com/social-hub.html)

* [Timeout](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
