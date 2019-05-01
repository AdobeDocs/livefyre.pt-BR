---
description: Notas de versão de 18 de janeiro de 2018.
seo-description: Notas de versão de 18 de janeiro de 2018.
seo-title: 18 de janeiro de 2018
solution: Experience Manager
title: 18 de janeiro de 2018
uuid: 8141 f 431-c 154-4 c 8 f-bbcd-b 7 c 712 fe 5 f 7 d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 18 de janeiro de 2018{#january}

Notas de versão de 18 de janeiro de 2018.

## Versão de produção

| **Tipo de edição** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Aplicativos | Corrigido o bug que impedia a renderização correta dos Avatars quando um arquivo jpeg era usado. |
| Bug | Modq | Correção de um bug para clientes S 1 para permitir filtragem por Coleções em modq. |
| Bug | Fluxos | Correção de um erro que quebrava uma regra de fluxo quando o filtro de idioma era definido como &quot;nenhum&quot;. |
| Bug | Fluxos | Correção de um erro que impedia que as regras de fluxo do Youtube fossem salvas. |
| Bug | Fluxos | Corrige um erro em que os usuários podem criar entradas geográficas formatadas incorretamente nas regras de fluxo e salvá-las, o que fazia com que o fluxo falhasse. Agora, os usuários não podem mais salvar tags geográficas formatadas incorretas. |
| Bug | Studio | Correção de um problema que impedia que alguns usuários fizessem logon no Livefyre. |

## Versão do UAT

| **Tipo de edição** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Biblioteca | Correção de erros de segurança. Todas as chamadas de autenticação agora são feitas usando o protocolo HTTPS em vez de HTTP. |
| Aprimoramento | Tags inteligentes | O conteúdo continuado agora é marcado automaticamente pelo Adobe Sensei conforme é salvo em uma pasta ou publicado em um aplicativo. |
| Bug | Fluxos | Correção de um problema em que as regras de fluxo do Instagram não reconheciam caracteres japoneses. |
| Aprimoramento | Fluxos | Os clientes agora podem usar os operadores lógicos (ANY, ALL, NOT) para criar filtros de tag inteligente detalhados em fluxos que curtam conteúdo muito mais preciso. Por exemplo, se eu usar a hashtag # himalyas, selecione mostrar apenas imagens que incluem &quot;neve&quot;. |
| Bug | Studio | Correção de um erro que exibia caracteres especiais em nomes como HTML. |

