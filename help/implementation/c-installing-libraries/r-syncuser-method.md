---
description: Informa o Livefyre a obter informações do usuário de um URL de sincronização do usuário definido anteriormente. Retorna um booleano.
title: Método de Rede syncUser
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

---

# syncUser Network Method{#syncuser-network-method}

Informa o Livefyre a obter informações do usuário de um URL de sincronização do usuário definido anteriormente. Retorna um booleano.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| userId | String   | A ID do usuário para sincronizar com o Livefyre. Você deve ter um URL de sincronização de usuário definido com o Livefyre antes de chamar esse método. |

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

## Exemplo de Python {#section_dwg_gds_rz}

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
