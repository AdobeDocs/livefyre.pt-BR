---
title: Incorporar um aplicativo
description: Incorporar um aplicativo
exl-id: 12f75093-1b4d-4cf1-8593-dbd17ff33872
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Incorporar um aplicativo{#embed-an-app}

Adicione aplicativos do Livefyre às suas páginas da Web usando a estrutura de código incorporado do Livefyre.js.

Esta documentação destina-se a um público-alvo técnico. Para [informações não técnicas sobre aplicativos](/help/using/c-about-apps/c-about-apps.md).

Esta seção descreve a estrutura do código que você precisará incluir no modelo da página para incorporar os aplicativos do Livefyre no seu site.

1. Crie um arquivo .html com um espaço reservado para Livefyre.

   Crie um novo arquivo .html no editor de texto de sua escolha. Crie um elemento `<div>` de espaço reservado no qual o aplicativo será incorporado.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Inclua a biblioteca Livefyre.js.

   Em seguida, inclua a Biblioteca JS do Livefyre. Coloque a seguinte referência em um elemento `<script>` no elemento `<head>`. Em seguida, abra a página em um navegador e use o inspetor da Web do navegador para confirmar se o Livefyre está carregado.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Construa o aplicativo Livefyre.

   Use `Livefyre.require` para criar aplicativos Core e SDK, transmitindo os pacotes Livefyre que você planeja usar.

   1. Criar um aplicativo principal.

      Para criar um aplicativo principal (Comentários, Blog ao vivo ou Chat), use a seguinte estrutura:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Crie um aplicativo SDK.

      Para criar um aplicativo SDK, como Mural de mídia ou Feed, use a seguinte estrutura:

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

      Consulte [mais informações sobre aplicativos específicos](/help/using/c-about-apps/c-about-apps.md). É recomendável fixar na versão principal mais recente do pacote (que pode ser encontrada por meio de [Livefyre.require](https://cdn.livefyre.com/packages.html)), para evitar integrações inesperadas quebradas.

Próximo: Adicione autenticação ao site para permitir que os usuários postem comentários.
