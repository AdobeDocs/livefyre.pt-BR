---
description: 'null'
seo-description: 'null'
seo-title: método de site buildCollection
solution: Experience Manager
title: método de site buildCollection
uuid: 52abc42a-9506-4492-b219-f2e05eb79c5f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# método de site buildCollection{#buildcollection-site-method}

| Variável | Tipo | Descrição |
|--- |--- |--- |
| type | CollectionType | O tipo da coleção. |
| title | String   | O título da coleção. |
| articleId | String   | Uma ID de artigo exclusiva que você escolheu para identificar uma Coleção no site. |
| url | String | O URL absoluto canônico para esta coleção. |

## Exemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Exemplo NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
