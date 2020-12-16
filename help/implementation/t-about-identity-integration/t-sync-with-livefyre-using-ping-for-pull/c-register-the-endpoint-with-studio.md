---
description: Registre o endpoint do URL para que Livefyre possa usar o URL para obter informações atualizadas do perfil.
seo-description: Registre o endpoint do URL para que Livefyre possa usar o URL para obter informações atualizadas do perfil.
seo-title: Registrar o Ponto de Extremidade no Studio
solution: Experience Manager
title: Registrar o Ponto de Extremidade no Studio
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# Registre o Endpoint com Studio{#register-the-endpoint-with-studio}

Registre o endpoint do URL para que Livefyre possa usar o URL para obter informações atualizadas do perfil.

Registre o Ping para URL de Puxo somente uma vez por rede. Depois de definido, esse valor não deve ser alterado a menos que o ponto de extremidade para obter dados de perfil do usuário do sistema de gerenciamento do usuário seja alterado.

1. Use o Studio para registrar esse terminal de URL com o Livefyre.
1. Registre o URL do qual o Livefyre buscará informações atualizadas do perfil do usuário, vá para **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** e insira-as no campo **[!UICONTROL Ping for Pull URL]**.

   Por exemplo, o URL pode ter a seguinte aparência: `https://example.yoursite.com/some_path/?id={id}`

