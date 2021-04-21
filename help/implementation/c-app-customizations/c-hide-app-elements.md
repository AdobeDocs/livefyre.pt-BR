---
description: Remova os componentes padrão do aplicativo Livefyre do seu aplicativo.
title: Ocultar elementos do aplicativo
exl-id: f8bbed2c-d009-41b8-927d-8d6ac4a63571
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# Ocultar elementos do aplicativo{#hide-app-elements}

Remova os componentes padrão do aplicativo Livefyre do seu aplicativo.

Use o CSS para ocultar elementos padrão do aplicativo Livefyre na sua página, permitindo personalizar a experiência do usuário para atender às suas necessidades.

Para ocultar elementos do aplicativo, basta definir a exibição como nenhum.

Exemplos:

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```
