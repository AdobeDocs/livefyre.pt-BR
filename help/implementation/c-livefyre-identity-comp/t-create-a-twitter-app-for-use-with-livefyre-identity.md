---
description: Você pode usar a identidade do Livefyre com o Twitter para permitir que
  os usuários usem seus logons do Twitter para interagir com Aplicativos no seu site.
seo-description: Você pode usar a identidade do Livefyre com o Twitter para permitir
  que os usuários usem seus logons do Twitter para interagir com Aplicativos no seu
  site.
seo-title: Criar um aplicativo do Twitter para usar com a identidade do Livefyre
solution: Experience Manager
title: Criar um aplicativo do Twitter para usar com a identidade do Livefyre
uuid: 841 cce 7 c -618 d -4154-85 a 3-1 de 96 d 04 bb 69
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Criar um aplicativo do Twitter para usar com a identidade do Livefyre{#create-a-twitter-app-for-use-with-livefyre-identity}

Você pode usar a identidade do Livefyre com o Twitter para permitir que os usuários usem seus logons do Twitter para interagir com Aplicativos no seu site.

Para habilitar o logon do Twitter, o Livefyre exige as seguintes informações do aplicativo do Twitter:

* Chave do consumidor (chave de API)
* Segredo do consumidor (segredo da API)

Para criar um aplicativo do Twitter para uso com a identidade do Livefyre:

1. Acesse [https://apps.twitter.com/](https://apps.twitter.com/)e faça logon em sua conta do Twitter para criar um novo aplicativo ou selecione um aplicativo existente para usar com a identidade do Livefyre.
1. Na página Configurações do aplicativo:

   * Enter **[!UICONTROL Callback URL:]**`https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (onde **{networkname}** é o nome da rede fornecida pelo Livefyre. Por exemplo: ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deselect **[!UICONTROL Enable Callback Locking]**.
   * Selecione **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Na **[!UICONTROL Permissions]** guia, selecione **[!UICONTROL Access: Read only]**.

Quando concluída, a página Gerenciamento de aplicativos do Twitter > Teclas e acessos de acesso listará a Chave de consumidor do aplicativo (Chave de API) e Segredo do consumidor (segredo API) para uso na página Configurações de integração do Studio.
