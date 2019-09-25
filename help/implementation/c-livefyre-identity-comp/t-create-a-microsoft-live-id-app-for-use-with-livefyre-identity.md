---
description: Você pode usar o Livefyre Identity com o Microsoft Live Identity para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.
seo-description: Você pode usar o Livefyre Identity com o Microsoft Live Identity para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.
seo-title: Criar um aplicativo Microsoft Live Identity para uso com a Livefyre Identity
solution: Experience Manager
title: Criar um aplicativo Microsoft Live Identity para uso com a Livefyre Identity
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar um aplicativo Microsoft Live Identity para uso com a Livefyre Identity{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Você pode usar o Livefyre Identity com o Microsoft Live Identity para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.

Para permitir que os usuários façam logon com suas credenciais do Microsoft Live Identity, o Livefyre exige as seguintes Informações de identidade do Microsoft Live:

* ID do cliente (chave privada)
* Segredo do cliente (senha)

Para criar um aplicativo do Microsoft Live Identity para usar com a Livefyre Identity:

1. Criar ou iniciar sessão numa conta Microsoft Live em [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Crie um novo aplicativo ou selecione um aplicativo existente para usar com a Livefyre Identity.
1. Clique em **[!UICONTROL Add Platform]** e selecione Web como o tipo de plataforma.
1. Verifique se a **[!UICONTROL Allow Implicit Flow]** opção está marcada e insira o URL de redirecionamento, usando seu nome de rede em vez de {nome-rede}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Gere um novo par de senhas/chaves para obter a Chave privada.
1. Em **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, alterne a **[!UICONTROL Enable Microsoft Live Login]** alternância para **[!UICONTROL On]**.
1. Digite o Microsoft Live Client ID e o Microsoft Live Client Secret.
1. Clique em **[!UICONTROL Save Settings]**.

Quando concluída, a página de detalhes do aplicativo do Microsoft Live Identity listará a ID do cliente (chave do consumidor) e o segredo do cliente (segredo do consumidor) do aplicativo para uso na página Configurações de integração do Studio.
