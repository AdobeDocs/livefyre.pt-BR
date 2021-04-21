---
description: Informa o Livefyre a atualizar o URL de sincronização de usuários da rede para o URL fornecido. Retorna um booleano.
title: Método de Rede setUserSyncUrl
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# Método de Rede setUserSyncUrl{#setusersyncurl-network-method}

Informa o Livefyre a atualizar o URL de sincronização de usuários da rede para o URL fornecido. Retorna um booleano.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| urlTemplate | String   | O URL para se registrar no Livefyre para sincronizar IDs de usuário. Requer que &quot;`{id}`&quot; faça parte da cadeia de caracteres de URL fornecida. |

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

## Exemplo de Python {#section_dwg_gds_rz}

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
