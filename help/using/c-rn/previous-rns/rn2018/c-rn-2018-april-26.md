---
description: Notas de versão para a versão de 26 de abril de 2018.
seo-description: Notas de versão para a versão de 26 de abril de 2018.
seo-title: 26 de abril de 2018
solution: Experience Manager
title: 26 de abril de 2018
uuid: a84ebe5c-40d5-43b5-a300-3e041ab22046
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# April 26, 2018{#april}

Notas de versão para a versão de 26 de abril de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* Adicionado um novo recurso que permite aos clientes configurar um número específico de colunas para um Mídia. O número de colunas escolhidas forçará o Mural de Mídia para esse número de colunas, independentemente do tamanho. Caso contrário, o número de colunas do Mídia padrão será "auto", onde as colunas se ajustarão a um número que otimize o Mídia para o tamanho da tela.
* No Media Wall Designer agora há uma alternância que permite desativar a animação automática do Media Wall que ocorre quando uma página com um Media Wall é carregada.
* Agora você pode escolher o limite de confiança para tags inteligentes em fluxos. A definição da pontuação de precisão (0-100) para tags permite controlar a precisão dos ativos que estamos recuperando.
* Recomendações de moderação adicionadas. O Livefyre agora verifica todas as publicações em aplicativos de comentários e prevê se você a lixará ou não com base nos dados históricos e no aprendizado de máquina. Essas recomendações são exibidas no ModQ.
   * Os usuários podem desativar as recomendações de moderação, que permitem que os usuários filtrem o ModQ pelo conteúdo que Livefyre acha que você vai jogar lixo.
   * Adicionada a capacidade de filtrar ModQ pela tag de recomendação de moderação, Lixeira.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Gerenciamento de direitos | Correção de um problema em que as solicitações de direitos não funcionavam para os Ativos depois de encontrá-las em uma Pesquisa Social. |
| Aprimoramento | Fluxos | Atualização do mecanismo de transmissão que permite que o conteúdo seja transmitido do Facebook para atender a uma alteração de back-end criada pelo Facebook. |
| Bug | Comércio UGC | Correção de um problema em que o botão "Loja" CTA não era exibido em um aplicativo Mosaico ou Película fotográfica ou em um modal de produtos ao passar o mouse sobre um cartão com um produto quando o botão CTA estava ativado. |
| Aprimoramento | Comércio UGC | Corrigido um problema no qual o sinalizador de Comércio UGC estava definido como "desligado" por padrão, em vez de "ligado". |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Biblioteca/pesquisa | Correção de um problema no qual os vídeos não eram carregados corretamente. |
| Aprimoramento | Studio | Foi adicionada a capacidade de ver as palavras sugeridas ao digitar os nomes das tags. |

