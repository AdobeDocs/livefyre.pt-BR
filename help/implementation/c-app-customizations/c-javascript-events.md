---
description: Os eventos disponíveis para os quais você pode vincular JavaScript para aplicativos de Conversação (por exemplo, Comentários, Chat, Blog em tempo real, Avaliações e Observações).
seo-description: Os eventos disponíveis para os quais você pode vincular JavaScript para aplicativos de Conversação (por exemplo, Comentários, Chat, Blog em tempo real, Avaliações e Observações).
seo-title: Definições e exemplos de eventos JavaScript
solution: Experience Manager
title: Definições e exemplos de eventos JavaScript
uuid: 61da2e2e-8fcd-482d-93df-c946f0475277
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Definições e exemplos de eventos JavaScript{#javascript-events-definitions-and-examples}

Os eventos disponíveis para os quais você pode vincular JavaScript para aplicativos de Conversação (por exemplo, Comentários, Chat, Blog em tempo real, Avaliações e Observações).

O Livefyre fornece eventos JavaScript para rastrear a atividade do usuário nos aplicativos Livefyre. Por exemplo, você pode desejar atualizar a página quando os usuários curtirem ou compartilharem conteúdo no Twitter ou Facebook, ou quando novo conteúdo for publicado.

O Livefyre também permite que você adicione eventos a integrações de análises de terceiros (Adobe Analytics JS, Google Analytics, Gerenciamento dinâmico de tags etc.) para rastrear eventos do aplicativo. Para obter mais informações, entre em contato com o gerente de integração de terceiros para fornecer os eventos corretos.

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
>Objetos de dados são fornecidos para todos os manipuladores de eventos. Objetos de dados de exemplo seguem cada evento.

## commentPosted {#section_qfr_51p_xz}

Um usuário postou um comentário.

* Um pai de nulo é um novo comentário.
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

## commentFlagged {#section_szy_s1p_xz}

Um usuário sinalizou um comentário.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

Um usuário gostou de um comentário.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

Um usuário compartilhou um comentário do fluxo. (Esse evento não é acionado quando os usuários compartilham do editor de comentários.) Esse evento é acionado quando o botão Compartilhar é clicado.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdates {#section_qdq_f1p_xz}

O número total de comentários visíveis nesta conversa mudou (aumentados ou diminuídos).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

Um usuário fez logon.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## userLoggedOut {#section_tsg_5z4_xz}

Um usuário desconectou.

os dados não estão definidos.

## socialMention {#section_a1w_tz4_xz}

Um usuário incluiu uma @menção em um comentário. Retorna uma matriz dos seguintes itens:

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeature

Um usuário moderador apresentou um comentário. Retorna uma matriz dos seguintes itens:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

O fluxo de comentários foi carregado e o conjunto inicial de conteúdo foi obtido do servidor e exibido ao usuário.

os dados não estão definidos.

## showMore {#section_pqg_nz4_xz}

Um usuário clicou no **[!UICONTROL Show More]** botão.

os dados não estão definidos.

## userSegulowed {#section_xxw_jz4_xz}

Retorna true quando um usuário clica no **[!UICONTROL Follow]** botão e false quando o conteúdo é publicado no fluxo.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnfollow {#section_wm1_gz4_xz}

Retorna true quando um usuário clica no botão **Desseguir** e false quando o conteúdo é postado no fluxo.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

