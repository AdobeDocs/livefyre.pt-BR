---
description: Crie a estrutura de solicitação de pull para receber e responder solicitações de acesso ao seu sistema de identidade do usuário.
title: Estrutura de solicitação de pull
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Estrutura de solicitação de pull{#pull-request-structure}

Crie a estrutura de solicitação de pull para receber e responder solicitações de acesso ao seu sistema de identidade do usuário.

Livefyre emite uma solicitação de pull para o URL do terminal.

Por exemplo, se o URL do terminal Pull for:

```
https://example.yoursite.com/some_path/?id={id}
```

a solicitação Livefyre Pull para esse endpoint será:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

onde `lftoken` é um Token Web JSON assinado com sua chave de rede e **[!UICONTROL {userAuthToken}]** é o token de autenticação de usuário gerado pelo Livefyre.

1. Use `lftoken` para validar se as solicitações para o URL de Ping foram enviadas pelo Livefyre e não por um agente mal-intencionado.
1. Para todas as solicitações recebidas:

   * Verifique se a sequência de consulta `lftoken` está presente na solicitação.
   * Use o método `validateLivefyreToken` nas bibliotecas do Livefyre para garantir que `lftoken` foi assinado com sua Chave de rede.

   * Se `lftoken` não estiver presente ou falhar na validação, não permita que o terminal responda com as informações do perfil. Em vez disso, responda com um código de status 403 (Proibido) e nenhum corpo de resposta.

1. `userAuthToken` é gerada pelo  `buildUserAuthToken` método Livefyre para o usuário, com a ID do usuário &quot;system&quot;. Este usuário é o primeiro usuário criado para cada nova rede.
