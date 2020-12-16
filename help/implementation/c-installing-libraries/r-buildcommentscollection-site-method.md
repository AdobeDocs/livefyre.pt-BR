---
description: Retorna um objeto Collection instanciado como um tipo Comments. Execute createOrUpdate() a partir do objeto Collection para concluir o processo de compilação.
seo-description: Retorna um objeto Collection instanciado como um tipo Comments. Execute createOrUpdate() a partir do objeto Collection para concluir o processo de compilação.
seo-title: método de site buildCommentsCollection
solution: Experience Manager
title: método de site buildCommentsCollection
uuid: 0e5c062e-960d-4ab0-ba32-0965731a1571
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---


# método de site buildCommentsCollection{#buildcommentscollection-site-method}

Retorna um objeto Collection instanciado como um tipo Comments. Execute createOrUpdate() a partir do objeto Collection para concluir o processo de compilação.

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

## Exemplo Python {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
