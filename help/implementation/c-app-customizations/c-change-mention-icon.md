---
description: Altere o ícone que é exibido a usuários do Livefyre no menu suspenso @mention.
seo-description: Altere o ícone que é exibido a usuários do Livefyre no menu suspenso @menção.
seo-title: Alterar ícone de menção
solution: Experience Manager
title: Alterar ícone de @mention
uuid: a 395 f 4 ff-a 774-454 a -8 d 94-4 a 3371 d 8 cc 2 c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# Alterar `@mention` ícone {#change-mention-icon}

Altere o ícone exibido para usuários do Livefyre no menu `@mention` suspenso.

Altere o ícone do Livefyre usado no menu `@mention` suspenso para um ícone de sua escolha, permitindo indicar os membros da comunidade com seu próprio ícone.

## Exemplo

Para alterar esse ícone, adicione o seguinte CSS à sua folha de estilo. Substitua &lt;*seu recurso*&gt; url pelo URL da imagem selecionada para substituir o crachá padrão Livefyre.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
