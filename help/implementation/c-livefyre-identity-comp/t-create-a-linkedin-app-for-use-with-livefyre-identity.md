---
description: Você pode usar o Livefyre Identity com o LinkedIn para permitir que os usuários usem seus logons do LinkedIn para interagir com os aplicativos do site.
seo-description: Você pode usar o Livefyre Identity com o LinkedIn para permitir que os usuários usem seus logons do LinkedIn para interagir com os aplicativos do site.
seo-title: Criar um aplicativo do LinkedIn para uso com a Livefyre Identity
solution: Experience Manager
title: Criar um aplicativo do LinkedIn para uso com a Livefyre Identity
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar um aplicativo do LinkedIn para uso com a Livefyre Identity{#create-a-linkedin-app-for-use-with-livefyre-identity}

Você pode usar o Livefyre Identity com o LinkedIn para permitir que os usuários usem seus logons do LinkedIn para interagir com os aplicativos do site.

Para ativar o logon do LinkedIn, o Livefyre requer as seguintes informações do aplicativo do LinkedIn:

* Chave do consumidor (chave da API)
* Segredo do consumidor (segredo da API)

Para criar um aplicativo do LinkedIn para uso com a Livefyre Identity:

1. Acesse https://www.linkedin.com/secure/developer e entre em sua conta do LinkedIn para criar um novo aplicativo ou selecionar um aplicativo existente para uso com o Livefyre Identity.
1. Clique em **[!UICONTROL Create Application]**.
1. Preencha o formulário para criar o aplicativo.
1. No **[!UICONTROL Default Application Permissions]**, ative as permissões **[!UICONTROL r_basicprofile]** e **[!UICONTROL r_emailaddress]** do aplicativo.
1. Insira o **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** como `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Salve o aplicativo.
1. Em **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, alterne a **[!UICONTROL Enable LinkedIn Login]** alternância para **[!UICONTROL On]**.
1. Insira a ID do cliente do LinkedIn e o segredo do cliente do LinkedIn.
1. Clique em **[!UICONTROL Save Settings]**.

Quando concluída, a página de detalhes do aplicativo do LinkedIn listará a chave da API (chave do consumidor) e o segredo da API (segredo do consumidor) do aplicativo para uso na página Configurações de integração do Studio.
