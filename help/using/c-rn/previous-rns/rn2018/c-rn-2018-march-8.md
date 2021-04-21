---
description: Notas de versão de 8 de março de 2018.
title: 8 de março de 2018
exl-id: 46d4a425-17e0-48a2-a596-5cc7163f9edd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 5%

---

# 8 de março de 2018{#march}

Notas de versão de 8 de março de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* **Excluindo aplicativos. **Adição da capacidade de excluir aplicativos no Studio para que os usuários possam gerenciar melhor a lista de aplicativos. Excluir um aplicativo o remove da tabela, mas não remove o aplicativo do site. O aplicativo continuará recebendo conteúdo de um fluxo se estiver configurado para isso.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Pesquisas | Pesquisa alterada para usar exclusivamente HTTPS. Anteriormente, as Pesquisas ainda tinham permissão para serem usadas com HTTP. |
| Bug | Studio | Correção de um problema que fazia com que a janela modal que exibia anúncios quando você faz logon no Studio fosse exibida em telas de baixa resolução. |

## Versão UAT

| Tipo de problema | Componente | Nota de versão |
|--- |--- |--- |
| Aprimoramento | Tira | Atualização dos seguintes recursos de acessibilidade para a Tira de filme: <br><ul><li>Setas da esquerda/direita corrigidas de &lt;div> para &lt;botão> </li><li>Visualize o elemento de imagem alterado de um rótulo ARIA menos descritivo, &quot;Abrir foto anexada&quot;, para um rótulo que lê o nome da plataforma e o texto da publicação.</li></ul> |
| Bug | Mural de mídia | Correção de um problema no Mural de mídia em que as tags não eram clicáveis quando uma publicação do Instagram era adicionada de uma regra de fluxo. |
| Aprimoramento | Mural de mídia | Melhoria na acessibilidade do mural de mídia das seguintes maneiras: <br><ul><li>Abrir e fechar modais por meio de comandos do teclado não mudará mais o foco de volta para o topo da página. Em vez disso, o foco permanece no elemento focado pela última vez antes do pop-up modal.</li><li>O botão Carregar mais pode ser tabulado e acionado usando a tecla Enter do teclado.</li></ul> |
| Bug | Rights Management | Correção de um erro em que não era possível visualizar o modal da solicitação de direitos depois que os direitos de um ativo do Instagram eram concedidos. |
