---
description: Automatize o processo usando as APIs de recurso
seo-description: Automatize o processo usando as APIs de recurso
seo-title: APIs de recursos
title: APIs de recursos
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# APIs de recursos{#feature-apis}

Automatize o processo usando as APIs de recurso

Use as APIs de recurso para automatizar o processo pelo qual o conteúdo é apresentado. Por exemplo, ao criar um Blog ao vivo ou um aplicativo de comentário, atribua todo o conteúdo publicado por um moderador selecionado para direcionar a conversa e estabelecer a consistência dentro do stream.

O Livefyre oferece APIs Feature e Unfeature.

## Recurso {#section_jpw_nqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

&#x200B;Insira o token de usuário para o moderador selecionado.

**Dados da postagem**

```
{value: <number>} 
```

O valor será usado para classificar o conteúdo em destaque, do maior ao menor (10 aparecerão antes de 1 na lista de conteúdo em destaque). O padrão desse valor é **agora** em cada época, portanto, os comentários em destaque serão classificados de novo para o mais antigo.

**Exemplo de resposta**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>O campo de dados ainda não está em uso.

## Desrecurso {#section_knh_mqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Insira o token do usuário para o moderador selecionado.

**Exemplo de resposta**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>O campo de dados ainda não está em uso.

