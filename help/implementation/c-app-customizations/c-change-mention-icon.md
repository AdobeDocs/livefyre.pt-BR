---
description: Altere o ícone que é exibido a usuários do Livefyre no menu suspenso @mention.
seo-description: Altere o ícone que é exibido a usuários do Livefyre no menu suspenso @menção.
seo-title: Alterar ícone de menção
solution: Experience Manager
title: Alterar ícone de @mention
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# Alterar `@mention` ícone {#change-mention-icon}

Change the icon displayed for Livefyre users in the `@mention` pulldown menu.

Altere o ícone Livefyre usado no menu suspenso para `@mention` um ícone de sua escolha, permitindo que você indique os membros da sua comunidade com seu próprio ícone.

## Exemplo

Para alterar esse ícone, adicione o seguinte CSS à sua folha de estilos. Substitua o url &lt;*seu recurso*&gt; pelo URL da imagem selecionada para substituir o selo padrão do Livefyre.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
