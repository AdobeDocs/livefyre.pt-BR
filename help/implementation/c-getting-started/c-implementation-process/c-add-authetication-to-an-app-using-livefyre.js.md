---
description: Use o Livefyre. js para adicionar autenticação em toda a página para seus aplicativos do Livefyre.
seo-description: Use o Livefyre. js para adicionar autenticação em toda a página para seus aplicativos do Livefyre.
seo-title: Adicionar a autenticação a um aplicativo usando o Livefyre. js
solution: Experience Manager
title: Adicionar a autenticação a um aplicativo usando o Livefyre. js
uuid: b 7 c 61 e 07-e 34d -45 d 7-9112-c 50155 e 38 f 1 d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# Adicionar autenticação a um aplicativo usando o Livefyre. js{#add-authetication-to-an-app-using-livefyre-js}

Use o Livefyre. js para adicionar autenticação em toda a página para seus aplicativos do Livefyre.

`Livefyre.js Aut`h é um pacote javascript desenvolvido pelo Livefyre que permite que todos os aplicativos do site compartilhem uma única integração de autenticação. O Auth permite definir como os usuários devem se registrar, fazer login e fazer logout delegando esses fluxos a um objeto authdelegate definido.

## Etapa 1: Ativar autenticação para uma página {#section_pgp_jtt_bbb}

Use `Livefyre.js` para ativar a autenticação de uma página para permitir que os usuários façam logon e interajam com aplicativos usando seu sistema de autenticação existente.

1. Para habilitar a autenticação em uma página, adicione `Livefyre.js` o elemento *&lt; head &gt;* da página da Web ou do modelo do site.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Use `Livefyre.require` para ativar a autenticação. O uso `Livefyre.require` é semelhante ao uso necessário para chamar outros pacotes. O código de integração para exigir a autenticação dessa autenticação é:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Etapa 2: Registrar um authdelegate {#section_oqm_15t_bbb}

Para ativar a autenticação, crie um `AuthDelegate` e passe para `Livefyre.js` Autenticação.

Um `AuthDelegate` é um objeto que você define que determina como os usuários farão logon, logout e visualização de perfis.

1. Crie um `AuthDelegate`. A maneira como você constrói depende `AuthDelegate` do seu provedor de identidade. Consulte Integração de identidade para obter instruções mais detalhadas.

1. Transmita a `AuthDelegate``Livefyre.js` Autenticação. O mais simples `AuthDelegate` registra o mesmo usuário em toda vez que um usuário disparou o método de logon delegado de um aplicativo:

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

Sincronize as informações do perfil do usuário entre o Livefyre e o seu provedor de identidade.

Você deve sincronizar as informações de perfil do usuário entre o Livefyre e o seu Provedor de identidade. Para obter mais informações, consulte [Integração de captura de Janchuva](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
