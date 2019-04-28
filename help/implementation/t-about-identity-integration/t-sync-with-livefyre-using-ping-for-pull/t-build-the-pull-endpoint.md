---
description: Crie o terminal de extração para receber e responder a solicitações de acesso ao seu sistema de identidade do usuário.
seo-description: Crie o terminal de extração para receber e responder a solicitações de acesso ao seu sistema de identidade do usuário.
seo-title: Criar o endpoint de extração
solution: Experience Manager
title: Criar o endpoint de extração
uuid: 1703152 f-aaa 7-4 a 88-aa 33-d 9 f 8957 ad 42 b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Criar o endpoint de extração{#build-the-pull-endpoint}

Crie o terminal de extração para receber e responder a solicitações de acesso ao seu sistema de identidade do usuário.

1. Crie um terminal HTTPS que receba solicitações do Livefyre e responda com um objeto JSON que contenha os dados do usuário mais recentes.

   >[!NOTE]
   >
   >Esse terminal deve estar acessível. Também é altamente recomendado que ambas as solicitações e respostas sejam enviadas sobre o protocolo HTTPS.

1. Registre o Endpoint com o Studio.
