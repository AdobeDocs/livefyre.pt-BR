---
description: Você pode alterar o texto de aviso exibido nas máscaras de vídeo usando .
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

Você pode alterar o texto de aviso exibido nas máscaras de vídeo usando .

Este texto existe para estar em conformidade com o Regulamento GDPR. Se uma fonte não oferecer suporte a um proxy, o Livefyre exibirá esse texto e uma máscara no conteúdo, a menos que um usuário clique no vídeo e aprove o rastreamento potencial dessa fonte.

Se você não usar `userPrivacyMaskDelegate`, o seguinte texto padrão será exibido:

Adicione `userPrivacyMaskDelegate` depois de `userPrivacyOptOut`. Você pode adicionar todos os sinalizadores de privacidade do Livefyre de uma só vez como parte de um objeto do Livefyre.

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
