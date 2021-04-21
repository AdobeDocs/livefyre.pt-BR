---
description: Altere o ícone que é exibido a usuários do Livefyre no menu suspenso @menção.
title: Alterar ícone de menção
exl-id: e078ef7f-7f16-4f5d-9152-95ae7fe7e4bd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---

# Alterar ícone `@mention` {#change-mention-icon}

Altere o ícone exibido para usuários do Livefyre no menu suspenso `@mention`.

Altere o ícone Livefyre usado no menu suspenso `@mention` para um ícone de sua escolha, permitindo indicar os membros da comunidade com seu próprio ícone.

## Exemplo

Para alterar esse ícone, adicione o seguinte CSS à sua folha de estilos. Substitua &lt;*o url de recurso* pelo URL da imagem selecionada para substituir o símbolo padrão Livefyre.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
