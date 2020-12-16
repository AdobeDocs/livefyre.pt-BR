---
description: Crie a estrutura de solicitação pull para receber e responder solicitações de acesso ao seu sistema de identidade do usuário.
seo-description: Crie a estrutura de solicitação pull para receber e responder solicitações de acesso ao seu sistema de identidade do usuário.
seo-title: Estrutura de solicitação de puxamento
solution: Experience Manager
title: Estrutura de solicitação de puxamento
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# Estrutura de Solicitação de Puxo{#pull-request-structure}

Crie a estrutura de solicitação pull para receber e responder solicitações de acesso ao seu sistema de identidade do usuário.

O Livefyre emite uma solicitação de Puxo para o URL do terminal.

Por exemplo, se o URL do terminal de puxar for:

```
https://example.yoursite.com/some_path/?id={id}
```

a solicitação Livefyre Pull para este terminal será:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

em que `lftoken` é um Token Web JSON assinado com sua chave de rede e **[!UICONTROL {userAuthToken}]** é o token de autenticação do usuário gerado pelo Livefyre.

1. Use `lftoken` para validar se as solicitações do URL Ping for Pull foram enviadas pelo Livefyre e não por um agente mal-intencionado.
1. Para todas as solicitações recebidas:

   * Certifique-se de que a sequência de query `lftoken` esteja presente na solicitação.
   * Use o método `validateLivefyreToken` nas bibliotecas do Livefyre para garantir que `lftoken` foi assinado com sua chave de rede.

   * Se `lftoken` não estiver presente ou falhar na validação, não permita que o terminal responda com as informações do perfil. Em vez disso, responda com um código de status 403 (Proibido) e sem corpo de resposta.

1. `userAuthToken` é gerado pelo  `buildUserAuthToken` método Livefyre para o usuário, com a ID do usuário &quot;system&quot;. Este usuário é o primeiro usuário criado para cada nova rede.
