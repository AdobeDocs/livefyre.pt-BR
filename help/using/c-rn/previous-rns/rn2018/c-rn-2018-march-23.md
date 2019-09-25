---
description: Notas de versão para a versão de 23 de março de 2018.
seo-description: Notas de versão para a versão de 23 de março de 2018.
seo-title: 23 de março de 2018
solution: Experience Manager
title: 23 de março de 2018
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 23, 2018{#march}

Notas de versão para a versão de 23 de março de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* **** Novo na produção: O Facebook criou uma atualização de segurança para o logon do Facebook que fará com que o logon do Facebook de um cliente não funcione corretamente. Para corrigir esse problema, é necessário:

   1. Adicione o seguinte URL ao **[!UICONTROL Valid OAuth redirect URIs]** campo nas Configurações OAuth do cliente. Substitua `<networkname>` pelo nome de rede correto:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Mude **[!UICONTROL Use Strict Mode for Redirect URI]** para **[!UICONTROL Yes]**.

* **** Novo na UAT:Agora você pode escolher o limite de confiança para tags inteligentes em fluxos. A definição da pontuação de precisão (0-100) para tags permite controlar a precisão dos ativos que estamos recuperando.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Mídia | Correção de um problema no Media Wall em que as tags não eram clicáveis quando uma postagem do Instagram era adicionada de uma regra de fluxo. |
| Bug | ModQ | Correção de um problema no qual o ModQ não era carregado corretamente. |
| Bug | ModQ | Corrigido um problema no qual a incorporação de áudio fazia com que o ModQ parasse de funcionar. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Película fotográfica | Correção de alguns problemas para tornar a Película fotográfica mais acessível. |
| Aprimoramento | Studio | Agora você pode fazer logon no Livefyre usando um logon IMS. |

