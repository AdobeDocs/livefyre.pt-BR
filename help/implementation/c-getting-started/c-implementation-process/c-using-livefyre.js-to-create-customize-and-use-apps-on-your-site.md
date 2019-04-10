---
seo-title: Incorporar um aplicativo
solution: Experience Manager
title: Incorporar um aplicativo
uuid: e 75 caf 0 e -04 ea -4 b 04-89 ed-fea 1183 ecf 63
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Incorporar um aplicativo{#embed-an-app}

Adicione aplicativos do Livefyre às suas páginas da Web usando a estrutura de código incorporado do Livefyre. js.

Esta documentação destina-se a um público-alvo técnico. Para [informações não técnicas sobre aplicativos](/help/using/c-about-apps/c-about-apps.md).

Esta seção descreve a estrutura de códigos que deverá ser incluída no modelo de página para incorporar aplicativos do Livefyre ao seu site.

1. Crie um arquivo.html com um espaço reservado do Livefyre.

   Crie um novo arquivo.html no editor de texto de sua escolha. Crie um elemento do Livefyre do `<div>` espaço reservado no qual o aplicativo será incorporado.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Inclua a biblioteca do Livefyre. js.

   Em seguida, inclua a Biblioteca JS do Livefyre. Coloque a seguinte referência em um `<script>` elemento no `<head>` elemento. Em seguida, abra sua página em um navegador e use o inspetor web do navegador para confirmar que o Livefyre é carregado.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Construa o aplicativo Livefyre.

   Use `Livefyre.require` para criar aplicativos principais e SDK passando no (s) pacote (s) do Livefyre que você planeja usar.

   1. Crie um aplicativo principal.

      Para criar um Aplicativo principal (Comentários, Blog ao vivo ou Bate-papo), use a seguinte estrutura:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Crie um aplicativo do SDK.

      Para criar um aplicativo SDK como o Media Wall ou Feed, use a seguinte estrutura:

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

      Consulte [mais informações sobre aplicativos específicos](/help/using/c-about-apps/c-about-apps.md). Recomenda-se fixar à versão mais recente do pacote (que pode ser encontrada por meio [do Livefyre. exigir](https://cdn.livefyre.com/packages.html)), a fim de evitar integrações quebradas inesperadas.

Próximo: Adicione autenticação ao site para permitir que os usuários façam comentários.
