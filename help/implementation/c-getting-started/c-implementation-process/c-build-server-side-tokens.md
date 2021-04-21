---
description: Um guia para criar tokens de coletaMeta e autenticação.
title: Criar tokens do lado do servidor
exl-id: f709b79e-9236-443e-b862-c7d281815d91
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# Criar tokens do lado do servidor{#build-server-side-tokens}

Um guia para criar tokens de coletaMeta e autenticação.

A criação dos tokens que o Livefyre usa para validar solicitações garante que somente você possa fazer atualizações na sua rede do Livefyre.

## CollectionMeta Token

Saiba como criar um token para criar conversas novas e exibir conversas existentes.

## Token de autenticação

Saiba como criar um token para autenticação de usuários, uma etapa necessária no processo de integração se você não estiver usando o Janrain Capture para gerenciamento de usuários.

## Token de autenticação do usuário {#section_l5l_hwt_bbb}

Esta seção descreve como gerar o objeto JSON UserAuth que cria o token de autenticação de usuário necessário para registrar usuários em seus aplicativos.

Para criar o token, use a biblioteca de idioma preferencial para transmitir os seguintes parâmetros:

| Parâmetro | Tipo | Descrição |
|---|---|---|
| networkName | Sequência *necessária* | O nome da rede Livefyre (fornecido pela Livefyre). |
| networkKey | Sequência *necessária* | A chave secreta para esta rede específica (fornecida pela Livefyre). |
| userId | Sequência *necessária* | A ID do usuário que faz logon como armazenada no sistema de gerenciamento de usuários (somente caracteres alfanuméricos, traço, sublinhado e pontos são permitidos: `[a-zA-Z0-9_-.]`). **Observação:** o userId deve ser exclusivo. |
| expira | Número inteiro *necessário* | Quando o token deve expirar de agora (em segundos). **Observação:** esse valor também pode ser passado como um flutuante. O token da Web JSON produzido armazenará esse valor em época UNIX. |
| displayName | Sequência *necessária* | Texto para identificar esse usuário na interface do usuário e em comentários. (Número máximo de caracteres: 50.) |
