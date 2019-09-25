---
seo-title: Incorporar um aplicativo
solution: Experience Manager
title: Incorporar um aplicativo
uuid: e75caf0e-04ea-4b04-89ed-fea1183ecf63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Incorporar um aplicativo{#embed-an-app}

Adicione aplicativos do Livefyre a suas páginas da Web usando a estrutura de código incorporada do Livefyre.js.

Esta documentação destina-se a um público técnico. Para obter informações [não técnicas sobre aplicativos](/help/using/c-about-apps/c-about-apps.md).

Esta seção descreve a estrutura de código que será necessário incluir no modelo de página para incorporar os aplicativos Livefyre ao site.

1. Crie um arquivo .html com um espaço reservado para Livefyre.

   Crie um novo arquivo .html no editor de texto de sua escolha. Crie um `<div>` elemento Livefyre de espaço reservado no qual o aplicativo será incorporado.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Inclua a biblioteca Livefyre.js.

   Em seguida, inclua a Biblioteca Livefyre JS. Coloque a seguinte referência em um `<script>` elemento no seu `<head>` elemento. Em seguida, abra sua página em um navegador e use o inspetor da Web do navegador para confirmar se o Livefyre está carregado.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Construa o aplicativo Livefyre.

   Use `Livefyre.require` para criar aplicativos Core e SDK transmitindo os pacotes Livefyre que você planeja usar.

   1. Crie um aplicativo principal.

      Para criar um aplicativo principal (Comentários, Blog ao vivo ou Bate-papo), use a seguinte estrutura:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Crie um aplicativo SDK.

      Para criar um aplicativo SDK, como Media Wall ou Feed, use a seguinte estrutura:

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      Consulte [mais informações sobre aplicativos](/help/using/c-about-apps/c-about-apps.md)específicos. Recomenda-se fixar a versão principal mais recente do pacote (que pode ser encontrada através do [Livefyre.requirements](https://cdn.livefyre.com/packages.html)), para evitar integrações inesperadas quebradas.

Próximo: Adicione autenticação ao site para permitir que os usuários postem comentários.
