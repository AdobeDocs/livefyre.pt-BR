---
description: Você pode usar a Livefyre Identity com o Yahoo! para permitir que os usuários usem seu Yahoo! faça logon para interagir com os aplicativos do site.
seo-description: Você pode usar a Livefyre Identity com o Yahoo! para permitir que os usuários usem seu Yahoo! faça logon para interagir com os aplicativos do site.
seo-title: Crie um Yahoo! Aplicativo para uso com Livefyre Identity
solution: Experience Manager
title: Crie um Yahoo! Aplicativo para uso com Livefyre Identity
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Crie um Yahoo! Aplicativo para uso com Livefyre Identity{#create-a-yahoo-app-for-use-with-livefyre-identity}

Você pode usar a Livefyre Identity com o Yahoo! para permitir que os usuários usem seu Yahoo! faça logon para interagir com os aplicativos do site.

Para permitir que os usuários façam logon com suas credenciais do Yahoo, o Livefyre requer as seguintes informações do aplicativo do Yahoo:

* ID do cliente (Consumer key)
* Segredo do cliente (Consumer secret)

Para criar um Yahoo! aplicativo para uso com a Livefyre Identity:

1. Vá para [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/) e entre em seu Yahoo! para criar um novo aplicativo ou selecionar um aplicativo existente para uso com a Livefyre Identity.
1. Selecionar **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. Selecione **[!UICONTROL API Permissions: Profiles (Social Directory)]** e **[!UICONTROL Read Public]**.

   Quando concluída, a página de detalhes do aplicativo do Yahoo será lista na ID do cliente (Consumer key) e no segredo do cliente (Consumer secret) do aplicativo para uso na página Configurações de integração do Studio.

   >[!NOTE]
   >
   >Se você ativar o Yahoo! faça logon sem criar um Yahoo! e se você deixar os campos ID do cliente e Segredo do cliente no Studio em branco, o Livefyre usará o OpenID para registrar esses usuários nos aplicativos Livefyre. Neste caso, o OAuth e a marca personalizada não estarão disponíveis.