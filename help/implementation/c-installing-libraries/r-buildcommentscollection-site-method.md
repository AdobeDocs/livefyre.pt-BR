---
description: Retorna um objeto Collection instanciado como um tipo Comments . Execute createOrUpdate() no objeto Collection para concluir o processo de compilação.
title: Método do Site buildCommentsCollection
exl-id: 9534c25a-fd1c-4a09-92e2-d196ac218ef3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 8%

---

# Método do Site buildCommentsCollection{#buildcommentscollection-site-method}

Retorna um objeto Collection instanciado como um tipo Comments . Execute createOrUpdate() no objeto Collection para concluir o processo de compilação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String   | O título da coleção. |
| articleId | String   | Uma ID de artigo exclusiva que você escolheu para identificar uma Coleção no site. |
| url | String | O URL absoluto canônico para esta coleção. |

## Exemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## Exemplo de NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
