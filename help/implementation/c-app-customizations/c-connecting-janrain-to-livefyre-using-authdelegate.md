---
description: O Livefyre.required fornece um plug-in que permite que o auth escute o barramento do Backplane Janrain.
seo-description: O Livefyre.required fornece um plug-in que permite que o auth escute o barramento do Backplane Janrain.
seo-title: Conectando Janrain ao Livefyre usando AuthDelegate
title: Conectando Janrain ao Livefyre usando AuthDelegate
uuid: 9d56e3f4-960a-4108-aab5-2795b0e71c88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Conectando Janrain ao Livefyre usando AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}

O Livefyre.required fornece um plug-in que permite que o auth escute o barramento do Backplane do Janrain.

Quando uma mensagem de identidade/login é transmitida no canal Backplane, auth.authenticate() será chamado para você com o token de Autenticação Livefyre do usuário. Você ainda deve implementar um AuthDelegate.

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
>O objeto window.Backplane deve ser definido na sua página antes de chamar auth.plugin com o plug-in Livefyre Backplane. Para garantir que o objeto Backplane esteja disponível, chame o código de instanciação do Livefyre de um retorno de chamada onReady. Consulte seu contato com o Janrain para determinar quando outros aplicativos podem usar o objeto Backplane.

A seguir estão alguns exemplos de como um representante de autenticação pode procurar uma integração do Janrain Capture.

>[!NOTE]
>
>O delegado de autenticação varia dependendo da sua instância Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* O retorno de chamada passado para o método de logon do delegado de autenticação
* A referência à variável de captura do Janrain.
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

* **** endLogout: O retorno de chamada passado para o método de logon do delegado de autenticação.

* **** window.Backplane: Uma referência ao objeto Backplane.

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

Isso pode vincular-se a qualquer parte do site que você gostaria que os usuários visitem para exibir sua própria página de perfil. Este exemplo apenas imprime o objeto do autor passado.

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

Como Editar perfil, isso deve vincular à página de um usuário diferente do usuário conectado no momento. Isso pode ser implementado como você desejar. Este exemplo simplesmente registra o parâmetro author no console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

