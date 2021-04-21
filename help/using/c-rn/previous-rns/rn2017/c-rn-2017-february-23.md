---
description: Notas de versão para 23 de fevereiro de 2017.
title: 23 de fevereiro de 2017
exl-id: 3a5708a1-4be6-447f-ae6e-8f5a37171ed7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 7%

---

# 23 de fevereiro de 2017{#february}

Notas de versão para 23 de fevereiro de 2017.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Aprimoramento | Android SDK | O Android SDK foi reorganizado para garantir que os diretórios de implementação de exemplo e referência sejam mais claramente identificáveis pela localização. |
| Aprimoramento | Android SDK | O Android SDK foi modificado para oferecer suporte a uma versão mínima de SDK de 14 (depois de 16). |
| Bug | Aplicativos de conversa | Aprimoramento dos aplicativos de conversa para sempre vincularem aos perfis de usuário, mesmo sem uma integração completa de autenticação. |
| Bug | Mosaico | Correção de um bug que agora disponibiliza todas as imagens do Twitter por HTTPS. |
| Aprimoramento | Pesquisar e fluxos | Adição da capacidade de pesquisar pelo Instagram Places (check-in) na Pesquisa da Instagram da biblioteca e nas Regras de fluxo do Instagram. |
| Bug | Configurações | Correção de um erro que impedia que as contas do Twitter Social fossem salvas. |
| Bug | Pesquisa social | Correção de um erro que impedia o funcionamento correto da opção &quot;Ocultar imagens explícitas&quot;. |
| Aprimoramento | Storify 2 | Aprimoramento do Storify 2 para oferecer suporte a permalinks que abrem um modal (antes, o aplicativo rolava para o local de publicação na página). No Designer do Storify 2, adicionamos uma configuração para alternar entre o comportamento de Rolagem e de Link manual modal. O comportamento do permalink modal será o comportamento padrão. |
| Aprimoramento | Storify 2 | Aprimoramento da integração do Storify 2 Google AMP para produzir um arquivo CSS menor. |
| Aprimoramento | Fluxos | Correção de um bug com regras do Facebook que fazia com que o conteúdo fosse recebido com metadados incompletos. |
| Bug | Fluxos | Conteúdo aprimorado (imagens e vídeos) das Regras de fluxo de email a serem disponibilizadas via HTTPS. |
| Bug | Fluxos | Adição de um rótulo para o Valor do Raio da compilação em mapas nas Regras de fluxo do Twitter. |
| Bug | Fluxos | Correção de um bug com Regras de fluxo de página do Facebook e Facebook para inserir publicações com vários anexos de mídia adequadamente. |
| Aprimoramento | Fluxos | Adição de um novo recurso para permitir que os usuários optem por aplicar ou desativar regras SAFE por regra de fluxo. |
| Aprimoramento | Studio | Correção de um erro que fazia com que o conteúdo não fosse publicado ou salvo corretamente se já existisse. |
| Bug | Studio | Correção de um erro que fazia com que vários &amp;&#39;s fossem anexados ao url ao usar filtros no Studio. |
| Bug | Studio | Correção de um erro que impedia que determinadas caixas de seleção nos filtros do Studio fossem desmarcadas. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Aplicativos | Correção de um erro para mostrar conteúdo em modais de mídia com as taxas de aspecto corretas. |
| Bug | Mural de mídia | Correção de um erro que fazia com que os Murais de mídia não fossem renderizados se caracteres estrangeiros específicos fossem incluídos. |
| Bug | Pesquisar | Correção de um erro que fazia com que as páginas fossem carregadas incorretamente ao paginar os resultados de pesquisa com &quot;Imagens explícitas da ocultação&quot; ativadas. |
| Aprimoramento | Studio | Aumento do tempo da sessão antes de expirar as sessões de logon do Usuário do Studio . Depois que uma sessão do Studio expirar, o usuário será redirecionado para fazer logon novamente. |
| Bug | Studio | Correção de um bug que, às vezes, impedia os usuários de salvar as credenciais do Instagram. |
| Bug | Studio | Correção de um erro que impedia que a &quot;Tag de recurso&quot; fosse salva corretamente quando aplicada. |
