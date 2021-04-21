---
description: Descreve as opções para adicionar autenticação de usuário aos aplicativos Livefyre, incluindo o Janrain Capture ou seu próprio serviço de identidade.
title: Integração de identidade
exl-id: a3b849fc-0182-4fed-94b5-6d7199fc4e44
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Integração de identidade{#identity-integration}

Descreve as opções para adicionar autenticação de usuário aos aplicativos Livefyre, incluindo o Janrain Capture ou seu próprio serviço de identidade.

## Integração de identidade {#t_about_identity_integration}

Descreve as opções para adicionar autenticação de usuário aos aplicativos Livefyre, incluindo o Janrain Capture ou seu próprio serviço de identidade.

Os aplicativos Livefyre incluem uma função interativa avançada, como publicar um comentário, escrever uma revisão ou curtir o conteúdo. Para que seus usuários interajam com os aplicativos do Livefyre, é necessário integrar o Livefyre a um serviço de identidade usando a Auth Livefyre.js.

O Livefyre.js Auth fornece autenticação centralizada para todos os aplicativos Livefyre no seu site e o coloca no controle de exatamente como os usuários devem fazer logon e se registrar. Adicione Auth globalmente ao modelo do seu site e use-o em todas as páginas, ou adicione-o uma vez por página, e quando os usuários assinaram o Livefyre JS Auth, ele transmitirá automaticamente as informações do usuário para todos os aplicativos na página.

Quer você tenha criado um serviço de identidade personalizado ou esteja usando um serviço de identidade de terceiros, como o Janrain Capture, esta seção aborda tudo o que você precisa saber para integrar.
