---
description: Crie uma nova coleção criando um collcollectionmeta que é passado para
  o Livefyre.
seo-description: Crie uma nova coleção criando um collcollectionmeta que é passado
  para o Livefyre.
seo-title: Criar uma coleção usando o collectionmeta token
solution: Experience Manager
title: Criar uma coleção usando o collectionmeta token
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Criar uma coleção usando o collectionmeta token{#create-a-collection-using-the-collectionmeta-token}

Crie uma nova coleção criando um collcollectionmeta que é passado para o Livefyre.

1. Crie o collectionmeta token.
1. Crie a soma de verificação.

   A soma de verificação será necessária se você quiser notificar o Livefyre de qualquer alteração feita na Coleção. O Livefyre atualizará sua coleção somente se a soma de verificação fornecida for diferente da soma de verificação enviada anteriormente. Criar uma soma de verificação é como criar um `collectionMeta` token, mas em vez de chamar `buildCollectionMetaToken` a sua chamada `buildChecksum`.

Crie tokens de usuário para autenticação no Livefyre.