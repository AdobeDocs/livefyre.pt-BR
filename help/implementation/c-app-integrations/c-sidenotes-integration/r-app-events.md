---
description: Você pode ouvir eventos em uma instância de Sidenotes.
seo-description: Você pode ouvir eventos em uma instância de Sidenotes.
seo-title: Eventos de aplicativo de sidenotes
solution: Experience Manager
title: Eventos de aplicativo de sidenotes
uuid: afca 4 b 03-c 370-41 ca-aa 12-45 bc 357517 ca
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Eventos de aplicativo de sidenotes {#sidenotes-app-events}

Você pode ouvir eventos em uma instância de Sidenotes.

Retornos de chamada podem ser registrados com `onmethod` o método e não registrados com o `removeListener` método. Um `once` método está disponível para conveniência se a chamada de retorno deva ser chamada somente uma vez e depois não registrada.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Para obter mais informações sobre eventos do Livefyre, consulte a página Eventos do javascript na seção Referência.

| Chave | Descrição |
|--- |--- |
| sidenotes. initialized | Disparado quando o aplicativo é instanciado, tem dados e está na página. |
| sidenotes. commentflagged | Disparado quando um comentário foi sinalizado. Os dados contêm: <br><ul><li>`targetId`: id do comentário sinalizado</li><li>`type`: string do tipo de sinalizador `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Disparado quando um comentário foi publicado. Os dados contêm: <br><ul><li> `authorId`: id do autor do comentário </li><li>`bodyHtml`: corpo do comentário </li><li> `parent`: id do pai do comentário ou nulo</li></ul> |
| `sidenotes.commentShared` | Disparado quando um comentário foi compartilhado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi compartilhado </li><li> `sharedToFacebook`: se o comentário foi compartilhado no Facebook </li><li>`sharedToTwitter`: se o comentário foi compartilhado no Twitter</li></ul> |
| `sidenotes.commentVoted` | Disparado quando um comentário foi votado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi votado </li><li> `targetAuthorId`: id do autor cujo comentário foi votado</li><li> `type`: tipo numérico de voto: 0: ' clear ', 1: ' upvote'ou 2: ' downvotem '</li></ul> |
| `sidenotes.userLoggedIn` | Disparado quando um usuário faz logon. Os dados contêm: <br><ul><li>`avatar`: avatar url para o usuário </li><li>`displayName`: nome de exibição do usuário</li><li>`id`: id do usuário</li><li> `isModerator`: se o usuário é moderador da coleção atual</li></ul> |
| `sidenotes.userLoggedOut` | Disparado quando um usuário faz logout |
