---
description: Crie o ping para que sua página jogue Livefyre quando os usuários atualizarem seu perfil.
seo-description: Crie o ping para que sua página jogue Livefyre quando os usuários atualizarem seu perfil.
seo-title: Criar o ping
solution: Experience Manager
title: Criar o ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516

---


# Criar o ping{#build-the-ping}

Crie o ping para que sua página jogue Livefyre quando os usuários atualizarem seu perfil.

Quando o Livefyre receber uma notificação de atualização com o e `networkName` , `user_id`, o sistema enviará uma solicitação de Puxo para seu Ping for Pull URL.

>[!NOTE]
>
>403/Não autorizado em resposta ao seu Ping indica um valor inválido `lftoken` anexado à solicitação de Ping. Certifique-se de que o `lftoken` é para um usuário com privilégios de proprietário de rede `user_id` ou o usuário do sistema. Se você estiver usando bibliotecas Livefyre, use o `buildLivefyreToken` método para gerar um token de sistema válido para a solicitação.

1. Adicione o código à sua página que aciona o Livefyre quando os usuários atualizarem seu perfil. Construa o URL desta forma:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Seu Livefyre forneceu o nome da rede.
   * **[!UICONTROL user_id:]** A ID do usuário.
   * **[!UICONTROL token:]** Token de sistema válido.

1. Puxe a estrutura de solicitação.
