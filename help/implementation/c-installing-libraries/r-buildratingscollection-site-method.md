---
description: Retorna um objeto Collection instanciado como um tipo de Classificações. Execute create_or_update() do objeto Collection para concluir o processo de compilação.
seo-description: Retorna um objeto Collection instanciado como um tipo de Classificações. Execute create_or_update() do objeto Collection para concluir o processo de compilação.
seo-title: método de site buildRatingsCollection
title: método de site buildRatingsCollection
uuid: 5eea2ba3-48e1-4cd2-aa73-ea81788af1df
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# método de site buildRatingsCollection{#buildratingscollection-site-method}

Retorna um objeto Collection instanciado como um tipo de Classificações. Execute create_or_update() do objeto Collection para concluir o processo de compilação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String   | O título da coleção. |
| articleId | String   | Uma ID de artigo exclusiva que você escolheu para identificar uma Coleção no site. |
| url | String | O URL absoluto canônico para esta coleção. |

## Exemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## Exemplo NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

