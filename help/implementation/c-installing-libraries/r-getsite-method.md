---
description: Retorna um novo objeto Site.
seo-description: Retorna um novo objeto Site.
seo-title: Método de rede getsite
solution: Experience Manager
title: Método de rede getsite
uuid: 67 de 781 e -5240-4 be 5-9 e 93-c 614828 e 0 bb 5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método de rede getsite{#getsite-network-method}

Retorna um novo objeto Site.
| Variável | Tipo | Descrição|
|— |— |— |
| Siteid | String | A ID fornecida do Livefyre para o site ou aplicativo ao qual a coleção pertence. Por exemplo: 303617. |
| Sitekey | String | O Chave secreta fornecida pelo Livefyre para siteid. |

## Exemplo Java {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Exemplo de Python {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Rupor exemplo {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

