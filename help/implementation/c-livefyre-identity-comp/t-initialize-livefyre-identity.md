---
description: O pacote do Livefyre. js garante que todos os componentes sociais na
  sua página possam descobrir uma única integração de autenticação.
seo-description: O pacote do Livefyre. js garante que todos os componentes sociais
  na sua página possam descobrir uma única integração de autenticação.
seo-title: Inicializar identidade do Livefyre
title: Inicializar identidade do Livefyre
uuid: 9365 d 827-2734-4 a 84-bfe 7-9 be 573 b 2 b 03 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Inicializar identidade do Livefyre{#initialize-livefyre-identity}

O pacote do Livefyre. js garante que todos os componentes sociais na sua página possam descobrir uma única integração de autenticação.

O Livefyre fornece `lfep-auth-delegate` um pacote que fará um representante de autenticação apropriado para você. O Auth deve ser fornecido um objeto authdelegate que saiba como executar ações de autenticação, como login e logout.

1. Adicione Livefyre. js à sua página da Web.
1. Para saber o Auth para delegar essas ações à Identidade do Livefyre, adicione o seguinte:

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
