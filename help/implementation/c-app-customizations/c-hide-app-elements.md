---
description: Remova os componentes padrão do aplicativo Livefyre do aplicativo.
seo-description: Remova os componentes padrão do aplicativo Livefyre do aplicativo.
seo-title: Ocultar elementos do aplicativo
solution: Experience Manager
title: Ocultar elementos do aplicativo
uuid: ea 090 b 6 e -99 f 5-4 bd 7-aa 9 e-d 39 a 4 dff 1543
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Ocultar elementos do aplicativo{#hide-app-elements}

Remova os componentes padrão do aplicativo Livefyre do aplicativo.

Use o CSS para ocultar os elementos padrão do Livefyre de sua página, permitindo personalizar a experiência do usuário para atender às suas necessidades.

Para ocultar elementos do aplicativo, basta definir a exibição como Nenhum.

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

