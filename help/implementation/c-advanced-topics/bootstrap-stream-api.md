---
description: Use a API de fluxo e do Bootstrap com os aplicativos Livefyre.
title: Visualizando detalhes da conta
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Use a API de fluxo e do Bootstrap com os aplicativos Livefyre {#bootstrap-stream-api}

## API do Bootstrap {#bootstrap-api}

### Como posso recuperar conteúdo mais antigo que as 50 partes mais recentes? {#howcontentolder}

O Bootstrap é todo o conteúdo em um aplicativo Livefyre. São os dados em cache, normalmente de 12 a 20 minutos. Ele é entregue em partes de 50 partes e é paginado para que você possa recuperar conteúdo com mais de 50 partes.

[Referência da API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Exemplo de solicitação](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

A solicitação de exemplo acima carrega a página `init` que contém as Configurações da coleção e o único conjunto inicial de ~50 partes do conteúdo mais recente. Para pesquisar conteúdo mais antigo, você deve carregar as páginas de inicialização subsequentes com `N` sendo o número da página:

Solicitação: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Por exemplo, um aplicativo de amostra tem 120 partes de conteúdo. O conteúdo &quot;1&quot; é o conteúdo mais antigo e o conteúdo &quot;70&quot; é o conteúdo mais recente.

* `Init` O carregará ~120-70 partes de conteúdo em ordem decrescente:  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` O carregará entre 1 e 50 partes do conteúdo em ordem crescente:  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json`
* `1.json` O carregará entre 51 e 100 partes do conteúdo em ordem crescente:  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json`
* `2.json` O carregará ~101-120 partes de conteúdo em ordem crescente:`https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json`

[Clique aqui para ver o Fluxograma da Pesquisa de Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de fluxo {#stream-api}

O que é a API de fluxo?
Stream é uma pesquisa longa que, por design, deve permanecer aberta por aproximadamente 30 segundos. A descrição da técnica Long Polling pode ser encontrada aqui: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Esse endpoint de pesquisa prolongada transmite conteúdo novo (por exemplo, um usuário publica um comentário), alterações no status do conteúdo (por exemplo, o usuário exclui o comentário, curtidas) e alterações de moderação no conteúdo (por exemplo, o moderador aprova um conteúdo) para um aplicativo do Livefyre.

A solicitação para a API de fluxo deve ser de aproximadamente 30 segundos (pesquisa prolongada), com o tempo limite esperado após 30 segundos, quando nenhum novo conteúdo é transmitido.

Referência da API: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operações:v3.1:collection:atualizações:método=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Exemplo de solicitação:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Observe: O `maxEventId` em uma resposta da API de fluxo é a ID de evento mais alta das atualizações nessa resposta. Use esse valor como parâmetro de caminho `lastEventId` ao criar o URL da próxima solicitação de API de fluxo para obter atualizações que ocorrem depois de todas as atualizações nessa resposta.

O exemplo abaixo é baseado em um Aplicativo de comentários:

O comentário &quot;Primeiro comentário&quot; foi publicado primeiro. &quot;Segundo comentário&quot; foi publicado depois.

Primeira resposta da API de fluxo de comentários:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

O `maxEventId` na resposta é &quot;1520289700953369&quot; que será usado como `lastEventId` para pesquisar o endpoint para obter atualizações (ou seja, Segundo comentário) que ocorrem após todas as atualizações nessa resposta.

Segunda resposta da API de fluxo de comentários:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

O `maxEventID` &quot;1520289700953369&quot; na resposta deve, por sua vez, ser usado como o `lastEventID` para criar a resposta da API de fluxo para a próxima atualização.
