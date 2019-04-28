---
description: Notas de versão da versão de March 3 de março de 23 18.
seo-description: Notas de versão da versão de March 3 de março de 23 18.
seo-title: 23 de março de 2018
solution: Experience Manager
title: 23 de março de 2018
uuid: b 69 b 8715-ace 4-48 e 0-8 f 54-ce 4 e 12170 ef 3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 3 de março de 23 18{#march}

Notas de versão da versão de March 3 de março de 23 18.

## Novos recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* **Novo na produção:** O Facebook criou uma atualização de segurança para logon do Facebook que fará com que o login do Facebook de um cliente não funcione corretamente. Para corrigir esse problema, você deve:

   1. Adicione o seguinte URL ao **[!UICONTROL Valid OAuth redirect URIs]** campo nas Configurações do cliente oauth. Substitua `<networkname>` pelo nome correto da rede:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Alternar **[!UICONTROL Use Strict Mode for Redirect URI]****[!UICONTROL Yes]** para.

* **Novo no UAT:** Agora é possível escolher o limite de confiança para tags inteligentes em fluxos. Definir a pontuação de precisão (0-100) para tags permite controlar a precisão dos ativos que estamos recuperando.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de edição** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Media Wall | Correção de um problema no Media Wall em que tags não eram clicadas quando uma postagem do Instagram era adicionada a partir de uma regra de fluxo. |
| Bug | Modq | Correção de um problema que fazia com que o modq não fosse carregado corretamente. |
| Bug | Modq | Correção de um problema em que incorporar áudio fazia com que o modq parasse de funcionar. |

## Versão do UAT

| **Tipo de edição** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Película fotográfica | Correção de alguns problemas para tornar a Película fotográfica mais acessível. |
| Aprimoramento | Studio | Agora é possível fazer logon no Livefyre usando um logon IMS. |

