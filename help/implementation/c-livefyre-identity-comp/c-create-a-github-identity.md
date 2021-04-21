---
description: Você pode usar a identidade do Livefyre com a identidade do GitHub para permitir que os usuários usem seus logons do GitHub para interagir com os aplicativos do site.
title: Criar um aplicativo de identidade do GitHub para uso com a identidade do Livefyre
exl-id: f25ffd0e-ea4f-42ac-abfc-c02018421b85
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---

# Crie um aplicativo de identidade do GitHub para uso com o Livefyre Identity{#create-a-github-identity-app-for-use-with-livefyre-identity}

Você pode usar a identidade do Livefyre com a identidade do GitHub para permitir que os usuários usem seus logons do GitHub para interagir com os aplicativos do site.

Para permitir que os usuários façam logon com suas credenciais de identidade do GitHub, o Livefyre exige as seguintes informações de identidade do GitHub:

* ID do cliente (chave privada)
* Segredo do cliente (Senha)

Para criar um aplicativo de identidade do GitHub para usar com a identidade do Livefyre:

1. Crie ou faça logon em uma conta GitHub em [](https://github.com/settings/developers).
1. Registre um novo aplicativo ou selecione um existente para usar com o Livefyre Identity.
1. Insira todas as informações no formulário. Insira o **[!UICONTROL Authorization callback URL]**, usando o nome da rede em vez de `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. Em **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, alterne o botão **[!UICONTROL Enable GitHub Login]** para **[!UICONTROL On]**.

1. Insira a ID do cliente GitHub e o Segredo do cliente GitHub.
1. Clique em **[!UICONTROL Save Settings]**.

Quando concluída, a página de detalhes do aplicativo da Identidade do GitHub listará a ID do cliente do aplicativo (Chave do consumidor) e o Segredo do cliente (Segredo do consumidor) para uso na página Configurações de integração do Studio.
