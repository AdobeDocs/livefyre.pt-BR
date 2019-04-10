---
description: Registre o endpoint de URL para que o Livefyre possa usar o URL para
  obter informações atualizadas do perfil.
seo-description: Registre o endpoint de URL para que o Livefyre possa usar o URL para
  obter informações atualizadas do perfil.
seo-title: Registre o Endpoint com o Studio
solution: Experience Manager
title: Registre o Endpoint com o Studio
uuid: 4 eb 816 ee-d 743-43 bf-bfee-d 9 b 9 fd 98 b 482
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Registre o Endpoint com o Studio{#register-the-endpoint-with-studio}

Registre o endpoint de URL para que o Livefyre possa usar o URL para obter informações atualizadas do perfil.

Registre o Ping para URL de extração apenas uma vez por rede. Depois de definido, esse valor não deve ser alterado, a menos que o terminal obtenha os dados do perfil do usuário de seu sistema de gerenciamento de usuários.

1. Use o Studio para registrar este terminal de URL com o Livefyre.
1. Registre o URL no qual o Livefyre obterá informações atualizadas do perfil do usuário, vá para **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**e insira-o no **[!UICONTROL Ping for Pull URL]** campo.

   Por exemplo, a URL pode ser: `https://example.yoursite.com/some_path/?id={id}`

