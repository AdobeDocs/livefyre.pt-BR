---
description: Retorna um objeto de Coleção instanciado como um tipo de Contagem. Execute
  create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-description: Retorna um objeto de Coleção instanciado como um tipo de Contagem.
  Execute create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-title: Método de site buildcountingcollection
title: Método de site buildcountingcollection
uuid: e 293 d 66 a -0025-4230-997 e -295 ce 4625713
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método de site buildcountingcollection{#buildcountingcollection-site-method}

Retorna um objeto de Coleção instanciado como um tipo de Contagem. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String | O título da Coleção. |
| Articleid | String | Uma ID de artigo exclusiva escolhida para identificar uma coleção dentro do site. |
| url | String | O URL canônico canônico desta coleção. |

## Exemplo Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildCountingCollection(title, articleId, url); 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildCountingCollection(title, articleId, url); 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$collection = site->buildCountingCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

## Rupor exemplo {#section_enh_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

