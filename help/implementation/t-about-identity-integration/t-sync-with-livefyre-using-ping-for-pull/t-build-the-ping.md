---
description: Crie o ping para que sua página emita Livefyre quando os usuários atualizarem seu perfil.
title: Criar o ping
exl-id: 626c200b-eaff-483f-b1eb-7d8993fe5e7c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Criar o Ping{#build-the-ping}

Crie o ping para que sua página emita Livefyre quando os usuários atualizarem seu perfil.

Quando o Livefyre recebe uma notificação de atualização com os `networkName` e `user_id`, o sistema enviará uma solicitação de pull ao seu Ping para URL de pull.

>[!NOTE]
>
>403/Não autorizado em resposta ao seu Ping indica um `lftoken` inválido anexado à solicitação do Ping. Certifique-se de que `lftoken` seja para `user_id` com privilégios de proprietário de rede ou o usuário do sistema. Se você estiver usando bibliotecas do Livefyre, use o método `buildLivefyreToken` para gerar um token de sistema válido para a solicitação.

1. Adicione código à página que consulta o Livefyre quando os usuários atualizam o perfil. Construa o URL da seguinte maneira:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Seu Livefyre forneceu o nome da rede.
   * **[!UICONTROL user_id:]** A ID do seu usuário.
   * **[!UICONTROL token:]** Token de sistema válido.

1. Puxe a estrutura da solicitação.
