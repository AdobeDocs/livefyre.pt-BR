---
description: Você pode usar o Livefyre Identity com o Twitter para permitir que os usuários usem seus logons do Twitter para interagir com os aplicativos do site.
title: Criar um aplicativo do Twitter para uso com a identidade do Livefyre
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Criar um aplicativo do Twitter para uso com a identidade do Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Você pode usar o Livefyre Identity com o Twitter para permitir que os usuários usem seus logons do Twitter para interagir com os aplicativos do site.

Para ativar o logon do Twitter, o Livefyre requer as seguintes informações do aplicativo Twitter:

* Chave do consumidor (chave da API)
* Segredo do consumidor (Segredo da API)

Para criar um aplicativo Twitter para uso com a identidade do Livefyre:

1. Acesse [https://apps.twitter.com/](https://apps.twitter.com/) e faça logon em sua conta Twitter para criar um novo ou selecionar um aplicativo existente para ser usado com o Livefyre Identity.
1. Na página Configurações do aplicativo:

   * Insira **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (onde **{networkName}** é o nome de rede fornecido pelo Livefyre. Por exemplo:** [!UICONTROL labs]** em **[!UICONTROL `labs.fyre.co`]**.)
   * Desmarque **[!UICONTROL Enable Callback Locking]**.
   * Selecionar **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Na guia **[!UICONTROL Permissions]**, selecione **[!UICONTROL Access: Read only]**.

Quando concluída, a página Gerenciamento de aplicativos > Chaves e tokens de acesso da Twitter listará a Chave do consumidor (Chave da API) e o Segredo do consumidor (Segredo da API) do aplicativo para uso na página Configurações de integração do Studio.
