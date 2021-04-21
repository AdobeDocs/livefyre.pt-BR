---
description: Registre o endpoint do URL para que o Livefyre possa usar o URL para obter informações de perfil atualizadas.
title: Registre o Endpoint com Studio
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Registre o Endpoint com Studio{#register-the-endpoint-with-studio}

Registre o endpoint do URL para que o Livefyre possa usar o URL para obter informações de perfil atualizadas.

Registre o Ping para URL de pull apenas uma vez por rede. Depois de definido, esse valor não deve ser alterado, a menos que o endpoint para buscar dados de perfil do usuário do sistema de gerenciamento de usuários seja alterado.

1. Use o Studio para registrar esse ponto de extremidade de URL com o Livefyre.
1. Registre o URL do qual o Livefyre buscará informações atualizadas do perfil do usuário, vá para **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** e insira-o no campo **[!UICONTROL Ping for Pull URL]**.

   Por exemplo, o URL pode ter a seguinte aparência: `https://example.yoursite.com/some_path/?id={id}`
