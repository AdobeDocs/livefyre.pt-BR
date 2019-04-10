---
description: Automatizar o processo usando as apis de recurso
seo-description: Automatizar o processo usando as apis de recurso
seo-title: Apis de recurso
title: Apis de recurso
uuid: eac 3 a 156-0 b 60-4 ffa -8 b 6 f-e 451 eb 03 da 77
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Apis de recurso{#feature-apis}

Automatizar o processo usando as apis de recurso

Use as apis de recurso para automatizar o processo em destaque. Por exemplo, ao criar um Blog ou Aplicativo de comentário ao vivo, todo o conteúdo publicado por um moderador selecionado para orientar a conversa e estabelecer consistência no stream.

O Livefyre oferece Apis de recurso e não recursos.

## Recurso {#section_jpw_nqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

Digite o token do usuário para o moderador selecionado.

**Dados de postagem**

```
{value: <number>} 
```

O valor será usado para classificar conteúdo em destaque, maior para o menor (10 aparecerá antes de 1 na lista de conteúdo em destaque). Esse valor é padrão **agora** em tempo de época, portanto os comentários em destaque geralmente serão classificados mais recentes para o mais antigo.

**Exemplo de resposta**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>O campo de dados ainda não está em uso.

## Não recurso {#section_knh_mqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Digite o token do usuário para o moderador selecionado.

**Exemplo de resposta**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>O campo de dados ainda não está em uso.

