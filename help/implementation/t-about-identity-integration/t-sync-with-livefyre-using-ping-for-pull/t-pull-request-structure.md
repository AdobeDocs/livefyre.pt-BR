---
description: Crie a estrutura de solicitação de extração para receber e responder a solicitações de acesso ao seu sistema de identidade do usuário.
seo-description: Crie a estrutura de solicitação de extração para receber e responder a solicitações de acesso ao seu sistema de identidade do usuário.
seo-title: Estrutura de solicitação de extração
solution: Experience Manager
title: Estrutura de solicitação de extração
uuid: bf 6 b 9 e 45-d 08 a -48 e 6-acc 6-e 4 fa 56428 d 25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

---


# Estrutura de solicitação de extração{#pull-request-structure}

Crie a estrutura de solicitação de extração para receber e responder a solicitações de acesso ao seu sistema de identidade do usuário.

O Livefyre emite uma solicitação extraída para o URL de terminal.

Por exemplo, se o URL de ponto de extremidade puxado for:

```
https://example.yoursite.com/some_path/?id={id}
```

a solicitação do Livefyre Pull para este endpoint será:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

onde `lftoken` é um token da Web JSON assinado com sua chave de rede e **[!UICONTROL {userAuthToken}]** é o token de autenticação do usuário gerado pelo Livefyre.

1. Use `lftoken` para validar que as solicitações para o Ping para URL de extração foram enviadas pelo Livefyre e não por um agente mal-intencionado.
1. Para todas as solicitações de entrada:

   * Verifique se a string `lftoken` de consulta está presente na solicitação.
   * Use `validateLivefyreToken` o método nas bibliotecas do Livefyre para garantir `lftoken` que foi assinado com sua chave de rede.

   * Se `lftoken` não estiver presente, ou falhar na validação, não permita que o terminal responda com as informações do perfil. Em vez disso, responda com um código de status 403 (Proibido) e sem corpo de resposta.

1. `userAuthToken` é gerado pelo método Livefyre `buildUserAuthToken` para o usuário, com a ID do usuário «system». Esse usuário é o primeiro usuário criado para cada nova rede.
