---
description: O pacote Livefyre.js Auth garante que todos os componentes sociais da página possam descobrir uma única integração de autenticação.
title: Inicializar a identidade do Livefyre
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Inicializar identidade do Livefyre{#initialize-livefyre-identity}

O pacote Livefyre.js Auth garante que todos os componentes sociais da página possam descobrir uma única integração de autenticação.

O Livefyre fornece um pacote `lfep-auth-delegate` que fará um representante de autenticação apropriado para você. A autenticação deve ser fornecida por um objeto AuthDelegate que saiba como executar ações de autenticação, como logon e logout.

1. Adicione Livefyre.js à sua página da Web.
1. Para informar ao Auth para delegar essas ações à identidade do Livefyre, adicione o seguinte:

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
