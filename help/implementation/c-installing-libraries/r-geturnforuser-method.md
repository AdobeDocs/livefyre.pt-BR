---
description: Este método retorna o URN para o usuário dessa rede.
seo-description: Este método retorna o URN para o usuário dessa rede.
seo-title: Método de rede geturnforuser
solution: Experience Manager
title: Método de rede geturnforuser
uuid: b 70 b 8 b 0 f -2 b 3 a -4 a 1 d -90 d 0-93 a 97 a 137 ad 4
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método de rede geturnforuser{#geturnforuser-network-method}

Este método retorna o URN para o usuário dessa rede.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| Userid | String | O userid para usar no URN. |

## Exemplo Java {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Saída de amostra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Saída de amostra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Saída de amostra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Saída de amostra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Rupor exemplo {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Saída de amostra:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
