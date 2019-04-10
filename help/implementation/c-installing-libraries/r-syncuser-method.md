---
description: Informa ao Livefyre para extrair informações do usuário de um URL de
  sincronização de usuário definido anteriormente. Retorna um Booliano.
seo-description: Informa ao Livefyre para extrair informações do usuário de um URL
  de sincronização de usuário definido anteriormente. Retorna um Booliano.
seo-title: Método de rede syncuser
solution: Experience Manager
title: Método de rede syncuser
uuid: 2 affb 03 d -3907-4 b 01-9 a 64-02 ba 1 b 06 da 14
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Método de rede syncuser{#syncuser-network-method}

Informa ao Livefyre para extrair informações do usuário de um URL de sincronização de usuário definido anteriormente. Retorna um Booliano.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| Userid | String | A ID de usuário para sincronização com o Livefyre. Você deve ter um URL de sincronização de usuário definido com o Livefyre antes de chamar este método. |

## Exemplo Java {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Saída de amostra:

```
true
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Saída de amostra:

```
true
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Saída de amostra:

```
true
```

## Exemplo de Python {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Saída de amostra:

```
True
```

## Rupor exemplo {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Saída de amostra:

```
True
```
