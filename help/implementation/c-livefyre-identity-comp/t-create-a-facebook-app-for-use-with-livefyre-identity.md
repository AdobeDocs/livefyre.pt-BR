---
description: Você pode usar o Livefyre Identity com o Facebook para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.
title: Criar um aplicativo do Facebook para uso com a identidade do Livefyre
exl-id: ec320865-6ea3-4f6f-a5f6-31f3d5cbdc93
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---

# Criar um aplicativo do Facebook para uso com a identidade do Livefyre{#create-a-facebook-app-for-use-with-livefyre-identity}

Você pode usar o Livefyre Identity com o Facebook para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.

Para permitir que os usuários façam logon com as credenciais do Facebook, o Livefyre exige as seguintes informações do aplicativo Facebook:

* ID do aplicativo
* Segredo do aplicativo

Para criar um aplicativo Facebook para uso com a Livefyre Identity:

1. Vá para [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Faça logon em sua conta de desenvolvedor do Facebook.
1. Clique em **[!UICONTROL Add New App]** ou selecione um aplicativo existente para usar com a Identidade do Livefyre.
1. Clique em **[!UICONTROL Settings]** e em **[!UICONTROL Basic]**. Insira um endereço **[!UICONTROL Contact Email]**, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** e **[!UICONTROL Terms of Service URL]**.
1. Clique no sinal de mais ( **[!UICONTROL +]**) ao lado de **[!UICONTROL Products]**.
1. Clique em **[!UICONTROL Set Up]** em **[!UICONTROL Facebook Login]**.
1. Clique em **[!UICONTROL Settings]** e configure o seguinte:

   * Defina **[!UICONTROL Client OAuth Login]** para **[!UICONTROL Yes]**.
   * Defina **[!UICONTROL Web OAuth Login]** para **[!UICONTROL Yes]**.
   * Defina **[!UICONTROL Use Strict Mode for Redirect URIs]** para **[!UICONTROL Yes]**.
   * Defina **[!UICONTROL Enforce HTTPS for Web OAuth Login]** para **[!UICONTROL Yes]**.
   * Em **[!UICONTROL Valid OAuth redirect URLs]**, adicione o URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (onde `{networkName}` é o nome de rede fornecido pelo Livefyre).

1. Em **[!UICONTROL App Review]**:

   * Tornar o aplicativo público.
   * Certifique-se de que **[!UICONTROL Approved Items]** para **[!UICONTROL Login Permissions]** inclua `email`, `public_profile` e `user_friends`.

Quando concluída, a página Painel do desenvolvedor do Facebook listará sua ID do aplicativo e o Segredo do aplicativo para uso nas Configurações de integração do Studio.
