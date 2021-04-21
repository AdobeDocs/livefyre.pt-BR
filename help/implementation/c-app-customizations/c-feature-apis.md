---
description: Automatize o processo usando as APIs de recurso
title: APIs de recursos
exl-id: 765e47fe-a406-44e6-b4fb-b2e85fc83c01
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# APIs de recursos{#feature-apis}

Automatize o processo usando as APIs de recurso

Use as APIs de recurso para automatizar o processo pelo qual o conteúdo é apresentado. Por exemplo, ao criar um Blog em tempo real ou um Aplicativo de comentário, atribua todo o conteúdo publicado por um moderador selecionado para orientar a conversa e estabelecer consistência no fluxo.

O Livefyre oferece APIs Feature e Unfeature .

## Recurso {#section_jpw_nqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

&#x200B; Digite o token de usuário para o moderador selecionado.

**Dados da postagem**

```
{value: <number>} 
```

O valor será usado para classificar o conteúdo em destaque, do maior para o menor (10 aparecerá antes de 1 na lista de conteúdo em destaque). Esse valor é padronizado para **now** em época, portanto, os comentários em destaque normalmente serão classificados do mais novo ao mais antigo.

**Exemplo de resposta**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>O campo de dados ainda não está em uso.

## Cancelar funcionalidade {#section_knh_mqw_xz}

**Recurso**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Insira o token de usuário para o moderador selecionado.

**Exemplo de resposta**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>O campo de dados ainda não está em uso.
