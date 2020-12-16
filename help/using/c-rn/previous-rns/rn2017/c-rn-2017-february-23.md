---
description: Notas de versão para a versão de 23 de fevereiro de 2017.
seo-description: Notas de versão para a versão de 23 de fevereiro de 2017.
seo-title: 23 de fevereiro de 2017
title: 23 de fevereiro de 2017
uuid: 9b08acf4-15e9-43b7-8abc-c0d720b156e6
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 8%

---


# 23 de fevereiro de 2017{#february}

Notas de versão para a versão de 23 de fevereiro de 2017.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Android SDK | Reorganizou o Android SDK para garantir que os diretórios de implementação de exemplo e referência sejam mais claramente identificáveis pela localização. |
| Aprimoramento | Android SDK | O Android SDK foi modificado para oferecer suporte a uma versão mínima do SDK de 14 (abaixo de 16). |
| Bug | Aplicativos de conversa | Aplicativos de conversa aprimorados para sempre se vincularem aos perfis do usuário, mesmo sem uma integração total de autenticação. |
| Bug | Mosaico | Correção de um bug que agora serve todas as imagens do Twitter via HTTPS. |
| Aprimoramento | Pesquisar e fluxos | Foi adicionada a capacidade de pesquisar por Instagram Places (check-in) nas Regras de pesquisa do Instagram da biblioteca e do Instagram Stream. |
| Bug | Configurações | Correção de um erro que impedia a gravação de Contas do Twitter Social. |
| Bug | Pesquisa social | Correção de um erro que impedia o funcionamento correto da opção &quot;Ocultar imagens explícitas&quot;. |
| Aprimoramento | Storify 2 | Aprimorado o Storify 2 para oferecer suporte a permissões de abertura de um modal (antes o aplicativo rolava para o local de publicação na página). No Designer do Storify 2, adicionamos uma configuração para alternar entre o comportamento de Rolagem e o de permalink Modal. O comportamento padrão do permalink modal será o comportamento padrão. |
| Aprimoramento | Storify 2 | Aprimorada a integração do Storify 2 com o Google AMP para produzir um arquivo CSS menor. |
| Aprimoramento | Fluxos | Correção de um bug com regras do Facebook que fazia com que o conteúdo fosse extraído com metadados incompletos. |
| Bug | Fluxos | Conteúdo aprimorado (imagens e vídeos) das Regras de fluxo de e-mail para estar disponível via HTTPS. |
| Bug | Fluxos | Adição de um rótulo para o Valor de Raio de Milha em mapas nas Regras de Fluxo do Twitter. |
| Bug | Fluxos | Correção de um bug com Regras de fluxo de página do Facebook e Facebook para obter postagens com vários anexos de mídia adequadamente. |
| Aprimoramento | Fluxos | Adicionado um novo recurso para permitir que os usuários optem por aplicar ou desativar regras SAFE por regra de fluxo. |
| Aprimoramento | Studio | Correção de um bug que fazia com que o conteúdo não fosse publicado ou salvo corretamente se já existisse. |
| Bug | Studio | Correção de um bug que fazia com que vários &amp;’s não fossem anexados ao url ao usar filtros no Studio. |
| Bug | Studio | Correção de um erro que impedia que determinadas caixas de seleção em filtros do Studio permitissem a desseleção. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Aplicativos | Correção de um bug que exibia conteúdo em módulos de mídia com as proporções corretas. |
| Bug | Mídia | Correção de um bug que fazia com que o Media Walls não fosse renderizado se caracteres estrangeiros específicos fossem incluídos. |
| Bug | Pesquisar | Correção de um bug que fazia com que as páginas fossem carregadas incorretamente ao paginar pelos resultados da pesquisa com &quot;Ocultar imagens explícitas&quot; ativado. |
| Aprimoramento | Studio | Aumento do tempo de sessão antes de expirar as sessões de logon do usuário do Studio. Quando uma sessão do Studio expirar, o usuário será redirecionado para fazer logon novamente. |
| Bug | Studio | Correção de um bug que às vezes impedia os usuários de salvar as credenciais do Instagram. |
| Bug | Studio | Correção de um erro que impedia que a &quot;Tag de recurso&quot; fosse salva corretamente quando aplicada. |

