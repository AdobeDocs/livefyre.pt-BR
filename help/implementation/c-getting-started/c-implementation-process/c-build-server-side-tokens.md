---
description: Um guia para criar tokens collectionMeta e auth.
seo-description: Um guia para criar tokens collectionMeta e auth.
seo-title: Criar tokens do lado do servidor
solution: Experience Manager
title: Criar tokens do lado do servidor
uuid: 8313f26e-5ceb-414e-a61a-480bb7a8ba66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Criar tokens do lado do servidor{#build-server-side-tokens}

Um guia para criar tokens collectionMeta e auth.

A criação dos tokens que o Livefyre usa para validar solicitações garante que somente você possa fazer atualizações na rede do Livefyre.

## CollectionMeta Token

Saiba como criar um token para criar conversas novas e exibir conversas existentes.

## Token de autenticação

Saiba como criar um token para autenticação de usuários, uma etapa necessária no processo de integração se você não estiver usando o Janrain Capture para gerenciamento de usuários.

## Token de autenticação do usuário {#section_l5l_hwt_bbb}

Esta seção descreve como gerar o objeto JSON UserAuth que cria o token de Autenticação de Usuário necessário para fazer logon de usuários em seus aplicativos.

Para criar o token, use a biblioteca de idiomas preferida para transmitir os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| networkName | String *necessária* | O nome da rede Livefyre (fornecido pela Livefyre). |
| networkKey | String *necessária* | A chave secreta para esta rede específica (fornecida pela Livefyre). |
| userId | String *necessária* | A ID do usuário que faz logon como armazenada no sistema de gerenciamento de usuários (somente caracteres alfanuméricos, traço, sublinhado e pontos são permitidos: `[a-zA-Z0-9_-.]`). **** Observação: A userId deve ser exclusiva. |
| expira | Número inteiro *necessário* | Quando o token deve expirar agora (em segundos). **** Observação: Esse valor também pode ser passado como flutuante. O token da Web JSON produzido armazenará esse valor na época UNIX. |
| displayName | String *necessária* | Texto para identificar esse usuário na interface do usuário e em comentários. (Número máximo de caracteres: 50.) |

