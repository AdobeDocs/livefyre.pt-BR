---
description: Esta seção descreve como gerar o objeto JSON UserAuth que cria o token de Autenticação de Usuário necessário para fazer logon de usuários em seus aplicativos.
seo-description: Esta seção descreve como gerar o objeto JSON UserAuth que cria o token de Autenticação de Usuário necessário para fazer logon de usuários em seus aplicativos.
seo-title: Token de autenticação do usuário
solution: Experience Manager
title: Token de autenticação do usuário
uuid: 6483debd-453c-4780-b19c-1d8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Token de autenticação do usuário{#user-auth-token}

Esta seção descreve como gerar o objeto JSON UserAuth que cria o token de Autenticação de Usuário necessário para fazer logon de usuários em seus aplicativos.

Esta seção descreve como gerar o objeto JSON UserAuth que cria o token de Autenticação de Usuário necessário para fazer logon de usuários em seus aplicativos.

Para criar o token, use a biblioteca de idiomas preferida para transmitir os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| networkName | String *necessária* | O nome da rede Livefyre (fornecido pela Livefyre). |
| networkKey | String *necessária* | A chave secreta para esta rede específica (fornecida pela Livefyre). |
| userId | String *necessária* | A ID do usuário que faz logon como armazenada no sistema de gerenciamento de usuários (somente caracteres alfanuméricos, traço, sublinhado e pontos são permitidos: [a-zA-Z0-9_-.]). **** Observação: A userId deve ser exclusiva. |
| expira | Número inteiro *necessário* | Quando o token deve expirar agora (em segundos). **** Observação: Esse valor também pode ser passado como flutuante. O token da Web JSON produzido armazenará esse valor na época UNIX. |
| displayName | String *necessária* | Texto para identificar esse usuário na interface do usuário e em comentários. (Número máximo de caracteres: 50.) |

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
>As chaves de rede não são compartilhadas para contas demosite do Livefyre. Você receberá uma chave de rede depois que o Livefyre tiver provisionado um ambiente para você. Esta chave deve ser mantida privada.

