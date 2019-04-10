---
description: É possível alterar o texto de aviso exibido nas máscaras de vídeo usando.
seo-description: É possível alterar o texto de aviso exibido nas máscaras de vídeo
  usando.
seo-title: Userprivacymaskdelegate
solution: Experience Manager
title: Userprivacymaskdelegate
uuid: 8 e 5 a 2750-bf 45-4 e 70-a 5 f 9-37 f 5 e 7 c 61 f 8 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacymaskdelegate{#userprivacymaskdelegate}

É possível alterar o texto de aviso exibido nas máscaras de vídeo usando.

Esse texto existe para manter-se em conformidade com o regulamento do RGPD. Se uma fonte não suporta um proxy, o Livefyre exibe esse texto e uma máscara no conteúdo, a menos que um usuário clique no vídeo e aprove o rastreamento potencial dessa origem.

Se você não usar `userPrivacyMaskDelegate`, o seguinte texto padrão é exibido:

Adicionar `userPrivacyMaskDelegate` depois `userPrivacyOptOut`. Você pode adicionar todos os sinalizadores de privacidade do Livefyre simultaneamente como parte de um objeto do Livefyre.

Este é um exemplo de como usar `userPrivacyMaskDelegate`:

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
