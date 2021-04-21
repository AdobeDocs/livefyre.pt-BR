---
description: Livefyre.require fornece um plug-in que permite que o auth ouça o barramento do Backplane Janrain.
title: Conectar o Janrain ao Livefyre usando o AuthDelegate
exl-id: d0fe0e88-5827-478b-b2ef-03f06fb3902c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# Conectando Janrain ao Livefyre usando AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.require fornece um plug-in que permite que o auth ouça o barramento do Backplane Janrain.

Quando uma mensagem de identidade/login é transmitida no canal Backplane, auth.authentication() será chamado para você com o token de autenticação Livefyre do usuário. Você ainda deve implementar um AuthDelegate.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>O objeto window.Backplane deve ser definido na página antes de chamar auth.plugin com o plug-in Livefyre Backplane. Para garantir que o objeto Backplane esteja disponível, chame o código de instanciação do Livefyre a partir de um retorno de chamada onReady. Consulte o contato do Janrain para determinar quando outros aplicativos podem usar o objeto Backplane.

A seguir estão alguns exemplos de como um representante de autenticação pode procurar uma integração com o Janrain Capture.

>[!NOTE]
>
>O delegado de autenticação varia de acordo com a instância do Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* O retorno de chamada passado para o método de logon do delegado de autenticação
* A referência para a variável de captura do Janrain.
* : Uma referência ao objeto Backplane.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

Logout

* **endLogout:** o retorno de chamada passado para o método de logon do delegado de autenticação.

* **window.Backplane:** uma referência ao objeto Backplane.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

Editar perfil

Isso pode vincular-se a qualquer parte do site que você gostaria que os usuários visitem para visualizar sua própria página de perfil. Este exemplo apenas imprime o objeto do autor transmitido.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

Exibir perfil

Como Editar perfil, isso deve vincular a uma página de usuário diferente da página que está conectada no momento. Isso pode ser implementado da maneira que você entender. Este exemplo simplesmente registra o parâmetro author no console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```
