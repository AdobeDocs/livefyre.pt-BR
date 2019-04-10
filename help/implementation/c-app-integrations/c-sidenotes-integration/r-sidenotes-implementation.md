---
description: Implementar observações usando a implementação .js.
seo-description: Implementar observações usando a implementação .js.
seo-title: Implementação de sidecotes
solution: Experience Manager
title: Implementação de sidecotes
uuid: aa 13852 e-e 2 b 0-4 a 86-97 cd-d 08 ab 5 e 2 cfab
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Implementação de sidecotes{#sidenotes-implementation}

## Implementar observações usando a implementação .js

Para implementar esse recurso, passe um mapeamento de objeto 1-1 das sequências de caracteres que deseja substituir para o objeto de configuração Javascript. Se você não fornecer um campo, o texto padrão será usado.

### Exemplo

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
