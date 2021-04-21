---
description: Notas de versão para a versão de 18 de janeiro de 2018.
title: 18 de janeiro de 2018
exl-id: aaf49dc9-64eb-4354-8bcb-04039fa25f10
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 7%

---

# 18 de janeiro de 2018{#january}

Notas de versão para a versão de 18 de janeiro de 2018.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Aplicativos | Correção de um erro que impedia a renderização correta do Avatars quando um arquivo jpeg era usado. |
| Bug | ModQ | Correção de um bug para clientes S1 para permitir a filtragem por Coleções no ModQ. |
| Bug | Fluxos | Correção de um erro que quebrou uma regra de fluxo quando o filtro de idioma era definido como &quot;nenhum&quot;. |
| Bug | Fluxos | Correção de um erro que impedia que as regras de fluxo do YouTube fossem salvas. |
| Bug | Fluxos | Corrige um erro em que os usuários podiam criar entradas geográficas formatadas incorretamente nas regras de fluxo e salvá-las, o que causava a falha do fluxo. Agora, os usuários não podem mais salvar tags geográficas mal formatadas. |
| Bug | Studio | Correção de um problema que impedia alguns usuários de fazer logon no Livefyre. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Biblioteca | Correção de bug de segurança. Todas as chamadas de autenticação agora são feitas usando o protocolo HTTPS em vez de HTTP. |
| Aprimoramento | Tags inteligentes | O conteúdo transmitido agora é automaticamente marcado de forma inteligente pela Adobe Sensei , pois é salvo em uma pasta ou publicado em um aplicativo. |
| Bug | Fluxos | Correção de um problema em que as regras de fluxo do Instagram não reconheciam caracteres japoneses. |
| Aprimoramento | Fluxos | Os clientes agora podem usar os operadores lógicos ( ANY, ALL, NOT) para criar filtros de tags inteligentes detalhados em fluxos que curam conteúdo muito mais preciso. Por exemplo, se eu usar a hashtag #himalyas eu posso selecionar para mostrar apenas imagens que incluem &quot;montanhas&quot; de &quot;neve&quot;. |
| Bug | Studio | Correção de um erro que mostrava caracteres especiais em nomes como HTML. |
