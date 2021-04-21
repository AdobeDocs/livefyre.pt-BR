---
description: Crie uma nova Coleção criando um token collectionMeta que é passado para o Livefyre.
title: Criar uma coleção usando o token CollectionMeta
exl-id: d2dafc90-de21-4998-8e85-83f970524329
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Criar uma coleção usando o CollectionMeta Token{#create-a-collection-using-the-collectionmeta-token}

Crie uma nova Coleção criando um token collectionMeta que é passado para o Livefyre.

1. Crie o token collectionMeta.
1. Crie a soma de verificação.

   A soma de verificação é necessária se você quiser notificar o Livefyre de qualquer alteração que tenha feito em sua Coleção. Livefyre atualizará sua Coleção somente se a soma de verificação fornecida for diferente da soma de verificação enviada anteriormente. Criar uma soma de verificação é como criar um token `collectionMeta`, mas em vez de chamar `buildCollectionMetaToken` você chama `buildChecksum`.

Crie tokens de usuário para autenticação no Livefyre.
