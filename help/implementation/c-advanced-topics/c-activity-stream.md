---
description: Saiba como monitorar e armazenar o conteúdo gerado pelo usuário que flui pelo sistema Livefyre.
seo-description: Saiba como monitorar e armazenar o conteúdo gerado pelo usuário que flui pelo sistema Livefyre.
seo-title: Fluxo de atividade
solution: Experience Manager
title: Fluxo de atividade
uuid: f40deec1-58ab-41c9-aac4-d2d8c9192bb9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---


# Fluxo de atividade {#activity-stream}

Saiba como monitorar e armazenar o conteúdo gerado pelo usuário que flui pelo sistema Livefyre.

Use a API de fluxo de Atividade para consumir dados gerados pelo usuário que fluem pelo sistema Livefyre em sua rede ou site. Por exemplo: use dados desta API para atualizar seus índices de pesquisa com base em classificações ou para gerenciar os crachás dos usuários em um sistema de terceiros com base em sua atividade.

API de fluxo de atividade:

Para obter uma lista completa dos pontos de extremidade disponíveis, consulte a seção Referência da API do Livefyre.

## Recursos {#section_aql_n4l_b1b}

Há dois pontos finais, um para o ambiente de preparo e outro para a produção.

### Armazenamento temporário

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Produção

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### Parâmetros

* **recurso:** ** stringUm URN do objeto para o qual você está solicitando dados de atividade.

* **desde:** ** integerUm número inteiro de 64 bits que representa a ID do último evento recebido. Especifique &quot;0&quot; se não tiver dados anteriores.

## Strings de URN {#section_skl_q4l_b1b}

Exemplos:

* **urn:livefyre:** `example.fyre.co` o fluxo de atividade para  `example.fyre.co`.
* **urn:livefyre:** `example.fyre.co:site=54321` o fluxo de atividade do site 54321 na  `example.fyre.co` rede.

## Políticas de token {#section_nwh_c5j_11b}

A API de fluxo de Atividade usa um token de portador OAuth para autenticação. Os Tokens do Portador fazem parte da especificação OAuth 2.0 e oficialmente descritos [aqui](https://tools.ietf.org/html/rfc6750#section-1.2).

Um token contém vários itens:

* Quem criou o token.
* A quem foi dado um token.
* Um horário em que não é mais válido.
* A coisa em que estamos operando.
* Uma lista de permissões que foram concedidas.

### Etapas

As etapas para criar um token do portador OAuth incluem:

* Crie um mapa/dicionário contendo o emissor, a audiência, o assunto, a expiração e o escopo.
* Use a biblioteca JWT, com seu segredo, para codificar um token JWT.
* Adicione &quot;Autenticação: &quot;Portador&quot; para sua solicitação HTTP.

A amostra de código abaixo demonstra as etapas acima em Python:

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

Onde as teclas do token do portador são definidas da seguinte forma:

* **is** *(Issuer)* Uma entidade com autoridade para gerar tokens. Pode ser o Livefyre, um site ou uma rede. (Para que uma nota chegue atrasada à escola, é seu pai.)
* **aud** *(Audiência)* A pessoa para a qual esse token foi gerado. Se você mesmo estiver criando o token, ele será o site ou a rede.
* **sub** *(Assunto)* O assunto para o qual as permissões devem ser concedidas. Por exemplo, se você estiver operando em uma coleção, o assunto deve ser o identificador da coleção. (No exemplo da escola, é você.)
* **exp** *(Expiração)* Um ponto no tempo em que o token não é mais válido.
* **scope** *(Scope)* Esta é uma lista das permissões concedidas sobre o assunto. &quot;Atraso na escola&quot; é um exemplo. O nome de uma API é outro exemplo.

## Exemplo {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## Resposta {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

Uma resposta com novos dados desde a última solicitação:

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## Notas {#section_hj3_crj_11b}

* Uma chamada bem-sucedida para a API produzirá um código de status HTTP 200. Todos os outros códigos de status devem ser considerados erros.
* Se não for nulo, use o valor de `data.meta.cursor.next` como o parâmetro `since` da próxima solicitação.
* Se o valor de `data.meta.cursor.next` for nulo, isso significa que não há novos dados a serem consumidos. Você deve solicitar novamente mais tarde com o mesmo valor `since` para ver se novos dados chegaram.
* Por uma questão de prática, você deve solicitar mais dados imediatamente se o valor `data.meta.cursor.next` não for nulo.
* O valor aproximado de duas horas dos dados recentes está disponível por meio dessa API na produção.
* Você deve configurar seus processos para pesquisar esse terminal frequentemente no cronjob para evitar a perda de dados. Um intervalo de cinco minutos deve ser perfeitamente adequado para a maioria das implementações.
