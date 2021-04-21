---
description: Você pode fazer logon de um usuário no console durante a integração e os testes para depurar a autorização.
title: Depuração do representante de autenticação
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Depuração do representante de autenticação{#debugging-auth-delegate}

Você pode fazer logon de um usuário no console durante a integração e os testes para depurar a autorização.

Faça logon de um usuário no console usando o seguinte `auth.authenticate` (token) e passe um token de usuário do Livefyre para autenticar usuários na página.

Você também pode modificar o exemplo mostrado acima e adicionar o seguinte trecho em linha no seu JavaScript para fazer logon rapidamente de um usuário no Livefyre (requer uma referência a auth).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```
