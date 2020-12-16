---
description: Você pode usar o Livefyre Identity com o Twitter para permitir que os usuários usem seus logons do Twitter para interagir com os aplicativos do site.
seo-description: Você pode usar o Livefyre Identity com o Twitter para permitir que os usuários usem seus logons do Twitter para interagir com os aplicativos do site.
seo-title: Criar um aplicativo do Twitter para uso com a Livefyre Identity
solution: Experience Manager
title: Criar um aplicativo do Twitter para uso com a Livefyre Identity
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Criar um aplicativo do Twitter para uso com a Livefyre Identity{#create-a-twitter-app-for-use-with-livefyre-identity}

Você pode usar o Livefyre Identity com o Twitter para permitir que os usuários usem seus logons do Twitter para interagir com os aplicativos do site.

Para habilitar o logon do Twitter, o Livefyre requer as seguintes informações do aplicativo do Twitter:

* consumer key (chave da API)
* consumer secret (segredo da API)

Para criar um aplicativo do Twitter para uso com a Livefyre Identity:

1. Acesse [https://apps.twitter.com/](https://apps.twitter.com/) e entre em sua conta do Twitter para criar um novo aplicativo ou selecionar um aplicativo existente para uso com a Livefyre Identity.
1. Na página Configurações do aplicativo:

   * Digite **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (onde **{networkName}** é o nome de rede fornecido pelo Livefyre. Por exemplo:** [!UICONTROL labs]** em **[!UICONTROL `labs.fyre.co`]**.)
   * Desmarque **[!UICONTROL Enable Callback Locking]**.
   * Selecionar **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Na guia **[!UICONTROL Permissions]**, selecione **[!UICONTROL Access: Read only]**.

Quando concluída, a página Gerenciamento de aplicativos do Twitter > Chaves e Tokens de acesso lista o Consumer key (chave da API) e o Consumer secret (segredo da API) do aplicativo para uso na página Configurações de integração do Studio.
