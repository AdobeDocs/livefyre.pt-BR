---
description: Define o SSL para chamadas de API como ativado ou desativado.
seo-description: Define o SSL para chamadas de API como ativado ou desativado.
seo-title: método de rede setSSL
solution: Experience Manager
title: método de rede setSSL
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

---


# método de rede setSSL{#setssl-network-method}

Define o SSL para chamadas de API como ativado ou desativado.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| ssl | Booleano | O padrão é verdadeiro. se você quiser SSL ativado, caso contrário, falso. <br><ul><li>Verdadeiro - SSL ativado </li><li>Falso - SSL desativado</li></ul> |

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

## Exemplo Python {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
network.ssl = false 
```
