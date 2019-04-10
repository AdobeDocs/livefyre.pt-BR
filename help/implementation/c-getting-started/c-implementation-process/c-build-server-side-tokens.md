---
description: Um guia para criar tokens collectionmeta e auth.
seo-description: Um guia para criar tokens collectionmeta e auth.
seo-title: Criar tokens do lado do servidor
solution: Experience Manager
title: Criar tokens do lado do servidor
uuid: 8313 f 26 e -5 ceb -414 e-a 61 a -480 bb 7 a 8 ba 66
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Criar tokens do lado do servidor{#build-server-side-tokens}

Um guia para criar tokens collectionmeta e auth.

Criar os tokens que o Livefyre usa para validar solicitações garante que apenas você possa fazer atualizações na sua rede do Livefyre.

## Collectionmeta token

Saiba como criar um token para criar novas conversas existentes e exibir conversas existentes.

## Token de autenticação

Saiba como criar um token para autenticação de usuários, uma etapa necessária no processo de integração se você não estiver usando Janrain Capture para gerenciamento de usuários.

## Token de autenticação do usuário {#section_l5l_hwt_bbb}

Esta seção descreve como gerar o objeto userauth JSON que cria o token de Autenticação do usuário necessário para registrar usuários em seus aplicativos.

Para criar o token, use a biblioteca de idiomas preferida para passar os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| Networkname | String *obrigatória* | O nome da rede Livefyre (fornecido pelo Livefyre). |
| Networkkey | String *obrigatória* | A chave secreta para esta rede específica (fornecida pelo Livefyre). |
| Userid | String *obrigatória* | A ID do usuário que faz logon como armazenado no sistema de gerenciamento de usuários (somente alfanumérico, traço, sublinhado e caracteres de pontos é permitida: `[a-zA-Z0-9_-.]`). **Observação:** O userid deve ser único. |
| expira | Número inteiro *obrigatório* | Quando o token deve expirar a partir de agora (em segundos). **Observação:** Esse valor também pode ser passado como flutuante. O token da Web JSON produzido armazenará esse valor na hora de época UNIX. |
| Displayname | String *obrigatória* | Texto para identificar esse usuário na interface do usuário e nos comentários. (Número máximo de caracteres: 50.) |

