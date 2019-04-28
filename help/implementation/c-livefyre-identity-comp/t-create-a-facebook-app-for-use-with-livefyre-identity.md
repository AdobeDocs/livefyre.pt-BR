---
description: Você pode usar a identidade do Livefyre com o Facebook para permitir que os usuários usem seus logons do Facebook para interagir com Aplicativos no seu site.
seo-description: Você pode usar a identidade do Livefyre com o Facebook para permitir que os usuários usem seus logons do Facebook para interagir com Aplicativos no seu site.
seo-title: Criar um aplicativo do Facebook para usar com a identidade do Livefyre
solution: Experience Manager
title: Criar um aplicativo do Facebook para usar com a identidade do Livefyre
uuid: a 7 f 7 be 4 e -8986-4 e 79-831 a -0 bb 0 ae 555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar um aplicativo do Facebook para usar com a identidade do Livefyre{#create-a-facebook-app-for-use-with-livefyre-identity}

Você pode usar a identidade do Livefyre com o Facebook para permitir que os usuários usem seus logons do Facebook para interagir com Aplicativos no seu site.

Para permitir que os usuários façam logon com suas credenciais do Facebook, o Livefyre exige as seguintes informações do aplicativo do Facebook:

* ID do aplicativo
* Segredo do aplicativo

Para criar um aplicativo do Facebook para uso com a identidade do Livefyre:

1. Acesse [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Faça logon em sua conta de desenvolvedor do Facebook.
1. Clique **[!UICONTROL Add New App]** ou selecione um aplicativo existente para usar com a identidade do Livefyre.
1. Clique **[!UICONTROL Settings]** em, em seguida **[!UICONTROL Basic]**. Insira um **[!UICONTROL Contact Email]** endereço **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** e **[!UICONTROL Terms of Service URL]**.
1. Clique no sinal de mais ( **[!UICONTROL +]**) ao lado **[!UICONTROL Products]**.
1. Clique em **[!UICONTROL Set Up]** abaixo **[!UICONTROL Facebook Login]**.
1. Clique **[!UICONTROL Settings]** em e configure o seguinte:

   * Defina **[!UICONTROL Client OAuth Login]** como **[!UICONTROL Yes]**.
   * Defina **[!UICONTROL Web OAuth Login]** como **[!UICONTROL Yes]**.
   * Defina **[!UICONTROL Use Strict Mode for Redirect URIs]** como **[!UICONTROL Yes]**.
   * Defina **[!UICONTROL Enforce HTTPS for Web OAuth Login]** como **[!UICONTROL Yes]**.
   * Em **[!UICONTROL Valid OAuth redirect URLs]**, adicione o URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (onde `{networkName}` é seu nome de rede fornecido pelo Livefyre).

1. Em **[!UICONTROL App Review]**:

   * Torne o aplicativo público.
   * Verifique se **[!UICONTROL Approved Items]****[!UICONTROL Login Permissions]** a inclusão `email`foi incluída, `public_profile`e `user_friends`.

Ao concluir, a página Painel do desenvolvedor do Facebook lista sua ID do aplicativo e segredo do aplicativo para uso nas Configurações de integração do Studio.
