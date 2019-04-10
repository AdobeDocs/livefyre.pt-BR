---
description: Retorna um objeto de Coleção instanciado como um tipo de Bate-papo. Execute
  create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-description: Retorna um objeto de Coleção instanciado como um tipo de Bate-papo.
  Execute create_ or_ update () do objeto Collection para concluir o processo de criação.
seo-title: Método do site do buildchatcollection
solution: Experience Manager
title: Método do site do buildchatcollection
uuid: 39 ee 32 d 0-29 c 9-47 a 8-a 458-a 3 cf 7 a 96 db 30
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método do site do buildchatcollection{#buildchatcollection-site-method}

Retorna um objeto de Coleção instanciado como um tipo de Bate-papo. Execute create_ or_ update () do objeto Collection para concluir o processo de criação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String | O título da Coleção. |
| Articleid | String | Uma ID de artigo exclusiva escolhida para identificar uma coleção dentro do site. |
| url | String | O URL canônico canônico desta coleção. |

## Exemplo Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Rupor exemplo {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
