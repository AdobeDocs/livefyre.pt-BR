---
description: O Livefyre. requer um plug-plugin que permita a autenticação de um ônibus
  de Janrain Backflight.
seo-description: O Livefyre. requer um plug-plugin que permita a autenticação de um
  ônibus de Janrain Backflight.
seo-title: Conectando Janrain ao Livefyre usando authdelegate
title: Conectando Janrain ao Livefyre usando authdelegate
uuid: 9 d 56 e 3 f 4-960 a -4108-aab 5-2795 b 0 e 71 c 88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Conectando Janrain ao Livefyre usando authdelegate{#connecting-janrain-to-livefyre-using-authdelegate}

O Livefyre. requer um plug-plugin que permita a autenticação de um ônibus de Janrain Backflight.

Quando uma mensagem de identidade/logon é transmitida no canal de Backmap, o auth. authenticate () será chamado para você com o token de Autenticação do Livefyre do usuário. Você ainda deve implementar um authdelegate.

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
>O objeto window. Backactivity deve ser definido na página antes de chamar auth. plugin com o plug-plugin do Livefyre Backplanet. Para garantir que o objeto Plano retroativo esteja disponível, chame o código de instanciação do Livefyre de um retorno de chamada onready. Entre em contato com o contato do Janrain para determinar quando outros aplicativos podem usar o objeto Backplano.

Estes são alguns exemplos de como um representante de autenticação pode procurar uma integração de Janrain Capture.

>[!NOTE]
>
>Seu delegado de autenticação variará dependendo da sua instância de Janrain.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* O retorno de chamada passado para o método de logon do seu autenticador
* A referência à variável de captura do Janrain.
* : Uma referência ao objeto backplano.

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

* **Finishlogout:** O retorno de chamada passado para o método de logon do seu autenticador de autenticação.

* **window. Backplano:** Uma referência ao objeto backplano.

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

Isso pode ser vinculado a qualquer parte do site que você deseja que os usuários visitem para visualizar sua própria página de perfil. Este exemplo apenas imprime o objeto do autor passado.

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

Como Editar perfil, isso deve vincular à página de um usuário diferente do usuário atualmente conectado. Isso pode ser implementado no entanto, você pode ser ajustado. Esse exemplo simplesmente registra o parâmetro do autor para o console.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

