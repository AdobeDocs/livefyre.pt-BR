---
description: Você pode usar o Livefyre Identity com o LinkedIn para permitir que os usuários usem seus logons do LinkedIn para interagir com os aplicativos do site.
title: Criar um aplicativo do LinkedIn para uso com a identidade do Livefyre
exl-id: e77eca6a-1698-414e-994e-1189f780ada1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# Criar um aplicativo do LinkedIn para uso com a identidade do Livefyre{#create-a-linkedin-app-for-use-with-livefyre-identity}

Você pode usar o Livefyre Identity com o LinkedIn para permitir que os usuários usem seus logons do LinkedIn para interagir com os aplicativos do site.

Para ativar o logon do LinkedIn, o Livefyre requer as seguintes informações do aplicativo LinkedIn:

* Chave do consumidor (chave da API)
* Segredo do consumidor (Segredo da API)

Para criar um aplicativo LinkedIn para uso com a identidade do Livefyre:

1. Acesse https://www.linkedin.com/secure/developer e faça logon em sua conta LinkedIn para criar um novo ou selecione um aplicativo existente para uso com a Livefyre Identity.
1. Clique em **[!UICONTROL Create Application]**.
1. Preencha o formulário para criar o Aplicativo.
1. No **[!UICONTROL Default Application Permissions]**, ative as permissões do aplicativo **[!UICONTROL r_basicprofile]** e **[!UICONTROL r_emailaddress]**.
1. Insira o **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** como `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Salve o aplicativo.
1. Em **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, alterne o botão **[!UICONTROL Enable LinkedIn Login]** para **[!UICONTROL On]**.
1. Insira a LinkedIn Client ID e o LinkedIn Client Secret.
1. Clique em **[!UICONTROL Save Settings]**.

Quando concluída, a página de detalhes do aplicativo da LinkedIn listará a Chave da API (Chave do consumidor) e o Segredo da API (Segredo do consumidor) do aplicativo para uso na página Configurações de integração do Studio.
