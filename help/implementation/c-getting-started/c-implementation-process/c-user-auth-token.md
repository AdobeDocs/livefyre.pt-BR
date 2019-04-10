---
description: Esta seção descreve como gerar o objeto userauth JSON que cria o token
  de Autenticação do usuário necessário para registrar usuários em seus aplicativos.
seo-description: Esta seção descreve como gerar o objeto userauth JSON que cria o
  token de Autenticação do usuário necessário para registrar usuários em seus aplicativos.
seo-title: Token de autenticação do usuário
solution: Experience Manager
title: Token de autenticação do usuário
uuid: 6483 debd -453 c -4780-b 19 c -1 d 8041693617
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Token de autenticação do usuário{#user-auth-token}

Esta seção descreve como gerar o objeto userauth JSON que cria o token de Autenticação do usuário necessário para registrar usuários em seus aplicativos.

Esta seção descreve como gerar o objeto userauth JSON que cria o token de Autenticação do usuário necessário para registrar usuários em seus aplicativos.

Para criar o token, use a biblioteca de idiomas preferida para passar os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| Networkname | String *obrigatória* | O nome da rede Livefyre (fornecido pelo Livefyre). |
| Networkkey | String *obrigatória* | A chave secreta para esta rede específica (fornecida pelo Livefyre). |
| Userid | String *obrigatória* | A ID do usuário que faz logon como armazenado no sistema de gerenciamento de usuários (somente alfanumérico, traço, sublinhado e caracteres de pontos é permitida: [a-zA-Z 0-9_-.]). **Observação:** O userid deve ser único. |
| expira | Número inteiro *obrigatório* | Quando o token deve expirar a partir de agora (em segundos). **Observação:** Esse valor também pode ser passado como flutuante. O token da Web JSON produzido armazenará esse valor na hora de época UNIX. |
| Displayname | String *obrigatória* | Texto para identificar esse usuário na interface do usuário e nos comentários. (Número máximo de caracteres: 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## Nodejs {#section_c42_mjz_1cb}

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
>As chaves de rede não são compartilhadas para contas de demosite do Livefyre. Você receberá uma chave de rede uma vez que o Livefyre provisionou um ambiente para você. Essa chave deve ser mantida privada.

