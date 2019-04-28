---
description: Retorna um objeto Collection instanciado como um tipo de Sidenotes. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-description: Retorna um objeto Collection instanciado como um tipo de Sidenotes. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-title: Método do site buildsitenotbarbarlection
solution: Experience Manager
title: Método do site buildsitenotbarbarlection
uuid: 2 bfbc 032-4 c 0 c -48 d 2-8 ce 6-02460 b 38 bd 6 c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método do site buildsitenotbarbarlection{#buildsitenotescollection-site-method}

Retorna um objeto Collection instanciado como um tipo de Sidenotes. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String | O título da Coleção. |
| Articleid | String | Uma ID de artigo exclusiva escolhida para identificar uma coleção dentro do site. |
| url | String | O URL canônico canônico desta coleção. |

## Exemplo Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## Rupor exemplo {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
