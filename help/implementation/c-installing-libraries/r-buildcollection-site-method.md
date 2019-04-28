---
description: 'null'
seo-description: 'null'
seo-title: Método do site do buildcollection
solution: Experience Manager
title: Método do site do buildcollection
uuid: 52 abc 42 a -9506-4492-b 219-f 2 e 05 eb 79 c 5 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método do site do buildcollection{#buildcollection-site-method}

| Variável | Tipo | Descrição |
|--- |--- |--- |
| type | Collectiontype | O tipo da Coleção. |
| title | String | O título da Coleção. |
| Articleid | String | Uma ID de artigo exclusiva escolhida para identificar uma coleção dentro do site. |
| url | String | O URL canônico canônico desta coleção. |

## Exemplo Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Rupor exemplo {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
