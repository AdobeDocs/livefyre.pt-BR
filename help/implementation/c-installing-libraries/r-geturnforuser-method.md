---
description: Este método retorna o URN para o usuário desta rede.
seo-description: Este método retorna o URN para o usuário desta rede.
seo-title: Método de Rede getUrnForUser
solution: Experience Manager
title: Método de Rede getUrnForUser
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método de Rede getUrnForUser{#geturnforuser-network-method}

Este método retorna o URN para o usuário desta rede.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| userId | String   | A userId a ser usada no URN. |

## Exemplo de Java {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Exemplo de saída:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemplo NodeJS {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Exemplo de saída:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Exemplo de saída:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Exemplo de saída:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Exemplo de saída:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
