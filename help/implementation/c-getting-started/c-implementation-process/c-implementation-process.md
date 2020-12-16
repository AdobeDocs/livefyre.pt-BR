---
description: O que esperar na implementação do Livefyre Studio.
seo-description: O que esperar na implementação do Livefyre Studio.
seo-title: Processo de implementação
solution: Experience Manager
title: Processo de implementação
uuid: 9a0f394e-3467-47d1-9816-45e2130db440
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 3%

---


# Processo de implementação{#implementation-process}

A duração da implementação do Livefyre depende da implementação e do escopo do trabalho.

## Visão geral da arquitetura de rede Livefyre {#section_dgj_l32_rbb}

O Livefyre usa os seguintes termos para discutir a arquitetura de rede:

* Rede. O domínio de mais alto nível no qual você planeja usar o Livefyre.
* Sites. Um subdomínio ou seção de site que faz parte da rede.
* Aplicativos. Uma renderização de conteúdo em seu site. O conteúdo é exibido nos aplicativos visualmente, usando aplicativos de visualização (mosaico, carrossel, cartão de recursos etc.) ou no formato de texto, usando aplicativos de conversa (Comentários, revisões, bate-papo etc.). Você pode colocar um ou mais aplicativos em seus sites.
* Fluxos. Os fluxos são filtros que pesquisam nas redes sociais e em outros sites para coletar conteúdo automaticamente para moderação ou publicação direta em um aplicativo.
* Conteúdo (por exemplo, UGC, comentários). O que é exibido nos aplicativos. O conteúdo pode ser visual (por exemplo, uma foto ou vídeo), somente áudio ou texto.

O diagrama a seguir mostra a relação entre Rede, Sites, Aplicativos e Conteúdo.

![](assets/network_site_architecture.png)

Você tem sua própria instância do Livefyre, que é seu painel central para moderar o conteúdo, gerenciar usuários e muito mais. Entre em contato com o CSM para obter acesso à sua instância do Livefyre.

## Etapas de integração {#section_s2j_d2x_tz}

Existem três etapas principais para a integração do Livefyre:

* Integração de aplicativos

   Quando você implementa o Livefyre, o estilo de implementação depende do caso de uso. Para [mais em cada tipo de implementação](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Integração de autenticação

   Você deve integrar seu sistema de gerenciamento de usuários existente ao Livefyre para aplicativos de conversação e outros aplicativos que exigem autenticação de usuário final em seu site. Se você não usar atualmente uma ferramenta de gerenciamento de usuários, poderá usar o Livefyre Identity. Para [obter mais informações sobre a identidade do Livefyre, o que é e como configurá-la](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Personalização

   A personalização é opcional, mas a maioria dos clientes personaliza os aplicativos para se ajustar à sua marca.

