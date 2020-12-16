---
description: Use o Livefyre.js para adicionar autenticação por toda a página aos seus aplicativos Livefyre.
seo-description: Use o Livefyre.js para adicionar autenticação por toda a página aos seus aplicativos Livefyre.
seo-title: Adicionar autenticação a um aplicativo usando Livefyre.js
solution: Experience Manager
title: Adicionar autenticação a um aplicativo usando Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# Adicionar autenticação a um aplicativo usando Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Use o Livefyre.js para adicionar autenticação por toda a página aos seus aplicativos Livefyre.

`Livefyre.js Aut`Ele é um pacote JavaScript desenvolvido pela Livefyre que permite que todos os aplicativos do seu site compartilhem uma única integração de autenticação. A autenticação permite que você defina como seus usuários devem se registrar, fazer logon e logout delegando esses fluxos a um objeto AuthDelegate que você definir.

## Etapa 1: Ativar autenticação para uma página {#section_pgp_jtt_bbb}

Use `Livefyre.js` para habilitar a autenticação de uma página, a fim de permitir que os usuários façam logon e interajam com os Aplicativos usando seu sistema de autenticação existente.

1. Para habilitar a autenticação em uma página, adicione `Livefyre.js` ao elemento *&lt;head>* da página da Web ou modelo de site.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Use `Livefyre.require` para ativar a autenticação. O uso de `Livefyre.require` é semelhante ao uso de exigir para chamar outros pacotes. O código de integração para exigir autenticação é semelhante a:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Etapa 2: Registrar um AuthDelegate {#section_oqm_15t_bbb}

Para habilitar a autenticação, crie um `AuthDelegate` e passe-o para `Livefyre.js` Autenticação.

Um `AuthDelegate` é um objeto definido por você que determina como os usuários farão logon, logout e visualizações.

1. Criar um `AuthDelegate`. A maneira como você constrói um `AuthDelegate` depende do seu provedor de identidade. Consulte Integração de identidade para obter instruções mais detalhadas.

1. Passe `AuthDelegate` para `Livefyre.js` Autenticação. O `AuthDelegate` mais simples registra o mesmo usuário sempre que um usuário disparou o método de logon delegado de um aplicativo:

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## Etapa 3: Sincronizar Dados do Usuário {#section_u4m_j5t_bbb}

Sincronize as informações do perfil do usuário entre o Livefyre e seu provedor de identidade.

Você deve sincronizar as informações de perfil do usuário entre o Livefyre e seu Provedor de identidade. Para obter mais informações, consulte [Integração do Janrain Capture](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
