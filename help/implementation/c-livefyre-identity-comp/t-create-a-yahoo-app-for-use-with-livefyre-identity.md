---
description: Você pode usar a identidade do Livefyre com o Yahoo! para permitir que os usuários usem o Yahoo! logons para interagir com aplicativos do site.
title: Crie um Yahoo! Aplicativo para uso com a identidade do Livefyre
exl-id: 6b4c6ea9-1cb0-4496-aabe-70811f464a3d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Crie um Yahoo! Aplicativo para uso com Livefyre Identity{#create-a-yahoo-app-for-use-with-livefyre-identity}

Você pode usar a identidade do Livefyre com o Yahoo! para permitir que os usuários usem o Yahoo! logons para interagir com aplicativos do site.

Para permitir que os usuários façam logon com as credenciais do Yahoo, o Livefyre exige as seguintes informações do aplicativo do Yahoo:

* ID do cliente (chave do consumidor)
* Segredo do cliente (Segredo do consumidor)

Para criar um Yahoo! aplicativo para uso com a Livefyre Identity:

1. Vá para [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/) e faça logon no Yahoo! para criar um novo aplicativo ou selecionar um existente para usar com o Livefyre Identity.
1. Selecionar **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. Selecione **[!UICONTROL API Permissions: Profiles (Social Directory)]** e **[!UICONTROL Read Public]**.

   Quando concluída, a página de detalhes do aplicativo do Yahoo listará a ID do cliente (Chave do consumidor) e o Segredo do cliente (Segredo do consumidor) do aplicativo para uso na página Configurações de integração do Studio.

   >[!NOTE]
   >
   >Se você ativar o Yahoo! fazer logon sem criar o Yahoo! e, se você deixar os campos Client ID e Client Secret no Studio em branco, o Livefyre usará o OpenID para registrar esses usuários nos aplicativos Livefyre. O OAuth e a marca personalizada não estarão disponíveis neste caso.
