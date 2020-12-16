---
description: Retorna um novo objeto Site.
seo-description: Retorna um novo objeto Site.
seo-title: Método de rede getSite
solution: Experience Manager
title: Método de rede getSite
uuid: 67de781e-5240-4be5-9e93-c614828e0bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---


# Método de Rede getSite{#getsite-network-method}

Retorna um novo objeto Site.
|Variável|Tipo|Descrição|
|— |— |— |
|siteId|String|A ID fornecida pelo Livefyre para o site ou aplicativo ao qual a Coleção pertence. Por exemplo: 303617.  |
|siteKey|String|A chave secreta fornecida pelo Livefyre para siteId.  |

## Exemplo de Java {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Exemplo de NodeJS {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Exemplo Python {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

