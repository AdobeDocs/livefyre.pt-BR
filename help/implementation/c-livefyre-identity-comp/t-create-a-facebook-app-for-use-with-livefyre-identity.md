---
description: Você pode usar o Livefyre Identity com o Facebook para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.
seo-description: Você pode usar o Livefyre Identity com o Facebook para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.
seo-title: Criar um aplicativo do Facebook para uso com a Livefyre Identity
solution: Experience Manager
title: Criar um aplicativo do Facebook para uso com a Livefyre Identity
uuid: a7f7be4e-8986-4e79-831a-0bb0ae555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Criar um aplicativo do Facebook para uso com a Livefyre Identity{#create-a-facebook-app-for-use-with-livefyre-identity}

Você pode usar o Livefyre Identity com o Facebook para permitir que os usuários usem seus logons do Facebook para interagir com os aplicativos do site.

Para permitir que seus usuários façam logon com suas credenciais do Facebook, o Livefyre requer as seguintes informações do aplicativo do Facebook:

* ID do aplicativo
* Segredo do aplicativo

Para criar um aplicativo do Facebook para uso com a Livefyre Identity:

1. Vá para [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Faça logon em sua conta de desenvolvedor do Facebook.
1. Clique em **[!UICONTROL Add New App]** ou selecione um aplicativo existente para uso com a Livefyre Identity.
1. Clique em **[!UICONTROL Settings]** e em **[!UICONTROL Basic]**. Insira um **[!UICONTROL Contact Email]** endereço, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** e **[!UICONTROL Terms of Service URL]**.
1. Clique no sinal de mais ( **[!UICONTROL +]**) ao lado de **[!UICONTROL Products]**.
1. Clique em **[!UICONTROL Set Up]** em **[!UICONTROL Facebook Login]**.
1. Clique em **[!UICONTROL Settings]** e configure o seguinte:

   * Defina **[!UICONTROL Client OAuth Login]** como **[!UICONTROL Yes]**.
   * Defina **[!UICONTROL Web OAuth Login]** como **[!UICONTROL Yes]**.
   * Defina **[!UICONTROL Use Strict Mode for Redirect URIs]** como **[!UICONTROL Yes]**.
   * Defina **[!UICONTROL Enforce HTTPS for Web OAuth Login]** como **[!UICONTROL Yes]**.
   * Em **[!UICONTROL Valid OAuth redirect URLs]**, adicione o URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (onde `{networkName}` é o nome de rede fornecido pelo Livefyre).

1. Em **[!UICONTROL App Review]**:

   * Torne o aplicativo público.
   * Certifique-se de que **[!UICONTROL Approved Items]** para **[!UICONTROL Login Permissions]** inclua `email`, `public_profile` e `user_friends`.

Quando concluída, a página de Painel do desenvolvedor do Facebook lista sua ID do aplicativo e o segredo do aplicativo para uso nas Configurações de integração do Studio.
