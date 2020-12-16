---
description: Reposicione o logotipo do Livefyre em sua página.
seo-description: Reposicione o logotipo do Livefyre em sua página.
seo-title: Mova o logotipo Livefyre
solution: Experience Manager
title: Mova o logotipo Livefyre
uuid: 807304ae-6070-4505-87db-169a925f714c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---


# Mova o logotipo Livefyre{#move-the-livefyre-logo}

Reposicione o logotipo do Livefyre em sua página.

Se o seu acordo com o Livefyre permitir, você poderá mover o logotipo do Livefyre da parte superior do fluxo de conteúdo para a parte inferior.

Por exemplo, adicione o seguinte HTML à sua página imediatamente após o elemento que contém o aplicativo Livefyre:

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

Em seguida, adicione o seguinte à folha de estilos da sua página:

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

