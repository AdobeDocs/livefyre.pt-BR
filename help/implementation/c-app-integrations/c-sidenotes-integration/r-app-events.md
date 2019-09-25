---
description: Você pode ouvir eventos em uma instância de Sidenotes.
seo-description: Você pode ouvir eventos em uma instância de Sidenotes.
seo-title: Eventos do aplicativo Sidenotes
solution: Experience Manager
title: Eventos do aplicativo Sidenotes
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Eventos do aplicativo Sidenotes {#sidenotes-app-events}

Você pode ouvir eventos em uma instância de Sidenotes.

Retornos de chamada podem ser registrados com o `onmethod` e não registrados com o `removeListener` método. Um `once` método está disponível para conveniência se o retorno de chamada deve ser chamado apenas uma vez e, em seguida, não registrado.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Para obter mais informações sobre eventos do Livefyre, consulte a página Eventos JavaScript na seção Referência.

| Chave | Descrição |
|--- |--- |
| sidenotes.initialized | Acionado quando o aplicativo é instanciado, tem dados e está na página. |
| sidenotes.commentFlagged | Acionado quando um comentário é sinalizado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi sinalizado</li><li>`type`: string de tipo de sinalizador `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Acionado quando um comentário é publicado. Os dados contêm: <br><ul><li> `authorId`: id do autor do comentário </li><li>`bodyHtml`: corpo do comentário </li><li> `parent`: id do pai do comentário, ou nulo</li></ul> |
| `sidenotes.commentShared` | Acionado quando um comentário é compartilhado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi compartilhado </li><li> `sharedToFacebook`: se o comentário foi compartilhado no Facebook </li><li>`sharedToTwitter`: se o comentário foi compartilhado no Twitter</li></ul> |
| `sidenotes.commentVoted` | Disparado quando um comentário é votado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi votado </li><li> `targetAuthorId`: id do autor cujo comentário foi votado</li><li> `type`: tipo de voto numérico:0: "clear", 1: "upvote" ou 2: "downvote"</li></ul> |
| `sidenotes.userLoggedIn` | Acionado quando um usuário faz logon. Os dados contêm: <br><ul><li>`avatar`: url de avatar para o usuário </li><li>`displayName`: nome de exibição do usuário</li><li>`id`: id do usuário</li><li> `isModerator`: se o usuário é moderador da coleção atual</li></ul> |
| `sidenotes.userLoggedOut` | Disparado quando um usuário faz logout |
