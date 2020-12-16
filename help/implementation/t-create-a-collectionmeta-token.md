---
description: Crie uma nova coleção criando um collectionMeta token passado para o Livefyre.
seo-description: Crie uma nova coleção criando um collectionMeta token passado para o Livefyre.
seo-title: Criar uma coleção usando o CollectionMeta Token
solution: Experience Manager
title: Criar uma coleção usando o CollectionMeta Token
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Criar uma coleção usando o CollectionMeta Token{#create-a-collection-using-the-collectionmeta-token}

Crie uma nova coleção criando um collectionMeta token passado para o Livefyre.

1. Crie o collectionMeta token.
1. Crie a soma de verificação.

   A soma de verificação é necessária se você quiser notificar o Livefyre de quaisquer alterações feitas na sua coleção. O Livefyre atualizará sua Coleção somente se a soma de verificação fornecida for diferente da soma de verificação enviada anteriormente. Criar uma soma de verificação é como criar um token `collectionMeta`, mas em vez de chamar `buildCollectionMetaToken` você chama `buildChecksum`.

Crie tokens de usuário para autenticação no Livefyre.