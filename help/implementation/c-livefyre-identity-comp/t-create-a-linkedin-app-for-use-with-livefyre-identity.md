---
description: Você pode usar a identidade do Livefyre com o linkedin para permitir
  que os usuários usem seus logons do linkedin para interagir com Aplicativos no seu
  site.
seo-description: Você pode usar a identidade do Livefyre com o linkedin para permitir
  que os usuários usem seus logons do linkedin para interagir com Aplicativos no seu
  site.
seo-title: Criar um aplicativo do linkedin para uso com a identidade do Livefyre
solution: Experience Manager
title: Criar um aplicativo do linkedin para uso com a identidade do Livefyre
uuid: c 5112 f 24-a 4 e 0-4526-afe 8-b 8 f 27 a 3 b 2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar um aplicativo do linkedin para uso com a identidade do Livefyre{#create-a-linkedin-app-for-use-with-livefyre-identity}

Você pode usar a identidade do Livefyre com o linkedin para permitir que os usuários usem seus logons do linkedin para interagir com Aplicativos no seu site.

Para ativar o logon do linkedin, o Livefyre exige as seguintes informações do aplicativo do linkedin:

* Chave do consumidor (chave de API)
* Segredo do consumidor (segredo da API)

Para criar um aplicativo do linkedin para uso com a identidade do Livefyre:

1. Acesse https://www.linkedin.com/secure/developer e faça logon na conta do linkedin para criar um novo aplicativo ou selecione um aplicativo existente para usar com a identidade do Livefyre.
1. Clique **[!UICONTROL Create Application]**em.
1. Preencha o formulário para criar o Aplicativo.
1. No **[!UICONTROL Default Application Permissions]**, ative as permissões **[!UICONTROL r_basicprofile]** e **[!UICONTROL r_emailaddress]** o aplicativo.
1. Insira o **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** como `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Salve o aplicativo.
1. Em **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**, altere a **[!UICONTROL Enable LinkedIn Login]** alternância para **[!UICONTROL On]**.
1. Insira a ID do cliente do linkedin e o segredo do cliente do linkedin.
1. Clique **[!UICONTROL Save Settings]**em.

Ao concluir, a página de detalhes do aplicativo do linkedin listará a chave de API do aplicativo (chave do consumidor) e o segredo da API (segredo do consumidor) para uso na página Configurações de integração do Studio.
