---
description: Você pode usar a identidade do Livefyre com o Google para permitir que
  os usuários usem seus logons do Google para interagir com aplicativos no seu site.
seo-description: Você pode usar a identidade do Livefyre com o Google para permitir
  que os usuários usem seus logons do Google para interagir com aplicativos no seu
  site.
seo-title: Criar um projeto do Google para uso com a identidade do Livefyre
solution: Experience Manager
title: Criar um projeto do Google para uso com a identidade do Livefyre
uuid: b 0 a 6 bb 8 a-abea -4 f 5 c -92 ed -026 e 60183 e 1 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar um projeto do Google para uso com a identidade do Livefyre{#create-a-google-project-for-use-with-livefyre-identity}

Você pode usar a identidade do Livefyre com o Google para permitir que os usuários usem seus logons do Google para interagir com aplicativos no seu site.

Para permitir que os usuários façam logon com suas credenciais do Google, o Livefyre exige as seguintes informações do projeto do Google:

* ID do cliente
* Segredo do cliente

Para criar um projeto do Google para uso com a identidade do Livefyre:

1. Acesse [https://console.cloud.google.com/project](https://console.cloud.google.com/project) e faça logon em sua conta do Google para criar um novo aplicativo ou selecione um aplicativo existente para usar com a identidade do Livefyre.
1. No painel do projeto, clique **[!UICONTROL Enable and Manage APIs]**em.
1. Na página Visão geral da API, em apis do Social, clique em para habilitar a API do Google +.
1. Na página Credenciais da API, selecione ID **[!UICONTROL Credentials > New credentials > OAuth]** do cliente. Na **[!UICONTROL Create client ID]** página que é aberta:

   * Selecione Tipo de aplicativo: Aplicativo da Web.
   * Digite um **[!UICONTROL Name]** para o **[!UICONTROL Client ID]**.
   * Deixe **[!UICONTROL Authorized JavaScript origins]** o campo em branco.
   * Inserir **[!UICONTROL Authorized redirect URIs]**: `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/google_fyre` (onde **[!UICONTROL {networkName}]** é o seu nome de rede fornecido pelo Livefyre. Por exemplo: ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Clique **[!UICONTROL Create]** em para salvar suas credenciais.

Ao concluir, a página Gerente de API do Google > Credenciais listará a ID do cliente do projeto e o segredo do cliente para uso na página Configurações de integração do Studio.
