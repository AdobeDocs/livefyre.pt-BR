---
description: Para autenticar um usuário com o Livefyre por meio de um fluxo não acionado por um aplicativo Livefyre, o Livefyre recomenda que você implemente o método foreachAuthentication no objeto AuthDelegate.
seo-description: Para autenticar um usuário com o Livefyre por meio de um fluxo não acionado por um aplicativo Livefyre, o Livefyre recomenda que você implemente o método foreachAuthentication no objeto AuthDelegate.
seo-title: Implementação do SSO
solution: Experience Manager
title: Implementação do SSO
uuid: c96d456c-b1ac-40e0-8d18-224652b9697f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Implementando SSO{#implementing-sso}

Para autenticar um usuário com o Livefyre por meio de um fluxo não acionado por um aplicativo Livefyre, o Livefyre recomenda que você implemente o método foreachAuthentication no objeto AuthDelegate.

Isso será chamado quando `authDelegate` for passado para `auth.delegate` e uma função de autenticação que pode ser transmitida várias vezes será transmitida. Este método fornece uma inversão do controle para eventos de autenticação para que seu `AuthDelegateobject` possa ser autocontido sem a necessidade de uma referência global para autenticação.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre depende de tokens do usuário para coordenar a autenticação. Como resultado, este token deve ser devolvido pelo seu serviço de identidade para autenticar um usuário com o Livefyre. Para saber como criar um token de usuário do Livefyre, consulte Criar um token de autenticação de usuário.

>[!NOTE]
>
>Após um logon bem-sucedido, o auth criará uma sessão para o usuário e tentará carregar a sessão do usuário ao atualizar e recarregar a página. `auth.logout()` limpará esta sessão. Isso significa que não é necessário gerenciar a sessão de um usuário independentemente da autorização.

