---
description: Informa o Livefyre a atualizar o URL de sincronização do usuário da rede para aquele fornecido. Retorna um booliano.
seo-description: Informa o Livefyre a atualizar o URL de sincronização do usuário da rede para aquele fornecido. Retorna um booliano.
seo-title: método de rede setUserSyncUrl
solution: Experience Manager
title: método de rede setUserSyncUrl
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# método de rede setUserSyncUrl{#setusersyncurl-network-method}

Informa o Livefyre a atualizar o URL de sincronização do usuário da rede para aquele fornecido. Retorna um booliano.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| urlTemplate | String   | O URL para se registrar no Livefyre para sincronizar IDs de usuário. Exige que &quot;`{id}`&quot; faça parte da cadeia de caracteres de URL fornecida. |

## Exemplo de Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Exemplo de saída:

```
true
```

## Exemplo de NodeJS {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Exemplo de saída:

```
true
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Exemplo de saída:

```
true
```

## Exemplo Python {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Exemplo de saída:

```
True
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Exemplo de saída:

```
True
```
