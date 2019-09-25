---
description: A biblioteca principal do Livefyre usada para alimentar o Livefyre no seu site.
seo-description: A biblioteca principal do Livefyre usada para alimentar o Livefyre no seu site.
seo-title: método updateAnchors
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# método updateAnchors {#updateAnchorsMethod}

Use o método updateAnchors para adicionar conteúdo identificado à página dinamicamente.

Esse método é útil para paginação ou em outros casos em que o conteúdo identificável é adicionado dinamicamente à página. Este método define novas âncoras para os elementos correspondentes e tem um único argumento: newSelectors.

**newSeltors**. Os seletores a serem adicionados a Sidenotes. Pode ser uma sequência de seletor, um objeto jQuery ou uma matriz de elementos (qualquer um dos tipos aceitos pelo argumento seletores transmitido durante a construção do aplicativo).
Formato:

```
app.updateAnchors(newSelectors);
```

Exemplo:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
