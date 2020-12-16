---
description: Você pode alterar o texto de aviso exibido nas máscaras de vídeo usando .
seo-description: Você pode alterar o texto de aviso exibido nas máscaras de vídeo usando .
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bf45-4e70-a5f9-37f5e7c61f8e
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

Você pode alterar o texto de aviso exibido nas máscaras de vídeo usando .

Este texto existe para cumprir o Regulamento RGPD. Se uma fonte não suportar um proxy, o Livefyre exibirá esse texto e uma máscara no conteúdo, a menos que um usuário clique no vídeo e aprove o rastreamento potencial dessa fonte.

Se você não usar `userPrivacyMaskDelegate`, o seguinte texto padrão será exibido:

Adicione `userPrivacyMaskDelegate` depois de `userPrivacyOptOut`. Você pode adicionar todos os sinalizadores de privacidade do Livefyre todos de uma só vez como parte de um objeto do Livefyre.

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
