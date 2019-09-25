---
description: Você pode fazer logon de um usuário pelo console durante a integração e os testes para depurar a autorização.
seo-description: Você pode fazer logon de um usuário pelo console durante a integração e os testes para depurar a autorização.
seo-title: Depuração do delegado de autenticação
solution: Experience Manager
title: Depuração do delegado de autenticação
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Depuração do delegado de autenticação{#debugging-auth-delegate}

Você pode fazer logon de um usuário pelo console durante a integração e os testes para depurar a autorização.

Faça logon em um usuário pelo console usando o seguinte `auth.authenticate` (token) e passe um token de usuário do Livefyre para autenticar usuários na página.

Você também pode modificar o exemplo mostrado acima e adicionar o seguinte snippet em linha no seu JavaScript para fazer rapidamente logon no Livefyre (requer uma referência para autenticação).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

