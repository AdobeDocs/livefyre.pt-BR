---
description: Você pode usar a identidade do Livefyre com Yahoo! para permitir que os usuários usem o Yahoo! logons para interagir com aplicativos em seu site.
seo-description: Você pode usar a identidade do Livefyre com Yahoo! para permitir que os usuários usem o Yahoo! logons para interagir com aplicativos em seu site.
seo-title: Crie um Yahoo! Aplicativo para uso com a identidade do Livefyre
solution: Experience Manager
title: Crie um Yahoo! Aplicativo para uso com a identidade do Livefyre
uuid: 6863 cd 2 e-eb 0 d -465 b-b 706-88 ecaccf 41 bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Crie um Yahoo! Aplicativo para uso com a identidade do Livefyre{#create-a-yahoo-app-for-use-with-livefyre-identity}

Você pode usar a identidade do Livefyre com Yahoo! para permitir que os usuários usem o Yahoo! logons para interagir com aplicativos em seu site.

Para permitir que os usuários façam logon com suas credenciais do Yahoo, o Livefyre exige as seguintes informações do Yahoo App:

* ID do cliente (chave do consumidor)
* Segredo do cliente (segredo do consumidor)

Para criar um Yahoo! aplicativo para uso com a identidade do Livefyre:

1. Acesse [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)e faça logon em seu Yahoo! para criar um novo aplicativo ou selecionar um aplicativo existente para uso com a identidade do Livefyre.
1. Selecione **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. Selecione **[!UICONTROL API Permissions: Profiles (Social Directory)]** e **[!UICONTROL Read Public]**.

   Quando concluir, a página de detalhes do aplicativo do Yahoo listará a ID do cliente do aplicativo (chave do consumidor) e o segredo do cliente (segredo do consumidor) para uso na página Configurações de integração do Studio.

   >[!NOTE]
   >
   >Se você ativar o Yahoo! logon sem criar um Yahoo! aplicativo e, se você deixar os campos ID do cliente e Segredo do cliente em Estúdio em branco, o Livefyre usará openid para registrar esses usuários em seus Aplicativos do Livefyre. O oauth e a marca personalizada não estarão disponíveis nesse caso.