---
description: Retorna um objeto de Coleção instanciado como um tipo de Blog. Execute
  create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-description: Retorna um objeto de Coleção instanciado como um tipo de Blog. Execute
  create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-title: Método do site do buildblogcollection
solution: Experience Manager
title: Método do site do buildblogcollection
uuid: 6 a 5 ec 6 b 9-bc 32-467 a-abe 6-a 57 c 6 defe 067
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método do site do buildblogcollection{#buildblogcollection-site-method}

Retorna um objeto de Coleção instanciado como um tipo de Blog. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String | O título da Coleção. |
| Articleid | String | Uma ID de artigo exclusiva escolhida para identificar uma coleção dentro do site. |
| url | String | O URL canônico canônico desta coleção. |

## Exemplo Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## Rupor exemplo {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

