---
description: Retorna um objeto Collection instanciado como um tipo de Revisões. Execute create_or_update() do objeto Collection para concluir o processo de compilação.
seo-description: Retorna um objeto Collection instanciado como um tipo de Revisões. Execute create_or_update() do objeto Collection para concluir o processo de compilação.
seo-title: método de site buildReviewsCollection
solution: Experience Manager
title: método de site buildReviewsCollection
uuid: 88af4c68-57de-4ae9-9394-550c94ede48f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# método de site buildReviewsCollection{#buildreviewscollection-site-method}

Retorna um objeto Collection instanciado como um tipo de Revisões. Execute create_or_update() do objeto Collection para concluir o processo de compilação.

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

## Exemplo Python {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

