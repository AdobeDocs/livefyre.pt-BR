---
description: Use o Bootstrap e a API de fluxo com aplicativos do Livefyre.
seo-description: Use o Bootstrap e a API de fluxo com aplicativos do Livefyre.
seo-title: Usar o bootstrap e a API de fluxo com aplicativos do Livefyre
solution: Experience Manager
title: Visualizando detalhes da conta
uuid: bace 558 f-ade 8-49 d 6-abda -9 ee 754 ce 4 ac 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Usar o bootstrap e a API de fluxo com aplicativos do Livefyre {#bootstrap-stream-api}

## API de bootstrap {#bootstrap-api}

### Como posso recuperar conteúdo mais antigo do que 50 peças mais recentes? {#howcontentolder}

Bootstrap é todo conteúdo em um aplicativo do Livefyre. São os dados em cache, normalmente de 12a 20 minutos. É entregue em blocos de 50 partes e é paginado para que você possa recuperar conteúdo com mais de 50 peças.

[Referência da API](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Exemplo de solicitação](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

A solicitação de exemplo acima carrega a `init` página que contém Configurações da coleção e o único conjunto inicial de ~ 50 partes do conteúdo mais recente. Para navegar pelo conteúdo mais antigo, é necessário carregar páginas de carregamento subsequentes com `N` o número da página:

Solicitação: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Por exemplo, um aplicativo de exemplo tem 120 partes de conteúdo. O conteúdo "1" é o conteúdo mais antigo e o conteúdo "70" é o conteúdo mais recente.

* `Init` carregará ~ 120-70 partes de conteúdo em ordem decrescente: [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` carregará ~ 1-50 partes de conteúdo em ordem crescente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` carregará ~ 51-100 partes de conteúdo em ordem crescente: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` carregará ~ 101-120 partes de conteúdo em ordem crescente:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Clique aqui para ver o Fluxograma de pesquisa do Bootstrap.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API de fluxo {#stream-api}

O que é a API de fluxo?
Stream é uma pesquisa longa que por design deve permanecer aberta por aproximadamente 30 segundos. A descrição na técnica de pesquisa longa pode ser encontrada aqui: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Este endpoint de longa pesquisa transmite novo conteúdo (por exemplo, um usuário posta um comentário), alterações no status do conteúdo (por exemplo, excluir seu comentário, curtir) e alterações de moderação ao conteúdo (por exemplo, moderador aprova um pedaço de conteúdo) a um aplicativo Livefyre.

A solicitação para a API de fluxo deve ser de ~ 30 segundos (pesquisa longa) com o tempo limite esperado após 30 segundos quando nenhum novo conteúdo for transmitido.

Referência da API: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Exemplo de solicitação:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Observação: A `maxEventId` resposta de API de fluxo é a mais alta ID de evento das atualizações nesta resposta. Use esse valor como `lastEventId` parâmetro de caminho ao criar o URL da próxima solicitação de API de fluxo para obter atualizações que ocorrem após todas as atualizações nessa resposta.

O exemplo abaixo é baseado em um Aplicativo de comentários:

Comentário "Primeiro comentário" foi publicado primeiro. " Segundo comentário "foi publicado depois.

Resposta da primeira API de fluxo de comentário:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

A `maxEventId` resposta é "1520289700953369", que será usada como `lastEventId` para fazer pesquisas no endpoint para obter atualizações (ou seja, Segundo comentário) que ocorre após todas as atualizações nessa resposta.

Segunda resposta da API de fluxo de comentário:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

A `maxEventID` mensagem "1520289700953369" na resposta deve ser usada como a `lastEventID` resposta para a resposta da API de fluxo na próxima atualização.