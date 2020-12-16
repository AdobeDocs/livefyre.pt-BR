---
description: Retorna um objeto Collection instanciado como um tipo de Chat. Execute create_or_update() do objeto Collection para concluir o processo de compilação.
seo-description: Retorna um objeto Collection instanciado como um tipo de Chat. Execute create_or_update() do objeto Collection para concluir o processo de compilação.
seo-title: método de site buildChatCollection
solution: Experience Manager
title: método de site buildChatCollection
uuid: 39ee32d0-29c9-47a8-a458-a3cf7a96db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# método de site buildChatCollection{#buildchatcollection-site-method}

Retorna um objeto Collection instanciado como um tipo de Chat. Execute create_or_update() do objeto Collection para concluir o processo de compilação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| title | String   | O título da coleção. |
| articleId | String   | Uma ID de artigo exclusiva que você escolheu para identificar uma Coleção no site. |
| url | String | O URL absoluto canônico para esta coleção. |

## Exemplo de Java {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## Exemplo de NodeJS {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Exemplo Python {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
