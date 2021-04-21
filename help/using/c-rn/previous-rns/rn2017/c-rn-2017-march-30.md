---
description: Notas de versão para 30 de março de 2017.
title: 30 de março de 2017
exl-id: 44c73ff9-8bc1-49c9-b720-aff425e5cd28
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 6%

---

# 30 de março de 2017{#march}

Notas de versão para 30 de março de 2017.

## Versão de produção

| Tipo de problema | Componente | Nota de versão |
|---|---|---|
| Bug | Pesquisa social | Correção de um bug que impedia a publicação de ativos do YouTube salvos na Pesquisa social. |
| Aprimoramento | Sincronização social | Sincronização do Twitter Social obsoleta. |
| Aprimoramento | Storify 2 | Adição de um aprimoramento para exibir a mensagem &quot;Nenhum resultado encontrado&quot; na pesquisa Tópico do Facebook quando nenhum resultado for encontrado. |
| Aprimoramento | Fluxos | Adicionadas Regras de resumo para Regras SAFE na parte inferior de uma página do Twitter Stream. |
| Bug | Fluxos | Adição de um aprimoramento para desativar visivelmente a caixa de seleção &quot;usuário verificado&quot; nas Regras de fluxo do Twitter, quando os autores excluídos são fornecidos. |
| Bug | Fluxos | Correção de um bug que permitia o uso de palavras-chave E e de um filtro de Localização em uma regra do Twitter. |
| Bug | Studio | Correção de um erro que impedia que a &quot;Tag de recurso&quot; fosse salva corretamente quando aplicada. |

## Versão UAT

| Tipo de problema | Componente | Nota de versão |
|---|---|---|
| Bug | Conteúdo do aplicativo | Alteração do comportamento de &quot;Mais informações&quot; de modo que, se houver vários eventos de sinalizador anônimo em um determinado conteúdo, o evento anterior será sempre exibido. |
| Bug | Biblioteca | Correção de um erro que causava falhas intermitentes nas pesquisas da biblioteca com hashtags. |
| Bug | Mapas | Correção de um bug no Maps para oferecer suporte a um grande número de conteúdo em clusters em dispositivos iOS. |
| Aprimoramento | Mosaico | Adição da capacidade de configurar aplicativos Mosaic para clicar em qualquer lugar em um cartão de conteúdo para abrir o modal por tipo de animação `none` no designer e `cardAnimation: 'off'`se instanciado por meio do SDK. |
| Bug | Mosaico | Correção de um erro que permitia que os usuários fizessem alterações nos aplicativos Mosaic no Designer. |
| Aprimoramento | Solicitação de direitos | Adição de um novo status de solicitação de direitos chamado &quot;Falha na solicitação&quot; para realçar quando as mensagens de solicitação de direitos não foram enviadas. |
| Aprimoramento | Configurações | Foi adicionada a capacidade de os clientes criarem Regras de moderação de spam em Configurações. |
| Aprimoramento | Pesquisa social | Correção de um bug que impedia a exibição de publicações VK.com por meio de Pesquisas sociais de URL. |
| Aprimoramento | Pesquisa social | Ao pesquisar conteúdo do Instagram pelo Studio, se a pesquisa for devido a um Token de API do Instagram expirado, a mensagem de erro agora indicará como tal. |
| Bug | Fluxos | Correção de um bug que resultava na exibição falsa de um banner de &quot;O aplicativo não está aceitando novo conteúdo&quot; na parte superior das páginas de Regra de fluxo. |
| Aprimoramento | Fluxos | Modificado o padrão de regras de fluxo recém-criadas para Aplicar regras SAFE quando aplicável. |
| Aprimoramento | Fluxos (anteriormente, preparar regras) | Remoção da opção &quot;Vinhas&quot; somente das regras de fluxo/preparação do Twitter, já que Vinhas agora são exibidas como vídeos do Twitter. |
| Bug | Studio Shell | Correção de um erro para que o Livefyre Studio fosse carregado se https:// fosse explicitamente anexado ao url. |
