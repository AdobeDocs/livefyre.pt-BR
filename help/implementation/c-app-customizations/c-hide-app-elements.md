---
description: Remova os componentes padrão do aplicativo Livefyre do aplicativo.
seo-description: Remova os componentes padrão do aplicativo Livefyre do aplicativo.
seo-title: Ocultar elementos do aplicativo
solution: Experience Manager
title: Ocultar elementos do aplicativo
uuid: ea090b6e-99f5-4bd7-aa9e-d39a4dff1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# Ocultar elementos do aplicativo{#hide-app-elements}

Remova os componentes padrão do aplicativo Livefyre do aplicativo.

Use o CSS para ocultar os elementos padrão do aplicativo Livefyre da sua página, permitindo que você personalize a experiência do usuário para atender às suas necessidades.

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

