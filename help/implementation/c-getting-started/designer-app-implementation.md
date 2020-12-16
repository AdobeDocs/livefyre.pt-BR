---
description: Use a API Bootstrap e fluxo com aplicativos Livefyre.
seo-description: Use a API Bootstrap e fluxo com aplicativos Livefyre.
seo-title: Implementação do aplicativo
solution: Experience Manager
title: Implementação do aplicativo
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Implementação do aplicativo {#appimplementation}

Caso de uso: Como cliente, desejo integrar o Livefyre ao meu CMS de terceiros usando o método Livefyre.js.

Há três maneiras de implementar o Livefyre em um componente AEM personalizado ou em outros CMS, como WordPress, Sitecore ou DemandWare: Implementação do aplicativo Designer, API, implementação e integração de autenticação de terceiros.

## Implementação do aplicativo Designer {#designerapp}

O que: A maneira mais fácil e rápida de integrar um aplicativo Livefyre. Você pode projetar, configurar e gerar um código incorporado personalizado do Javascript para integrar um aplicativo Liveyfre em uma página em minutos.

Como: [Criar, Pré-visualização, Publicar e Incorporar um aplicativo Livefyre](/help/using/c-about-apps/c-create-an-app.md)

Exemplo: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Implementação do Livefyre.js {#livefyrejsimp}

O que: [Livefyre.js](/help/implementation/c-livefyre.js.md) é a biblioteca principal que alimenta aplicativos e autenticação em um site. Ele define o objeto `window.Livefyre` global e um único método público, o Livefyre.requirements, que pode ser usado para carregar outras bibliotecas do Livefyre JavaScript que ajudam a incorporar aplicativos Livefyre e a integrar plataformas de autenticação de usuário de terceiros.

Como:

* [Criar uma coleção usando o CollectionMeta Token](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrar aplicativos a CMS de terceiros usando integrações de aplicativos

Exemplos:

* Aplicativo de comentários: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Revisões do aplicativo: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Mídia: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Para personalizações avançadas usando o SDK, consulte SDKs do StreamHub.

## Implementação da API {#apiimplementation}

Para criar experiências personalizadas e visualizações de dados, os aplicativos Livefyre podem ser criados do zero, consumindo o Livefyre e os dados sociais usando a API Bootstrap e Stream.

## Integração de autenticação de terceiros {#thirdpartyauth}

Para aplicativos Livefyre que exigem autenticação, consulte [Integração de identidade](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) para plataformas de autenticação de terceiros.

## Exemplos de cliente {#customerexamples}

Os seguintes clientes implementaram o Livefyre com integrações CMS de terceiros:

* [Mídia de tour PGA](https://www.pgatour.com/social-hub.html)

* [Tempo limite](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
