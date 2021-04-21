---
description: Use o Livefyre.js para adicionar autenticação em toda a página aos aplicativos do Livefyre.
title: Adicionar autenticação a um aplicativo usando Livefyre.js
exl-id: 6246a2bc-e7ff-4f86-a63a-36261c71d460
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Adicionar autenticação a um aplicativo usando Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Use o Livefyre.js para adicionar autenticação em toda a página aos aplicativos do Livefyre.

`Livefyre.js Aut`Ele é um pacote JavaScript desenvolvido pela Livefyre que permite que todos os aplicativos de seu site compartilhem uma única integração de autenticação. A autenticação permite definir como seus usuários devem se registrar, fazer logon e fazer logoff, delegando esses fluxos a um objeto AuthDelegate que você define.

## Etapa 1: Ativar autenticação para uma página {#section_pgp_jtt_bbb}

Use `Livefyre.js` para habilitar a autenticação de uma página para permitir que os usuários façam logon e interajam com os Aplicativos usando seu sistema de autenticação existente.

1. Para habilitar a autenticação em uma página, adicione `Livefyre.js` ao elemento *&lt;head>* de sua página da Web ou modelo de site.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Use `Livefyre.require` para habilitar a autenticação. O uso de `Livefyre.require` é semelhante ao uso de exigir para chamar outros pacotes. O código de integração para exigir autenticação é semelhante a:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Etapa 2: Registrar um AuthDelegate {#section_oqm_15t_bbb}

Para habilitar a autenticação, crie um `AuthDelegate` e passe-o para a autenticação `Livefyre.js`.

Um `AuthDelegate` é um objeto definido por você que determina como os usuários farão logon, logout e exibirão perfis.

1. Criar um `AuthDelegate`. A maneira como você constrói um `AuthDelegate` depende do seu provedor de identidade. Consulte Integração de identidade para obter instruções mais detalhadas.

1. Passe o `AuthDelegate` para a autenticação `Livefyre.js`. O `AuthDelegate` mais simples registra o mesmo usuário no sempre que um usuário acionou o método de logon delegado de um aplicativo:

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## Etapa 3: Sincronizar dados do usuário {#section_u4m_j5t_bbb}

Sincronize as informações do perfil de usuário entre o Livefyre e seu provedor de identidade.

Você deve sincronizar as informações de perfil do usuário entre o Livefyre e o Provedor de identidade. Para obter mais informações, consulte [Integração de captura do Janrain](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
