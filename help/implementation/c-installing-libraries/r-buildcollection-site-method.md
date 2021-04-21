---
title: Método do Site buildCollection
description: Método do Site buildCollection
exl-id: d5c9a2fb-2d30-44f4-8ebf-24b0ec7babee
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 15%

---

# Método do Site buildCollection{#buildcollection-site-method}

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

## Exemplo de NodeJS {#section_xkd_gds_rz}

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
