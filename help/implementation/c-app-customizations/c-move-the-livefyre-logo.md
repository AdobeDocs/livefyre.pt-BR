---
description: Reposicione o logotipo do Livefyre na sua página.
seo-description: Reposicione o logotipo do Livefyre na sua página.
seo-title: Mover o logotipo do Livefyre
solution: Experience Manager
title: Mover o logotipo do Livefyre
uuid: 807304 ae -6070-4505-87 db -169 a 925 f 714 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Mover o logotipo do Livefyre{#move-the-livefyre-logo}

Reposicione o logotipo do Livefyre na sua página.

Se o seu contrato com o Livefyre permitir, você pode mover o logotipo do Livefyre da parte superior do fluxo de conteúdo para a inferior.

Por exemplo, adicione o seguinte HTML à sua página imediatamente após o elemento que contém o aplicativo Livefyre:

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

Em seguida, adicione o seguinte à folha de estilo de sua página:

```
/* Hide the top logo */ 
.fyre-widget .fyre-logo-drop, .fyre-widget .fyre-logo-help, .fyre-widget .fyre-help { 
    display:none !important; 
} 
  
/* Style the bottom logo */ 
#powered_by_livefyre_new a {    background: url(https://cdn.livefyre.com/libs/fyre.conv/v3.0.0/images/poweredbylivefyre.png) no-repeat left top; 
    display: block; 
    height: 24px; 
    font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
} 
#powered_by_livefyre_new a:hover { 
    text-decoration: underline; 
}
```

