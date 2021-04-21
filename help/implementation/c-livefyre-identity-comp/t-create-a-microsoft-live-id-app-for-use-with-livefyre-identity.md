---
description: Você pode usar o Livefyre Identity com o Microsoft Live Identity para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.
title: Criar um aplicativo do Microsoft Live Identity para uso com a identidade do Livefyre
exl-id: 7702c956-ecb5-424a-9866-d6f73d4d4bc9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Crie um aplicativo de identidade do Microsoft Live para uso com o Livefyre Identity{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Você pode usar o Livefyre Identity com o Microsoft Live Identity para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.

Para permitir que os usuários façam logon com suas credenciais do Microsoft Live Identity, o Livefyre requer as seguintes Informações do Microsoft Live Identity:

* ID do cliente (chave privada)
* Segredo do cliente (Senha)

Para criar um aplicativo do Microsoft Live Identity para usar com a Identidade do Livefyre:

1. Crie ou faça logon em uma conta Microsoft Live em [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. Crie um novo aplicativo ou selecione um existente para usar com o Livefyre Identity.
1. Clique em **[!UICONTROL Add Platform]** e selecione Web como tipo de plataforma.
1. Verifique se a opção **[!UICONTROL Allow Implicit Flow]** está marcada e insira o URL de redirecionamento, usando seu nome de rede em vez de {nome-da-rede}: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Gere um novo par de senha/chave para obter a Chave privada.
1. Em **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**, alterne o botão **[!UICONTROL Enable Microsoft Live Login]** para **[!UICONTROL On]**.
1. Insira o Microsoft Live Client ID e o Microsoft Live Client Secret.
1. Clique em **[!UICONTROL Save Settings]**.

Quando concluída, a página de detalhes do aplicativo da Microsoft Live Identity listará a ID do cliente (Chave do consumidor) e o Segredo do cliente (Segredo do consumidor) do aplicativo para uso na página Configurações de integração do Studio.
