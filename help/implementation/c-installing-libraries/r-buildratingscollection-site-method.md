---
description: Retorna um objeto de Coleção instanciado como um tipo de Classificação.
  Execute create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-description: Retorna um objeto de Coleção instanciado como um tipo de Classificação.
  Execute create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-title: Método de site do buildratingscollection
title: Método de site do buildratingscollection
uuid: 5 eea 2 ba 3-48 e 1-4 cd 2-aa 73-ea 81788 af 1 df
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método de site do buildratingscollection{#buildratingscollection-site-method}

Retorna um objeto de Coleção instanciado como um tipo de Classificação. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String | O título da Coleção. |
| Articleid | String | Uma ID de artigo exclusiva escolhida para identificar uma coleção dentro do site. |
| url | String | O URL canônico canônico desta coleção. |

## Exemplo Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## Rupor exemplo {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

