---
description: Para autenticar um usuário com o Livefyre por um fluxo não acionado por
  um aplicativo Livefyre, o Livefyre recomenda implementar o método foreachauthentication
  no objeto authdelegate.
seo-description: Para autenticar um usuário com o Livefyre por um fluxo não acionado
  por um aplicativo Livefyre, o Livefyre recomenda implementar o método foreachauthentication
  no objeto authdelegate.
seo-title: Implementação do SSO
solution: Experience Manager
title: Implementação do SSO
uuid: c 96 d 456 c-b 1 ac -40 e 0-8 d 18-224652 b 9697 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Implementação do SSO{#implementing-sso}

Para autenticar um usuário com o Livefyre por um fluxo não acionado por um aplicativo Livefyre, o Livefyre recomenda implementar o método foreachauthentication no objeto authdelegate.

Isso será chamado quando `authDelegate` for passado `auth.delegate`e será aprovado uma função autenticada que pode ser transmitida várias vezes. Este método fornece uma inversão de controle para eventos de autenticação, para que sua `AuthDelegateobject` autocontida possa ser autocontida sem que uma referência global seja necessária.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

O Livefyre depende dos tokens do usuário para coordenar a autenticação. Como resultado, esse token deve ser retornado pelo serviço de identidade para autenticar um usuário com o Livefyre. Para saber como criar um token de usuário do Livefyre, consulte Criar um token de autenticação do usuário.

>[!NOTE]
>
>Após um login bem-sucedido, o autenticador criará uma sessão para o usuário e tentará carregar a sessão de um usuário na atualização da página e recarregar. `auth.logout()` eliminará esta sessão. Isso significa que não é necessário gerenciar a sessão de um usuário independentemente da autorização.

