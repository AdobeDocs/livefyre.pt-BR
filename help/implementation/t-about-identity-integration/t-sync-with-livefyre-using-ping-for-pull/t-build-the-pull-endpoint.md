---
description: Crie o terminal pull para receber e responder solicitações de acesso ao seu sistema de identidade do usuário.
seo-description: Crie o terminal pull para receber e responder solicitações de acesso ao seu sistema de identidade do usuário.
seo-title: Criar o ponto de extremidade de puxamento
solution: Experience Manager
title: Criar o ponto de extremidade de puxamento
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar o ponto de extremidade de puxamento{#build-the-pull-endpoint}

Crie o terminal pull para receber e responder solicitações de acesso ao seu sistema de identidade do usuário.

1. Crie um ponto de extremidade HTTPS que receba solicitações e respostas do Livefyre com um objeto JSON que contenha os dados mais recentes do usuário.

   >[!NOTE]
   >
   >Esse terminal deve estar acessível. Também é altamente recomendável que tanto as solicitações quanto as respostas sejam enviadas pelo protocolo HTTPS.

1. Registre o Endpoint com Studio.
