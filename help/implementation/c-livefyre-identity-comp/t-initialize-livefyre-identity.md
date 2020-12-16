---
description: O pacote Livefyre.js Auth garante que todos os componentes sociais na sua página possam descobrir uma única integração de autenticação.
seo-description: O pacote Livefyre.js Auth garante que todos os componentes sociais na sua página possam descobrir uma única integração de autenticação.
seo-title: Inicializar a identidade do Livefyre
title: Inicializar a identidade do Livefyre
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Inicializar o Livefyre Identity{#initialize-livefyre-identity}

O pacote Livefyre.js Auth garante que todos os componentes sociais na sua página possam descobrir uma única integração de autenticação.

O Livefyre fornece um pacote `lfep-auth-delegate` que fará uma delegação de autenticação apropriada para você. O Auth deve receber um objeto AuthDelegate que saiba como executar ações de autenticação, como logon e logout.

1. Adicione Livefyre.js à sua página da Web.
1. Para instruir o Auth a delegar essas ações à Livefyre Identity, adicione o seguinte:

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
