---
description: Notas de versão de 26 de abril de 2018.
title: 26 de abril de 2018
exl-id: af0ee64d-d60c-4b21-a628-08848313781c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 4%

---

# 26 de abril de 2018{#april}

Notas de versão de 26 de abril de 2018.

## Novos Recursos {#section_syx_mdt_wcb}

Os seguintes recursos são novos na versão de produção desta versão:

* Adição de um novo recurso que permite que os clientes configurem um número específico de colunas para um Mural de mídia. O número de colunas que você escolher forçará o Mural de mídia a esse número de colunas, independentemente do tamanho. Caso contrário, o padrão do número de colunas do Mural de mídia é &quot;auto&quot;, onde as colunas se ajustam a um número que otimiza o Mural de mídia para o tamanho da tela.
* No Media Wall Designer, agora há um botão que permite desativar a animação automática de Mídia que ocorre quando uma página com um Mural de mídia é carregada.
* Agora você pode escolher o limite de confiança para tags inteligentes em fluxos. Definir a pontuação de precisão (0-100) para tags permite controlar a precisão dos ativos que estamos recuperando.
* Recomendações de moderação adicionadas. Agora, Livefyre verifica todas as publicações em comentários de aplicativos e prevê se você irá enviá-las para a lixeira ou não com base em dados históricos e no aprendizado de máquina. Essas recomendações são exibidas no ModQ.
   * Os usuários podem desativar as recomendações de moderação, o que permite que os usuários filtrem o ModQ de acordo com o conteúdo que Livefyre acha que você vai enviar para a lixeira.
   * Adicionada a capacidade de filtrar ModQ pela tag de recomendação de moderação, Lixeira.

## Problemas {#section_ehw_ndt_wcb}

Os problemas nas tabelas a seguir foram resolvidos nesta versão.

## Versão de produção

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Rights Management | Correção de um problema em que as solicitações de direitos não funcionavam para o Assets depois de encontrá-las em uma Pesquisa social. |
| Aprimoramento | Fluxos | Atualização do mecanismo de transmissão que permite que o conteúdo faça stream do Facebook para estar em conformidade com uma alteração de back-end criada pelo Facebook. |
| Bug | Comércio UGC | Correção de um problema em que o botão &quot;Loja&quot; do CTA não era exibido em um aplicativo Mosaic ou Filmstrip ou em um modal de produtos ao passar o mouse sobre um cartão com um produto quando o botão CTA era ativado. |
| Aprimoramento | Comércio UGC | Correção de um problema em que o sinalizador de Comércio UGC era definido como &quot;desativado&quot; por padrão, em vez de &quot;ativado&quot;. |

## Versão UAT

| **Tipo de problema** | **Componente** | **Nota de versão** |
|---|---|---|
| Bug | Biblioteca/Pesquisa | Correção de um problema que fazia com que os vídeos não fossem carregados corretamente. |
| Aprimoramento | Studio | Foi adicionada a capacidade de ver as palavras sugeridas ao digitar os nomes das tags. |
