---
description: Descreve opções para adicionar autenticação de usuário aos aplicativos
  do Livefyre, incluindo Janelas de Janelas ou seu próprio serviço de identidade.
seo-description: Descreve opções para adicionar autenticação de usuário aos aplicativos
  do Livefyre, incluindo Janelas de Janelas ou seu próprio serviço de identidade.
seo-title: Integração de identidade
solution: Experience Manager
title: Integração de identidade
uuid: 079 dc 9 c 7-656 a -49 d 0-920 d -9 e 5 a 421 a 319 c
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Integração de identidade{#identity-integration}

Descreve opções para adicionar autenticação de usuário aos aplicativos do Livefyre, incluindo Janelas de Janelas ou seu próprio serviço de identidade.

## Integração de identidade {#t_about_identity_integration}

Descreve opções para adicionar autenticação de usuário aos aplicativos do Livefyre, incluindo Janelas de Janelas ou seu próprio serviço de identidade.

Os aplicativos do Livefyre incluem uma função interativa avançada, como postar um comentário, redigir uma revisão ou curtir conteúdo. Para que os usuários interajam com os Aplicativos do Livefyre, será necessário integrar o Livefyre com um serviço de identidade usando o Auth. js do Livefyre.

O Auth do Livefyre. js fornece autenticação centralizada para todos os aplicativos do Livefyre em todo o seu site e o dá a cobrança exatamente como os usuários devem fazer logon e registrar-se. Adicione Auth globalmente para o modelo do site e use-o em todas as páginas, ou adicione-o uma vez por página e, quando os usuários assinarem no Livefyre JS Auth, transmitirão automaticamente as informações do usuário a todos os aplicativos na página.

Se você criou um serviço de identidade personalizado ou está usando um serviço de identidade de terceiros como o Janrain Capture, esta seção aborda tudo o que você precisa para saber como integrar.
