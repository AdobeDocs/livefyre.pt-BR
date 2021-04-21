---
description: Você pode ouvir eventos em uma instância de Observações.
title: Eventos do aplicativo Sidenotes
exl-id: e341ca76-002d-425c-8d1a-35c3253fb254
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Destaca Eventos de Aplicativo {#sidenotes-app-events}

Você pode ouvir eventos em uma instância de Observações.

As chamadas de retorno podem ser registradas com o `onmethod` e não registradas com o método `removeListener`. Um método `once` está disponível para conveniência se o retorno de chamada for chamado apenas uma vez e depois não registrado.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Para obter mais informações sobre eventos do Livefyre, consulte a página Eventos do JavaScript na seção Referência .

| Chave | Descrição |
|--- |--- |
| sidenotes.initialized | Acionado quando o aplicativo é instanciado, tem dados e está na página. |
| sidenotes.commentFlagged | Disparado quando um comentário é sinalizado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi sinalizado</li><li>`type`: cadeia de caracteres de tipo de sinalizador  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Disparado quando um comentário é publicado. Os dados contêm: <br><ul><li> `authorId`: id do autor do comentário </li><li>`bodyHtml`: corpo do comentário </li><li> `parent`: id do pai do comentário, ou nulo</li></ul> |
| `sidenotes.commentShared` | Disparado quando um comentário é compartilhado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi compartilhado </li><li> `sharedToFacebook`: se o comentário foi compartilhado com a Facebook </li><li>`sharedToTwitter`: se o comentário foi compartilhado com a Twitter</li></ul> |
| `sidenotes.commentVoted` | Disparado quando um comentário é votado. Os dados contêm: <br><ul><li>`targetId`: id do comentário que foi votado </li><li> `targetAuthorId`: id do autor cujo comentário foi votado</li><li> `type`: tipo de votação numérica: 0: &quot;clear&quot;, 1: &quot;votação nominal&quot; ou 2: &quot;downvot&quot;</li></ul> |
| `sidenotes.userLoggedIn` | Acionado quando um usuário faz logon. Os dados contêm: <br><ul><li>`avatar`: url de avatar para o usuário </li><li>`displayName`: nome de exibição do usuário</li><li>`id`: id do usuário</li><li> `isModerator`: se o usuário é um moderador da coleção atual</li></ul> |
| `sidenotes.userLoggedOut` | Disparado quando um usuário faz logout |
