---
description: A biblioteca principal do Livefyre usada para alimentar o Livefyre no seu site.
title: Livefyre.js
uuid: null
exl-id: 5f60ce54-5669-4768-912d-c1b13946d8b8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# Método updateAnchors {#updateAnchorsMethod}

Use o método updateAnchors para adicionar dinamicamente o conteúdo identificado à página.

Esse método é útil para paginação ou em outros casos em que conteúdo identificável é adicionado dinamicamente à página. Esse método define novas âncoras para os elementos correspondentes e obtém um único argumento: newSelectors.

**newSeletors**. Os seletores a serem adicionados a Observações. Pode ser uma sequência de seletor, um objeto jQuery ou uma matriz de elementos (qualquer um dos tipos aceitos pelo argumento seletores transmitido durante a construção do aplicativo).
Formato:

```
app.updateAnchors(newSelectors);
```

Exemplo:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
