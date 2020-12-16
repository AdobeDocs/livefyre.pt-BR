---
description: Notas de versão para a versão de 18 de janeiro de 2018.
seo-description: Notas de versão para a versão de 18 de janeiro de 2018.
seo-title: 18 de janeiro de 2018
solution: Experience Manager
title: 18 de janeiro de 2018
uuid: 8141f431-c154-4c8f-bbcd-b7c712fe5f7d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 7%

---


# 18 de janeiro de 2018{#january}

Notas de versão para a versão de 18 de janeiro de 2018.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Aplicativos | Correção de um bug que impedia a renderização correta do Avatars quando um arquivo jpeg estava sendo usado. |
| Bug | ModQ | Correção de um bug para clientes S1 para permitir a filtragem por Coleções no ModQ. |
| Bug | Fluxos | Correção de um erro que quebrou uma regra de fluxo quando o filtro de idioma era definido como &quot;nenhum&quot;. |
| Bug | Fluxos | Correção de um bug que impedia que regras de fluxo do YouTube fossem salvas. |
| Bug | Fluxos | Corrige um erro no qual os usuários podem criar entradas geográficas formatadas incorretamente nas regras de fluxo e salvá-las, o que resultaria em falha do fluxo. Agora, os usuários não podem mais salvar tags geográficas mal formatadas. |
| Bug | Studio | Corrigido um problema que impedia que alguns usuários fizessem logon no Livefyre. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Biblioteca | Correção de erros de segurança. Todas as chamadas de autenticação agora são feitas usando o protocolo HTTPS em vez de HTTP. |
| Aprimoramento | Tags inteligentes | O conteúdo em sequência agora é automaticamente marcado de forma inteligente pela Adobe Sensei, pois é salvo em uma pasta ou publicado em um aplicativo. |
| Bug | Fluxos | Corrigido um problema no qual as regras de fluxo do Instagram não reconheciam caracteres japoneses. |
| Aprimoramento | Fluxos | Os clientes agora podem usar os operadores lógicos ( ANY, ALL, NOT) para criar filtros detalhados de tags inteligentes em fluxos que gerenciam conteúdo muito mais preciso. Por exemplo, se eu usar a hashtag #himalyas, posso selecionar para mostrar apenas imagens que incluem &quot;montanhas&quot; com &quot;neve&quot;. |
| Bug | Studio | Correção de um erro que mostrava caracteres especiais em nomes como HTML. |

