---
description: Os estilos personalizados são aplicados por meio de um objeto inserido no construtor Sidenotes.
seo-description: Os estilos personalizados são aplicados por meio de um objeto inserido no construtor Sidenotes.
seo-title: Estilos Personalizados de Sidenotes
title: Estilos Personalizados de Sidenotes
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Estilos Personalizados de Sidenotes{#sidenotes-custom-styles}

Os estilos personalizados são aplicados por meio de um objeto inserido no construtor Sidenotes.

As "chaves" são chaves de objeto que representam elementos DOM, enquanto as "propriedades" são propriedades CSS suportadas para a chave específica. Por exemplo, para personalizar o estilo de blockBtn (que é o botão que inicia o portão Sidenotes), é necessário construir um objeto como:

```
var styles = { 
   'blockBtn': { 
      'fontColor': '#555', 
      'fontSize': '18px' 
   } 
}; 
new Livefyre.Sidenotes({ 
   customStyles: styles, 
      ...  
})
```

| **Chave** | **Propriedades** | Descrição |
|---|---|---|
| `anonymousAvatar` | "height", "width" | Imagem de avatar anônima, à esquerda do editor de área de texto. |
| `blockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | O "ícone Iniciador" posicionado ao lado dos elementos especificados como compatíveis com nota. |
| `blockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Ícone Iniciador quando em um estado ativo. |
| `commentAvatar` | "height", "width" | Imagem de avatar à esquerda das notas de nível superior. |
| `commentBody` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Corpo de texto das notas encadeadas. |
| `commentDisplayName` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Exibir o nome do usuário que deixou uma nota. |
| `commentDownvote` | ‘fontColor’, ‘fontSize’ | Botão de votação em uma nota. |
| `commentReplyExpand` | "backgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Botão para expandir threads com um grande número de respostas. |
| `commentTags` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Tags sobre um usuário em uma nota. |
| `commentUpvote` | ‘fontColor’, ‘fontSize’ | Botão de aumento de votos em uma nota. |
| `editorTextarea` | ‘height’, ‘width’, ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Caixa de entrada de área de texto para notas de saída. |
| `mediaBlockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Ícone de iniciador de mídia quando estiver sobre um item de mídia (img, vídeo). |
| `mediaBlockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Ícone de iniciador de mídia em um estado ativo. |
| `numSidenotes` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight", "backgroundColor", "borderColor", "borderWidth", "height", "width" | Botão clicável que mostra o número de Sidenotes na coleção. |
| `numSidenotesPopover` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight", "backgroundColor", "borderColor", "borderWidth", "height", "width" | Popover com uma breve explicação de Sidenotes para o usuário. |
| `popover` | "backgroundColor" | Popover que é criado quando o ícone de iniciador é chamado. |
| `popoverArrowLeft` | "backgroundImage", "height", "left", "right", "top", "width" | Elemento de seta para a esquerda no portão que aponta para o elemento DOM que contém um ícone de iniciador. |
| `popoverArrorRight` | "backgroundImage", "height", "left", "right", "top", "width" | O elemento de seta para a direita no portão que aponta para o elemento DOM que contém um ícone de iniciador. |
| `popoverArrowTop` | "backgroundImage", "height", "left", "right", "top", "width" | O elemento de seta superior no povir que aponta para o elemento DOM que contém um ícone de iniciador. |
| `replyAvatar` | "height", "width" | Imagem de avatar à esquerda das notas de nível de resposta. |
| `streamPoweredBy` | "backgroundColor", "borderColor", "lineHeight" | Rodapé "acionado por" no portão. |
| `streamQueueButton` | "backgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Botão para indicar quando novas notas são enviadas em um portão aberto. |
| `userAvatar` | "height", "width" | Imagem de avatar do usuário autenticada, à esquerda do editor de área de texto. |

