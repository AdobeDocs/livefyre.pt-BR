---
description: Use a Bootstrap e a Stream API com aplicativos Livefyre.
seo-description: Use a Bootstrap e a Stream API com aplicativos Livefyre.
seo-title: Usar a API Bootstrap e Stream com aplicativos Livefyre
solution: Experience Manager
title: Exibindo Detalhes da Conta
uuid: bace558f-ade8-49d6-abda-9ee754ce4ac0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# Usar a API Bootstrap e Stream com aplicativos Livefyre {#bootstrap-stream-api}

## API de inicialização {#bootstrap-api}

### Como posso recuperar conteúdo mais antigo que as 50 mais recentes? {#howcontentolder}

O Bootstrap é todo conteúdo em um aplicativo Livefyre. São os dados em cache, normalmente com 12 a 20 minutos de duração. Ele é entregue em pedaços de 50 partes e é paginado para que você possa recuperar conteúdo com mais de 50 partes.

[Referência da API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Exemplo de solicitação](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

A solicitação de exemplo acima carrega a `init` página que contém as Configurações da coleção e o único conjunto inicial de ~50 partes do conteúdo mais recente. Para pesquisar conteúdo antigo, é necessário carregar as páginas de inicialização subsequentes com `N` o número da página:

Solicitação: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Por exemplo, um aplicativo de amostra tem 120 partes de conteúdo. O conteúdo "1" é o conteúdo mais antigo e o conteúdo "70" é o conteúdo mais recente.

* `Init` carregará ~120-70 partes de conteúdo em ordem decrescente: [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` carregará entre 1 e 50 partes de conteúdo em ordem crescente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` carregará cerca de 51 a 100 partes de conteúdo em ordem crescente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` carregará ~101-120 partes de conteúdo em ordem crescente:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Clique aqui para ver o Fluxograma da pesquisa Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de fluxo {#stream-api}

O que é a API de fluxo?
Stream é uma longa pesquisa que, por padrão, deve permanecer aberta por aproximadamente 30 segundos. A descrição da técnica de pesquisa longa pode ser encontrada aqui: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Esse endpoint de pesquisa prolongada transmite novo conteúdo (por exemplo, um usuário posta um comentário), alterações no status do conteúdo (por exemplo, o usuário exclui seus comentários, curtidas) e alterações de moderação do conteúdo (por exemplo, o moderador aprova um conteúdo) para um aplicativo Livefyre.

A solicitação para a API de fluxo deve ser ~30 segundos (pesquisa prolongada) com tempo limite esperado após 30 segundos quando nenhum novo conteúdo é transmitido.

Referência da API: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Exemplo de solicitação:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Observe que: A ID de evento mais alta das atualizações `maxEventId` em uma resposta de API de fluxo é a ID de evento mais alta dessa resposta. Use esse valor como parâmetro de `lastEventId` caminho ao criar o URL da próxima solicitação de API de fluxo para obter atualizações que ocorram após todas as atualizações nessa resposta.

O exemplo abaixo é baseado em um aplicativo de comentários:

O comentário "Primeiro comentário" foi publicado primeiro. "Segundo comentário" foi publicado depois.

Primeira resposta da API de fluxo de comentários:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

A resposta `maxEventId` é "1520289700953369", que será usado como referência `lastEventId` ao terminal para obter atualizações (isto é, o Segundo Comentário) que ocorrem após todas as atualizações nesta resposta.

Segunda resposta da API de fluxo de comentários:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

A resposta `maxEventID` "1520289700953369" deve, por sua vez, ser usada como a resposta da API de fluxo `lastEventID` para a próxima atualização.