---
description: Notas de versão para a versão de 30 de março de 2017.
seo-description: Notas de versão para a versão de 30 de março de 2017.
seo-title: 30 de março de 2017
title: 30 de março de 2017
uuid: 2adf04a9-6c52-4fa1-a0c9-b2d3886305e9
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 30, 2017{#march}

Notas de versão para a versão de 30 de março de 2017.

## Versão de produção

| Tipo de problema | Componente | Nota de versão |
|---|---|---|
| Bug | Pesquisa social | Correção de um bug que impedia a publicação de ativos salvos do YouTube no Social Search. |
| Aprimoramento | Sincronização social | Sincronização social obsoleta do Twitter. |
| Aprimoramento | Storify 2 | Adicionado um aprimoramento para exibir a mensagem "Nenhum resultado encontrado" na pesquisa Tópico do Facebook quando nenhum resultado é encontrado. |
| Aprimoramento | Fluxos | Adicionadas regras de resumo para regras SAFE na parte inferior da página de fluxo do Twitter. |
| Bug | Fluxos | Adicionado um aprimoramento para desativar visivelmente a caixa de seleção "usuário verificado" nas Regras de fluxo do Twitter quando autores excluídos são fornecidos. |
| Bug | Fluxos | Correção de um erro que permitia o uso de palavras-chave ANDing e um filtro de Localização em uma regra do Twitter. |
| Bug | Studio | Correção de um erro que impedia que a "Tag de recurso" fosse salva corretamente quando aplicada. |

## Versão UAT

| Tipo de problema | Componente | Nota de versão |
|---|---|---|
| Bug | Conteúdo do aplicativo | Alteração do comportamento de "Mais informações" de modo que, se houver vários eventos de sinalizador Anônimo em um determinado conteúdo, o primeiro evento sempre será exibido. |
| Bug | Biblioteca | Correção de um bug que causava a falha intermitente de pesquisas de Biblioteca com hashtags. |
| Bug | Mapas | Correção de um bug no Maps para suportar um grande número de conteúdo em clusters em dispositivos iOS. |
| Aprimoramento | Mosaico | Adicionada a capacidade de configurar aplicativos Mosaic para clicar em qualquer lugar em um cartão de conteúdo para abrir o modal por tipo de animação `none` no designer e `cardAnimation: 'off'`se houver instanciamento por meio do SDK. |
| Bug | Mosaico | Correção de um erro que permitia que os usuários fizessem alterações com êxito em aplicativos Mosaico no Designer. |
| Aprimoramento | Solicitação de direitos | Adicionado um novo status de solicitação de direitos chamado "Falha na solicitação" para realçar quando as mensagens de solicitação de direitos não são enviadas. |
| Aprimoramento | Configurações | Adicionada a capacidade de os clientes criarem Regras de moderação de spam em Configurações. |
| Aprimoramento | Pesquisa social | Correção de um erro que impedia a exibição de postagens VK.com por meio de Pesquisas sociais de URL. |
| Aprimoramento | Pesquisa social | Ao procurar conteúdo do Instagram no Studio, se a pesquisa for devido a um token da API do Instagram expirado, a mensagem de erro agora indicará como tal. |
| Bug | Fluxos | Correção de um erro que fazia com que o banner "O aplicativo não está aceitando novo conteúdo" fosse exibido falsamente na parte superior das páginas de Regras de fluxo. |
| Aprimoramento | Fluxos | Modificado o padrão de regras de fluxo recém-criadas para Aplicar regras SAFE quando aplicável. |
| Aprimoramento | Streams (anteriormente, Regras de preparação) | Removida a opção somente "Vines" das regras de fluxo/preparação do Twitter, pois as Vinhas agora são exibidas como vídeos do Twitter. |
| Bug | Studio Shell | Correção de um erro que fazia com que o Livefyre Studio fosse carregado se o https:// fosse explicitamente anexado ao url. |

