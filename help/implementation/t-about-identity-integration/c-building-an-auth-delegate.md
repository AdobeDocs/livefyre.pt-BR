---
description: O objeto AuthDelegate implementa o comportamento desejado para executar ações e eventos de autenticação, de modo que você possa personalizar a integração com o sistema de autenticação existente do site.
title: Objeto AuthDelegate
exl-id: 7c669138-627e-476e-a177-c71346f730df
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Objeto AuthDelegate{#authdelegate-object}

O objeto AuthDelegate implementa o comportamento desejado para executar ações e eventos de autenticação, de modo que você possa personalizar a integração com o sistema de autenticação existente do site.

## Criação de um representante de autenticação {#section_wmn_tv2_gz}

O pacote de autenticação deve ser fornecido com um delegado de autenticação antes de poder executar uma ação. Um delegado de autenticação é qualquer objeto JavaScript que implementa um dos métodos neste tópico.

## .login(endLogin) {#section_mpk_lv2_gz}

Faça logon em um usuário válido e chame a função finishLogin com um objeto Error , se houver um erro, ou as credenciais Livefyre do usuário. Implementações comuns desse método redirecionam o usuário para uma página de logon ou abrem uma nova janela ou modal.

Este exemplo notifica automaticamente a autenticação de um usuário do Livefyre com o token de autenticação:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

O mais simples representante de logon pode solicitar ao usuário final seu token de autenticação Livefyre.

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

Faça logout de um usuário e chame a função finishLogout com um objeto Error se houver um erro ou nulo para notificar o autenticação que o logout foi bem-sucedido.

Por exemplo:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

Execute as ações para visualizar o perfil de um usuário.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

Execute uma ação para editar o perfil de um usuário.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Ao implementar todos os métodos listados acima, o auth pode ser configurado com um representante de autenticação personalizado. Depois que um delegado é construído, ele pode ser fornecido para auth usando o método delegado.

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
