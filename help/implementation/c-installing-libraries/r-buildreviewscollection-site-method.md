---
description: Retorna um objeto de Coleção instanciado como um tipo de Revisão. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-description: Retorna um objeto de Coleção instanciado como um tipo de Revisão. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-title: Método do site buildreviewscollection
solution: Experience Manager
title: Método do site buildreviewscollection
uuid: 88 af 4 c 68-57 de -4 ae 9-9394-550 c 94 ede 48 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método do site buildreviewscollection{#buildreviewscollection-site-method}

Retorna um objeto de Coleção instanciado como um tipo de Revisão. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String | O título da Coleção. |
| Articleid | String | Uma ID de artigo exclusiva escolhida para identificar uma coleção dentro do site. |
| url | String | O URL canônico canônico desta coleção. |


## Exemplo Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Rupor exemplo {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

