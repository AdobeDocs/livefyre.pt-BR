---
description: Você pode usar a identidade do Livefyre com a identidade github para
  permitir que os usuários usem seus logons github para interagir com Aplicativos
  no seu site.
seo-description: Você pode usar a identidade do Livefyre com a identidade github para
  permitir que os usuários usem seus logons github para interagir com Aplicativos
  no seu site.
seo-title: Criar um aplicativo de identidade github para uso com a identidade do Livefyre
title: Criar um aplicativo de identidade github para uso com a identidade do Livefyre
uuid: cf 56164 c -1521-4 a 42-89 cb -39483764807 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Criar um aplicativo de identidade github para uso com a identidade do Livefyre{#create-a-github-identity-app-for-use-with-livefyre-identity}

Você pode usar a identidade do Livefyre com a identidade github para permitir que os usuários usem seus logons github para interagir com Aplicativos no seu site.

Para permitir que os usuários façam logon com suas credenciais de identidade github, o Livefyre exige as seguintes informações de identidade github:

* ID do cliente (chave privada)
* Segredo do cliente (senha)

Para criar um aplicativo de identidade github para uso com a identidade do Livefyre:

1. Crie ou faça logon em uma conta github em [](https://github.com/settings/developers).
1. Registre um novo aplicativo ou selecione um aplicativo existente para usar com a identidade do Livefyre.
1. Insira todas as informações no formulário. Digite o **[!UICONTROL Authorization callback URL]**nome, usando seu nome de rede em vez `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`de.

1. Em **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**, altere a **[!UICONTROL Enable GitHub Login]** alternância para **[!UICONTROL On]**.

1. Insira a ID do cliente github e o segredo do cliente github.
1. Clique **[!UICONTROL Save Settings]**em.

Ao concluir, a página de detalhes do aplicativo Github Identity listará a ID do cliente do aplicativo (Chave do consumidor) e o segredo do cliente (segredo do consumidor) para uso na página Configurações de integração do Studio.
