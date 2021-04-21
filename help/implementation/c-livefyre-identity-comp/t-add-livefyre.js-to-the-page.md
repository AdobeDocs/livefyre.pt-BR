---
description: O Livefyre.js é uma pequena biblioteca base que fornece autenticação para aplicativos no site.
title: Adicionar Livefyre.js à página
exl-id: 4c5dfb31-b7e5-48f7-826c-cddbee06d876
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# Adicionar Livefyre.js à página{#add-livefyre-js-to-the-page}

O Livefyre.js é uma pequena biblioteca base que fornece autenticação para aplicativos no site.

Para habilitar a autenticação:

1. Adicione Livefyre.js ao elemento `<head>` de sua página da Web ou modelo de site.
1. Adicione uma das seguintes opções à página:

   * `globalwindow.Livefyre` variável
   * `Livefyre.require` para carregar outros pacotes do Livefyre sob demanda

      ```
      <script src="//cdn.livefyre.com/Livefyre.js"></script>
      ```
