---
description: Retorna um novo objeto de Site.
title: Método de Rede getSite
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# Método de Rede getSite{#getsite-network-method}

Retorna um novo objeto de Site.
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

## Exemplo de Python {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```
