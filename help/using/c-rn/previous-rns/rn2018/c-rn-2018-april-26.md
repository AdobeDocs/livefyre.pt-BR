---
description: Notas de versão da versão de April 6 de abril de 26 18.
seo-description: Notas de versão da versão de April 6 de abril de 26 18.
seo-title: 26 de abril de 2018
solution: Experience Manager
title: 26 de abril de 2018
uuid: a 84 ebe 5 c -40 d 5-43 b 5-a 300-3 e 041 ab 22046
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# April 6 de abril de 26 18{#april}

Notas de versão da versão de April 6 de abril de 26 18.

## Novos recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* Adicionado um novo recurso que permite aos clientes configurar um número específico de colunas para um Mural de mídia. O número de colunas escolhidas forçará o mural de mídia nesse número de colunas, independentemente do tamanho. Caso contrário, o número de colunas de mural de mídia assumirá como padrão &quot;auto&quot; em que as colunas se ajustam a um número que otimiza o Media Wall para o tamanho da tela.
* No Designer de mural de mídia, há agora uma alternância que permite desativar a animação automática de Firewall que ocorre quando uma página com um mural de mídia é carregada.
* Agora é possível escolher o limite de confiança para tags inteligentes em fluxos. Definir a pontuação de precisão (0-100) para tags permite controlar a precisão dos ativos que estamos recuperando.
* Recomendações de moderação adicionadas. O Livefyre agora verifica todas as postagens em comentários e prevê se você vai lixeira ou não com base em dados históricos e aprendizado de máquina. Essas recomendações aparecem em modq.
   * Os usuários podem desativar as recomendações de moderação, que permitem que os usuários filtrem modq pelo conteúdo que o Livefyre acha que você vai lixeira.
   * Adição da capacidade de filtrar modq pela tag de recomendação de moderação, Lixeira.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de edição** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Gerenciamento de direitos | Correção de um problema em que as solicitações de direitos não funcionavam em Ativos depois de encontrá-las em uma Pesquisa Social. |
| Aprimoramento | Fluxos | Atualização do mecanismo de transmissão que permite que o conteúdo streaming do Facebook cumpra uma alteração de back-end criada pelo Facebook. |
| Bug | Comércio UGC | Correção de um problema em que o botão «Loja» CTA não era exibido em um aplicativo Mosaico ou Película fotográfica ou em um modal de produtos ao passar o mouse sobre um cartão com um produto quando o botão CTA estava ativado. |
| Aprimoramento | Comércio UGC | Correção de um problema em que o sinalizador de Comércio UGC era definido como &quot;desligado&quot; por padrão, em vez de &quot;ativado&quot;. |

## Versão do UAT

| **Tipo de edição** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Biblioteca/Pesquisa | Correção de um problema que fazia com que vídeos não fossem carregados corretamente. |
| Aprimoramento | Studio | Foi adicionada a capacidade de visualizar as palavras sugeridas ao digitar em nomes de tag. |

