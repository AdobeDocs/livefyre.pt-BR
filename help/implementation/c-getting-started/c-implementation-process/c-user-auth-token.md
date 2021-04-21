---
description: Esta seção descreve como gerar o objeto JSON UserAuth que cria o token de autenticação de usuário necessário para registrar usuários em seus aplicativos.
title: Token de autenticação do usuário
exl-id: 564144dd-6db4-447b-80ac-b743ecac833d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 2%

---

# Token de autenticação do usuário{#user-auth-token}

Esta seção descreve como gerar o objeto JSON UserAuth que cria o token de autenticação de usuário necessário para registrar usuários em seus aplicativos.

Esta seção descreve como gerar o objeto JSON UserAuth que cria o token de autenticação de usuário necessário para registrar usuários em seus aplicativos.

Para criar o token, use a biblioteca de idioma preferencial para transmitir os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| networkName | Sequência *necessária* | O nome da rede Livefyre (fornecido pela Livefyre). |
| networkKey | Sequência *necessária* | A chave secreta para esta rede específica (fornecida pela Livefyre). |
| userId | Sequência *necessária* | A ID do usuário que faz logon como armazenada no sistema de gerenciamento de usuários (somente caracteres alfanuméricos, traço, sublinhado e pontos são permitidos: [a-zA-Z0-9_-.]). **Observação:** o userId deve ser exclusivo. |
| expira | Número inteiro *necessário* | Quando o token deve expirar de agora (em segundos). **Observação:** esse valor também pode ser passado como um flutuante. O token da Web JSON produzido armazenará esse valor em época UNIX. |
| displayName | Sequência *necessária* | Texto para identificar esse usuário na interface do usuário e em comentários. (Número máximo de caracteres: 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>As chaves de rede não são compartilhadas para contas demositadas do Livefyre. Você receberá uma chave de rede depois que o Livefyre tiver provisionado um ambiente para você. Essa chave deve ser mantida privada.
