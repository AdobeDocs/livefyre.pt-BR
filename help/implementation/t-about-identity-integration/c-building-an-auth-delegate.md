---
description: O objeto authdelegate implementa o comportamento desejado para executar ações de autenticação e eventos, para que você possa personalizar a integração com o sistema de autenticação existente do site.
seo-description: O objeto authdelegate implementa o comportamento desejado para executar ações de autenticação e eventos, para que você possa personalizar a integração com o sistema de autenticação existente do site.
seo-title: Objeto authdelegate
solution: Experience Manager
title: Objeto authdelegate
uuid: a 6 acc 4 ef-d 442-4782-9 bfa-bbe 494547 c 2 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Objeto authdelegate{#authdelegate-object}

O objeto authdelegate implementa o comportamento desejado para executar ações de autenticação e eventos, para que você possa personalizar a integração com o sistema de autenticação existente do site.

## Criação de uma delegação de autenticação {#section_wmn_tv2_gz}

O pacote de autenticação deve ser fornecido com um representante de autenticação antes de poder executar uma ação. Um representante de autenticação é qualquer objeto javascript que implementa um dos métodos neste tópico.

## . login (finishlogin) {#section_mpk_lv2_gz}

Faça logon em um usuário válido e chame a função finishlogin com um objeto Error se houver um erro ou as credenciais do Livefyre do usuário. Implementações comuns desse método redirecionam o usuário para uma página de logon ou abrem uma nova janela ou modal.

Este exemplo notifica automaticamente o auth de um usuário do Livefyre com o token de autenticação, token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

O delegado de logon mais simples pode solicitar ao usuário final o token de Autenticação do Livefyre.

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## . logout (finishlogout) {#section_uqz_2v2_gz}

Faça logout de um usuário e chame a função finishlogout com um objeto Error se houver um erro ou nulo para notificar autenticação de que o logout foi bem-sucedido.

Por exemplo:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## . Viewprofile (usuário) {#section_kkv_dv2_gz}

Execute uma ação para visualizar o perfil de um usuário.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## . Editprofile (usuário) {#section_bkx_pq2_gz}

Execute uma ação para editar o perfil de um usuário.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Ao implementar todos os métodos listados acima, é possível configurar a autenticação com um autenticador personalizado personalizado. Depois que um delegado foi criado, ele pode ser fornecido para autenticação usando o método delegado.

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```

