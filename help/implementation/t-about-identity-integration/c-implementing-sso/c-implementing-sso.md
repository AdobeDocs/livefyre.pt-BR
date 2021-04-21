---
description: Para autenticar um usuário com o Livefyre por meio de um fluxo não acionado por um aplicativo do Livefyre, o Livefyre recomenda a implementação do método forAuthentication no objeto AuthDelegate .
title: Implementação de SSO
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Implementação de SSO{#implementing-sso}

Para autenticar um usuário com o Livefyre por meio de um fluxo não acionado por um aplicativo do Livefyre, o Livefyre recomenda a implementação do método forAuthentication no objeto AuthDelegate .

Isso será chamado quando `authDelegate` for passado para `auth.delegate` e uma função de autenticação que pode ser passada várias vezes será passada. Este método fornece uma inversão do controle para eventos de autenticação para que seu `AuthDelegateobject` possa ser autocontido sem exigir uma referência global para autenticação.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

O Livefyre depende de tokens de usuário para coordenar a autenticação. Como resultado, esse token deve ser retornado pelo serviço de identidade para autenticar um usuário com o Livefyre. Para saber como criar um token de usuário do Livefyre, consulte Criação de um token de autenticação de usuário.

>[!NOTE]
>
>Após um logon bem-sucedido, o auth criará uma sessão para o usuário e tentará carregar a sessão do usuário ao atualizar a página e recarregar. `auth.logout()` limpará esta sessão. Isso significa que não é necessário gerenciar a sessão de um usuário independentemente da autorização.
