---
description: A biblioteca principal do Livefyre usada para potencializar o Livefyre
  em seu site.
seo-description: A biblioteca principal do Livefyre usada para potencializar o Livefyre
  em seu site.
seo-title: Método updateanchors
solution: Experience Manager
title: Livefyre. js
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método updateanchors {#updateAnchorsMethod}

Use o método updateanchors para adicionar conteúdo sidenado à página dinamicamente.

Esse método é útil para paginação ou em outros casos em que o conteúdo com sidenload é adicionado à página dinamicamente. Esse método define novas âncoras para os elementos correspondentes e utiliza um único argumento: Newselectors.

**Newselectors**. Os seletores a serem adicionados aos Auxiliares. Pode ser uma string do seletor, um objeto jquery ou uma matriz de elementos (qualquer um dos tipos aceitos pelo argumento dos seletores passado durante a construção do aplicativo).
Formato:

```
app.updateAnchors(newSelectors);
```

Exemplo:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
