---
description: O objeto AuthDelegate implementa o comportamento desejado para saber como executar ações e eventos de autenticação, de modo que você possa personalizar a integração com o sistema de autenticação existente do site.
seo-description: O objeto AuthDelegate implementa o comportamento desejado para saber como executar ações e eventos de autenticação, de modo que você possa personalizar a integração com o sistema de autenticação existente do site.
seo-title: Objeto AuthDelegate
solution: Experience Manager
title: Objeto AuthDelegate
uuid: a6acc4ef-d442-4782-9bfa-bbe494547c2e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# Objeto AuthDelegate{#authdelegate-object}

O objeto AuthDelegate implementa o comportamento desejado para saber como executar ações e eventos de autenticação, de modo que você possa personalizar a integração com o sistema de autenticação existente do site.

## Criando um representante de autenticação {#section_wmn_tv2_gz}

O pacote auth deve ser fornecido com um delegado auth antes de poder executar uma ação. Um delegado de autenticação é qualquer objeto JavaScript que implementa um dos métodos neste tópico.

## .login(endLogin) {#section_mpk_lv2_gz}

Faça logon em um usuário válido e chame a função completeLogin com um objeto Error se houver um erro ou as credenciais do Livefyre do usuário. As implementações comuns deste método redirecionam o usuário para uma página de logon ou abrem uma nova janela ou modal.

Este exemplo notifica automaticamente a autenticação de um usuário do Livefyre com o token de autenticação, token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

O representante de logon mais simples pode solicitar ao usuário final o token de autenticação Livefyre.

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

## .logout(endLogout) {#section_uqz_2v2_gz}

Faça logout de um usuário e chame a função completeLogout com um objeto Error se houver um erro, ou nulo para notificar o auth de que o logout foi bem-sucedido.

Por exemplo:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

Agir para visualização do perfil de um usuário.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

Execute ações para editar o perfil de um usuário.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Ao implementar todos os métodos listados acima, a autenticação pode ser configurada com uma delegação de autenticação personalizada. Depois que um delegado é construído, ele pode ser fornecido para auth usando o método delegate.

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

