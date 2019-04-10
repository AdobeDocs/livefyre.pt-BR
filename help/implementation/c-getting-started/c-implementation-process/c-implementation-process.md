---
description: O que esperar na implementação do Livefyre Studio.
seo-description: O que esperar na implementação do Livefyre Studio.
seo-title: Processo de implementação
solution: Experience Manager
title: Processo de implementação
uuid: 9 a 0 f 394 e -3467-47 d 1-9816-45 e 2130 db 440
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Processo de implementação{#implementation-process}

O tempo de implantação do Livefyre depende da implementação e do escopo do trabalho.

## Visão geral da arquitetura de rede do Livefyre {#section_dgj_l32_rbb}

O Livefyre usa os seguintes termos na discussão da arquitetura de rede:

* Rede. O domínio mais alto em que você planeja usar o Livefyre.
* Sites. Um subdomínio ou seção do site que faz parte da rede.
* Aplicativos. Uma renderização de conteúdo em seu site. O conteúdo é exibido visualmente em Aplicativos, usando Aplicativos de visualização (Mosaico, Carrossel, Cartão de recursos etc.) ou em formato de texto, usando Aplicativos de conversa (Comentários, Revisões, Bate-papo etc.). Você pode colocar um ou mais aplicativos em seus sites.
* Fluxos. Os fluxos são filtros que pesquisam mídia social e outros sites para reunir conteúdo automaticamente para moderação ou publicação direta em um aplicativo.
* Conteúdo (por exemplo, UGC, comentários). O que é exibido nos aplicativos. O conteúdo pode ser visual (por exemplo, uma foto ou vídeo), apenas áudio ou texto.

O diagrama a seguir mostra a relação entre Rede, Sites, Aplicativos e Conteúdo.

![](assets/network_site_architecture.png)

Você tem sua própria instância do Livefyre, que é o painel central para moderar o conteúdo, gerenciar usuários e muito mais. Entre em contato com o CSM para obter acesso à sua instância do Livefyre.

## Etapas de integração {#section_s2j_d2x_tz}

Há três etapas principais para integrar o Livefyre:

* Integração do aplicativo

   Quando você implementa o Livefyre, o estilo da implementação depende do caso de uso. Para [mais informações sobre cada tipo de implementação](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Integração de autenticação

   Você deve integrar seu sistema de gerenciamento de usuário existente com o Livefyre for conversation Apps e qualquer outro aplicativo que exija autenticação de usuário final no site. Se você não usar atualmente uma ferramenta de gerenciamento de usuários, poderá usar a identidade do Livefyre. Para [obter mais informações sobre a identidade do Livefyre, ela é e como configurá-la](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Personalização

   A personalização é opcional, mas a maioria dos clientes personaliza os aplicativos para ajustá-los à sua marca.

