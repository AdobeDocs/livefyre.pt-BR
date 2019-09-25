---
description: Notas de versão para a versão de 8 de março de 2018.
seo-description: Notas de versão para a versão de 8 de março de 2018.
seo-title: 8 de março de 2018
solution: Experience Manager
title: 8 de março de 2018
uuid: 4ed67147-0837-4d5e-8e99-532a4278bcce
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 8, 2018{#march}

Notas de versão para a versão de 8 de março de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* **Excluindo aplicativos. **Adicionada a capacidade de excluir aplicativos no Studio para que os usuários possam gerenciar melhor a lista de aplicativos. A exclusão de um aplicativo o remove da tabela, mas não remove o aplicativo do site. O aplicativo continuará recebendo conteúdo de um fluxo se estiver configurado para isso.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Pesquisas | As pesquisas foram alteradas para usar HTTPS exclusivamente. Anteriormente, as pesquisas ainda podiam ser usadas com HTTP. |
| Bug | Studio | Correção de um problema que fazia com que a janela modal que exibe anúncios quando você faz logon no Studio fosse exibida em telas de baixa resolução. |

## Versão UAT

| Tipo de problema | Componente | Nota de versão |
|--- |--- |--- |
| Aprimoramento | Película fotográfica | Atualizados os seguintes recursos de acessibilidade para Película fotográfica: <br><ul><li>Setas para a esquerda/direita corrigidas de &lt;div&gt; para &lt;botão&gt; </li><li>O elemento de imagem de visualização foi alterado de um rótulo ARIA menos descritivo de "Abrir foto anexada" para um rótulo que lê o nome da plataforma e o texto da postagem.</li></ul> |
| Bug | Mídia | Correção de um problema no Media Wall em que as tags não eram clicáveis quando uma postagem do Instagram era adicionada de uma regra de fluxo. |
| Aprimoramento | Mídia | Melhoria na acessibilidade do Media Wall das seguintes maneiras: <br><ul><li>A abertura e o fechamento de módulos por meio de comandos do teclado não alterarão mais o foco de volta para a parte superior da página. Em vez disso, o foco permanece no último foco do elemento antes do pop-up modal.</li><li>O botão Carregar mais pode ser tabulado e acionado usando a tecla Enter do teclado.</li></ul> |
| Bug | Gerenciamento de direitos | Correção de um erro em que não era possível visualizar o modal da solicitação de direitos depois que os direitos de um ativo do Instagram eram concedidos. |

