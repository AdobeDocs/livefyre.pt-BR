---
description: Implementar observações usando a implementação .js.
seo-description: Implementar observações usando a implementação .js.
seo-title: Implementação de Sidenotes
solution: Experience Manager
title: Implementação de Sidenotes
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 28%

---


# Implementação de Sidenotes{#sidenotes-implementation}

## Implementar observações usando a implementação .js

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das strings que você deseja substituir para o objeto de configuração Javascript. Se você não fornecer um campo, o texto padrão será usado.

### Exemplo

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
