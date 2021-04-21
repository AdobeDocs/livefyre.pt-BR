---
description: Este método retorna o URN para o usuário desta rede.
title: Método de Rede getUrnForUser
exl-id: 272e724e-d09d-4d7d-9967-a229707ff47f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# Método de Rede getUrnForUser{#geturnforuser-network-method}

Este método retorna o URN para o usuário desta rede.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| userId | String   | O userId a ser usado no URN. |

## Exemplo de Java {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Exemplo de saída:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Exemplo de NodeJS {#section_xkd_gds_rz}

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
