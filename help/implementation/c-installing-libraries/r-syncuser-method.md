---
description: Informa o Livefyre a obter informações do usuário de um URL de sincronização do usuário definido anteriormente. Retorna um booliano.
seo-description: Informa o Livefyre a obter informações do usuário de um URL de sincronização do usuário definido anteriormente. Retorna um booliano.
seo-title: método de rede syncUser
solution: Experience Manager
title: método de rede syncUser
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# método de rede syncUser{#syncuser-network-method}

Informa o Livefyre a obter informações do usuário de um URL de sincronização do usuário definido anteriormente. Retorna um booliano.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| userId | String   | A ID do usuário para sincronização com o Livefyre. É necessário ter um URL de sincronização do usuário definido com o Livefyre antes de chamar esse método. |

## Exemplo de Java {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Exemplo de saída:

```
true
```

## Exemplo de NodeJS {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Exemplo de saída:

```
true
```

## Exemplo de PHP {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Exemplo de saída:

```
true
```

## Exemplo Python {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Exemplo de saída:

```
True
```

## Exemplo de Ruby {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Exemplo de saída:

```
True
```
