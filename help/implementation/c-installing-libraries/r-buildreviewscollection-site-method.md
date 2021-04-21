---
description: Retorna um objeto Collection instanciado como um tipo Reviews . Execute create_or_update() no objeto Collection para concluir o processo de compilação.
title: Método do Site buildReviewsCollection
exl-id: 581ad24c-d115-4ffb-93eb-936c2da6e3fa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# Método do Site buildReviewsCollection{#buildreviewscollection-site-method}

Retorna um objeto Collection instanciado como um tipo Reviews . Execute create_or_update() no objeto Collection para concluir o processo de compilação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String   | O título da coleção. |
| articleId | String   | Uma ID de artigo exclusiva que você escolheu para identificar uma Coleção no site. |
| url | String | O URL absoluto canônico para esta coleção. |


## Exemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## Exemplo de NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```
