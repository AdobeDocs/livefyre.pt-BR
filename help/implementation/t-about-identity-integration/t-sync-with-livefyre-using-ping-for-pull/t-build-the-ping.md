---
description: Crie o ping para que sua página armazene o Livefyre quando os usuários
  atualizam o perfil.
seo-description: Crie o ping para que sua página armazene o Livefyre quando os usuários
  atualizam o perfil.
seo-title: Criar o ping
solution: Experience Manager
title: Criar o ping
uuid: cb 8 cc 043-9 ea 5-407 c-b 70 f -3 f 1 e 37 accdae
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Criar o ping{#build-the-ping}

Crie o ping para que sua página armazene o Livefyre quando os usuários atualizam o perfil.

Quando o Livefyre receber uma notificação de atualização com o `networkName` e `user_id`, o sistema enviará uma solicitação extraída para o seu Ping para obter URL de extração.

>[!NOTE]
>
>403/Não autorizado em resposta ao ping indica um anexo inválido `lftoken` à solicitação Ping. Certifique-se de que seja `lftoken` para um `user_id` com privilégios de proprietário de rede ou o usuário do sistema. Se você estiver usando bibliotecas do Livefyre, use o `buildLivefyreToken` método para gerar um token de sistema válido para a solicitação.

1. Adicione código à sua página que pira o Livefyre quando os usuários atualizam o perfil. Construa o URL desta forma:

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** Seu nome de rede fornecido pelo Livefyre.
* **[!UICONTROL user_id:]** ID do usuário.
* **[!UICONTROL token:]** Token válido do sistema.

1. Puxar a estrutura de solicitação.
