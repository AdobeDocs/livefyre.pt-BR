---
description: Você pode ouvir eventos em uma instância de Sidenotes.
seo-description: Você pode ouvir eventos em uma instância de Sidenotes.
seo-title: Eventos do aplicativo Sidenotes
solution: Experience Manager
title: Eventos do aplicativo Sidenotes
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Eventos do aplicativo Sidenotes {#sidenotes-app-events}

Você pode ouvir eventos em uma instância de Sidenotes.

Os retornos de chamada podem ser registrados com `onmethod` e não registrados com o método `removeListener`. Um método `once` está disponível para conveniência se o retorno de chamada for chamado apenas uma vez e depois cancelado.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Para obter mais informações sobre eventos do Livefyre, consulte a página Eventos do JavaScript na seção Referência.

| Chave | Descrição |
|--- |--- |
| sidenotes.initialized | Acionado quando o aplicativo é instanciado, tem dados e está na página. |
| sidenotes.commentFlagged | Acionado quando um comentário é sinalizado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi sinalizado</li><li>`type`: string de tipo de sinalizador  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Acionado quando um comentário é publicado. Os dados contêm: <br><ul><li> `authorId`: id do autor do comentário </li><li>`bodyHtml`: corpo do comentário </li><li> `parent`: id do pai do comentário, ou nulo</li></ul> |
| `sidenotes.commentShared` | Acionado quando um comentário é compartilhado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi compartilhado </li><li> `sharedToFacebook`: se o comentário foi compartilhado no Facebook </li><li>`sharedToTwitter`: se o comentário foi compartilhado no Twitter</li></ul> |
| `sidenotes.commentVoted` | Disparado quando um comentário é votado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi votado </li><li> `targetAuthorId`: id do autor cujo comentário foi votado</li><li> `type`: tipo de voto numérico: 0: &quot;clear&quot;, 1: &quot;upvote&quot;, ou 2: &quot;downvote&quot;</li></ul> |
| `sidenotes.userLoggedIn` | Acionado quando um usuário faz logon. Os dados contêm: <br><ul><li>`avatar`: url de avatar para o usuário </li><li>`displayName`: nome de exibição do usuário</li><li>`id`: id do usuário</li><li> `isModerator`: se o usuário é moderador da coleção atual</li></ul> |
| `sidenotes.userLoggedOut` | Disparado quando um usuário faz logout |
