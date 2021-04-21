---
description: Notas de versão para 23 de março de 2018.
title: 23 de março de 2018
exl-id: 85fd6f79-7fa8-425e-b4c7-2e1635d6ef17
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 7%

---

# 23 de março de 2018{#march}

Notas de versão para 23 de março de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* **Novo em produção:** a Facebook criou uma atualização de segurança para o logon do Facebook que resultará no funcionamento incorreto do logon do Facebook de um cliente. Para corrigir esse problema, você deve:

   1. Adicione o seguinte URL ao campo **[!UICONTROL Valid OAuth redirect URIs]** nas Configurações do OAuth do cliente. Substitua `<networkname>` pelo nome de rede correto:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Alterne **[!UICONTROL Use Strict Mode for Redirect URI]** para **[!UICONTROL Yes]**.

* **Novo no UAT:** agora é possível escolher o limite de confiança para tags inteligentes em fluxos. Definir a pontuação de precisão (0-100) para tags permite controlar a precisão dos ativos que estamos recuperando.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Mural de mídia | Correção de um problema no Mural de mídia em que as tags não eram clicáveis quando uma publicação do Instagram era adicionada de uma regra de fluxo. |
| Bug | ModQ | Correção de um problema em que o ModQ não era carregado corretamente. |
| Bug | ModQ | Correção de um problema em que a incorporação de áudio fazia com que o ModQ parasse de funcionar. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Tira | Correção de alguns problemas para tornar a Filmstrip mais acessível. |
| Aprimoramento | Studio | Agora você pode fazer logon no Livefyre usando um logon IMS. |
