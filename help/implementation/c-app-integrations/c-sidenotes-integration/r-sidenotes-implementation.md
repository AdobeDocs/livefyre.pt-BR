---
description: Implementar observações usando a implementação .js.
title: Implementação de observações
exl-id: 07a68677-c67e-4128-8cb7-c5fb9e0ecc60
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 22%

---

# Implementação de identificações{#sidenotes-implementation}

## Implementar observações usando a implementação .js

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das cadeias de caracteres que deseja substituir no objeto de configuração Javascript. Se um campo não for fornecido, o texto padrão será usado.

### Exemplo

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
