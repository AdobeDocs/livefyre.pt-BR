---
description: Informa o Livefyre para atualizar o URL de sincronização de usuário da rede para aquele fornecido. Retorna um Booliano.
seo-description: Informa o Livefyre para atualizar o URL de sincronização de usuário da rede para aquele fornecido. Retorna um Booliano.
seo-title: Método de rede setusersyncurl
solution: Experience Manager
title: Método de rede setusersyncurl
uuid: cd 067 e 90-a 2 da -4 e 3 d -8 e 60-7 eabfd 86 fc 7 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Método de rede setusersyncurl{#setusersyncurl-network-method}

Informa o Livefyre para atualizar o URL de sincronização de usuário da rede para aquele fornecido. Retorna um Booliano.

| Variável | Tipo | Descrição |
|--- |--- |--- |
| Urltemplate | String | O URL para se registrar no Livefyre para sincronização de IDs de usuário. Requer «`{id}`» para fazer parte da string de URL fornecida. |

## Exemplo Java {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Saída de amostra:

```
true
```

## Exemplo de nodejs {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Saída de amostra:

```
true
```

## Exemplo PHP {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Saída de amostra:

```
true
```

## Exemplo de Python {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Saída de amostra:

```
True
```

## Rupor exemplo {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Saída de amostra:

```
True
```
