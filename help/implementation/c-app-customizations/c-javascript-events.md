---
description: Os eventos disponíveis para os quais você pode vincular JavaScript para aplicativos de Conversação (por exemplo, Comentários, Chat, Blog em tempo real, Avaliações e Observações).
seo-description: Os eventos disponíveis para os quais você pode vincular JavaScript para aplicativos de Conversação (por exemplo, Comentários, Chat, Blog em tempo real, Avaliações e Observações).
seo-title: Definições e exemplos de eventos javascript
solution: Experience Manager
title: Definições e exemplos de eventos javascript
uuid: 61 da 2 e 2 e -8 fcd -482 d -93 df-c 946 f 0475277
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Definições e exemplos de eventos javascript{#javascript-events-definitions-and-examples}

Os eventos disponíveis para os quais você pode vincular JavaScript para aplicativos de Conversação (por exemplo, Comentários, Chat, Blog em tempo real, Avaliações e Observações).

O Livefyre fornece eventos javascript para rastrear a atividade do usuário em seus Aplicativos do Livefyre. Por exemplo, você pode querer atualizar a página quando os usuários curtirem ou compartilhar conteúdo no Twitter ou Facebook, ou quando novo conteúdo é publicado.

O Livefyre também permite adicionar eventos a integrações de análise de terceiros (JS do Adobe Analytics, Google Analytics, Gerenciamento dinâmico de tags etc.), para rastrear eventos do aplicativo. Para obter mais informações, consulte o gerente de integração de terceiros para fornecer os eventos corretos.

Para vincular a esses eventos, adicione o seguinte código à página ao instanciar seu aplicativo em uma página. Substitua o nome do evento por `{eventName}`:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>Objetos de dados são fornecidos para todos os manipuladores de eventos. Os objetos de dados de exemplo seguem cada evento.

## Commentpostposted {#section_qfr_51p_xz}

Um usuário postou um comentário.

* Um pai de null é um novo comentário.
* Um pai de Nenhum é um comentário que foi editado.
* Um número para pai é a ID pai da resposta.

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## Commentflagged {#section_szy_s1p_xz}

Um usuário sinalizou um comentário.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## Commentliked {#section_vc1_r1p_xz}

Um usuário curtiram um comentário.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## Commentshared {#section_nqb_31p_xz}

Um usuário compartilhou um comentário a partir do stream. (Esse evento não é acionado quando os usuários compartilham a partir do editor de Comentários.) Esse evento é acionado quando o botão Compartilhar é clicado.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## Commentcountupdated {#section_qdq_f1p_xz}

O número total de comentários visíveis nesta conversa foi alterado (aumenta ou diminui).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## Userloggedin {#section_yjt_vz4_xz}

Um usuário se conectou.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## Userloggedout {#section_tsg_5z4_xz}

Um usuário desconectou-se.

os dados são indefinidos.

## Socialmention {#section_a1w_tz4_xz}

Um usuário incluiu @ menção em um comentário. Retorna uma matriz do seguinte:

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## Commentfeatured

Um usuário do moderador destaque um comentário. Retorna uma matriz do seguinte:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## Initialrendercomplete {#section_odc_4z4_xz}

O fluxo de comentário foi carregado e o conjunto inicial de conteúdo foi obtido do servidor e exibido para o usuário.

os dados são indefinidos.

## Showmais {#section_pqg_nz4_xz}

Um usuário clicou no **[!UICONTROL Show More]** botão.

os dados são indefinidos.

## Userfollowed {#section_xxw_jz4_xz}

Retorna true quando um usuário clica no **[!UICONTROL Follow]** botão e false quando o conteúdo é postado no stream.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## Userunfollow {#section_wm1_gz4_xz}

Retorna true quando um usuário clica no **botão Parar e** false quando o conteúdo é postado no stream.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

