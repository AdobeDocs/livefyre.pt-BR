---
description: Você pode registrar um usuário através do console durante a integração
  e testes para depurar a autorização.
seo-description: Você pode registrar um usuário através do console durante a integração
  e testes para depurar a autorização.
seo-title: Depurar delegação de autenticação
solution: Experience Manager
title: Depurar delegação de autenticação
uuid: fb 0 c 7396-190 e -4 dc 9-bf 26-23 dde 9 efd 45 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Depurar delegação de autenticação{#debugging-auth-delegate}

Você pode registrar um usuário através do console durante a integração e testes para depurar a autorização.

Faça logon de um usuário através do console usando o seguinte `auth.authenticate` (token) e transmita um token do usuário do Livefyre para autenticar usuários na página.

Você também pode modificar o exemplo mostrado acima e adicionar o seguinte snippet em linha no javascript para registrar rapidamente um usuário no Livefyre (requer uma referência a auth).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

