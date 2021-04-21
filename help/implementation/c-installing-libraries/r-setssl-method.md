---
description: Define o SSL para chamadas de API para ativação ou desativação.
title: Método de Rede setSSL
exl-id: 5682b84a-0b4d-479b-af40-60d2c6c38155
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# Método de Rede setSSL{#setssl-network-method}

Define o SSL para chamadas de API para ativação ou desativação.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| ssl | Booleano | O padrão é verdadeiro. se quiser o SSL ativado, caso contrário, é falso. <br><ul><li>Verdadeiro - SSL ativado </li><li>False - SSL desativado</li></ul> |

## Exemplo de Java {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## Exemplo de NodeJS {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Exemplo de Python {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
network.ssl = false 
```
