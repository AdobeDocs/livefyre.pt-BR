---
description: Define o SSL para ligar ou desligar chamadas de API.
seo-description: Define o SSL para ligar ou desligar chamadas de API.
seo-title: Método de rede setssl
solution: Experience Manager
title: Método de rede setssl
uuid: 8 d 989 e 63-c 859-456 a -99 ca -8 d 87933913 ba
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método de rede setssl{#setssl-network-method}

Define o SSL para ligar ou desligar chamadas de API.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| ssl | Booliano | O padrão é verdadeiro. se desejar SSL, senão falso. <br><ul><li>Verdadeiro - SSL em </li><li>False - SSL off</li></ul> |

## Exemplo Java {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Rupor exemplo {#section_enh_gds_rz}

```
network.ssl = false 
```
