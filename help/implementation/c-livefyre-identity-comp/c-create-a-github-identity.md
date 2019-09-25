---
description: Você pode usar a Identidade do Livefyre com a Identidade do GitHub para permitir que os usuários usem seus logons do GitHub para interagir com os aplicativos do site.
seo-description: Você pode usar a Identidade do Livefyre com a Identidade do GitHub para permitir que os usuários usem seus logons do GitHub para interagir com os aplicativos do site.
seo-title: Criar um aplicativo de identidade GitHub para uso com a identidade do Livefyre
title: Criar um aplicativo de identidade GitHub para uso com a identidade do Livefyre
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar um aplicativo de identidade GitHub para uso com a identidade do Livefyre{#create-a-github-identity-app-for-use-with-livefyre-identity}

Você pode usar a Identidade do Livefyre com a Identidade do GitHub para permitir que os usuários usem seus logons do GitHub para interagir com os aplicativos do site.

Para permitir que os usuários façam logon com suas credenciais de identidade do GitHub, o Livefyre exige as seguintes informações de identidade do GitHub:

* ID do cliente (chave privada)
* Segredo do cliente (senha)

Para criar um aplicativo de identidade GitHub para uso com a identidade do Livefyre:

1. Crie ou entre em uma conta GitHub em [](https://github.com/settings/developers).
1. Registre um novo aplicativo ou selecione um aplicativo existente para usar com a Livefyre Identity.
1. Insira todas as informações no formulário. Digite o **[!UICONTROL Authorization callback URL]**, usando seu nome de rede em vez de `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. Em **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, alterne a **[!UICONTROL Enable GitHub Login]** alternância para **[!UICONTROL On]**.

1. Insira a ID do cliente GitHub e o segredo do cliente GitHub.
1. Clique em **[!UICONTROL Save Settings]**.

Quando concluída, a página de detalhes do aplicativo da Identidade do GitHub listará a ID do cliente (Chave do consumidor) e o segredo do cliente (Segredo do consumidor) do aplicativo para uso na página Configurações de integração do Studio.
