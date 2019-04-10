---
description: Retorna um objeto de coleção instanciado como um tipo de Comentários.
  Execute o createorupdate () do objeto Collection para concluir o processo de criação.
seo-description: Retorna um objeto de coleção instanciado como um tipo de Comentários.
  Execute o createorupdate () do objeto Collection para concluir o processo de criação.
seo-title: Método de site do buildcommentscollection
solution: Experience Manager
title: Método de site do buildcommentscollection
uuid: 0 e 5 c 062 e -960 d -4 ab 0-ba 32-0965731 a 1571
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método de site do buildcommentscollection{#buildcommentscollection-site-method}

Retorna um objeto de coleção instanciado como um tipo de Comentários. Execute o createorupdate () do objeto Collection para concluir o processo de criação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String | O título da Coleção. |
| Articleid | String | Uma ID de artigo exclusiva escolhida para identificar uma coleção dentro do site. |
| url | String | O URL canônico canônico desta coleção. |

## Exemplo Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Rupor exemplo {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
