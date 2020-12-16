---
description: Crie o ping para que sua página jogue Livefyre quando os usuários atualizarem seu perfil.
seo-description: Crie o ping para que sua página jogue Livefyre quando os usuários atualizarem seu perfil.
seo-title: Criar o ping
solution: Experience Manager
title: Criar o ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Crie o Ping{#build-the-ping}

Crie o ping para que sua página jogue Livefyre quando os usuários atualizarem seu perfil.

Quando o Livefyre receber uma notificação de atualização com as `networkName` e `user_id`, o sistema enviará uma solicitação de Puxo para seu URL de Ping for Pull.

>[!NOTE]
>
>403/Não autorizado em resposta ao seu Ping indica um `lftoken` inválido anexado à solicitação de Ping. Certifique-se de que `lftoken` seja para um `user_id` com privilégios de proprietário de rede ou para o usuário do sistema. Se você estiver usando bibliotecas Livefyre, use o método `buildLivefyreToken` para gerar um token de sistema válido para a solicitação.

1. Adicione o código à sua página que aciona o Livefyre quando os usuários atualizarem seu perfil. Construa o URL desta forma:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Seu Livefyre forneceu o nome da rede.
   * **[!UICONTROL user_id:]** A ID do usuário.
   * **[!UICONTROL token:]** Token de sistema válido.

1. Puxe a estrutura de solicitação.
