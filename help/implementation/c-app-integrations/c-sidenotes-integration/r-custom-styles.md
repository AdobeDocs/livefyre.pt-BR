---
description: Os estilos personalizados são aplicados por meio de um objeto inserido no construtor Sidenotes.
seo-description: Os estilos personalizados são aplicados por meio de um objeto inserido no construtor Sidenotes.
seo-title: Estilos Personalizados de Sidenotes
title: Estilos Personalizados de Sidenotes
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---


# Indica Estilos Personalizados{#sidenotes-custom-styles}

Os estilos personalizados são aplicados por meio de um objeto inserido no construtor Sidenotes.

As &quot;chaves&quot; são chaves de objeto que representam elementos DOM, enquanto as &quot;propriedades&quot; são propriedades CSS suportadas para a chave específica. Por exemplo, para personalizar o estilo de blockBtn (que é o botão que inicia o portão Sidenotes), é necessário construir um objeto como:

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
| `anonymousAvatar` | &quot;height&quot;, &quot;width&quot; | Imagem de avatar anônima, à esquerda do editor de área de texto. |
| `blockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | O &quot;ícone Iniciador&quot; posicionado ao lado dos elementos especificados como compatíveis com nota. |
| `blockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Ícone Iniciador quando em um estado ativo. |
| `commentAvatar` | &quot;height&quot;, &quot;width&quot; | Imagem de avatar à esquerda das notas de nível superior. |
| `commentBody` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Corpo de texto das notas encadeadas. |
| `commentDisplayName` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Exibir o nome do usuário que deixou uma nota. |
| `commentDownvote` | ‘fontColor’, ‘fontSize’ | Botão de votação em uma nota. |
| `commentReplyExpand` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Botão para expandir threads com um grande número de respostas. |
| `commentTags` | ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Tags sobre um usuário em uma nota. |
| `commentUpvote` | ‘fontColor’, ‘fontSize’ | Botão de aumento de votos em uma nota. |
| `editorTextarea` | ‘height’, ‘width’, ‘fontColor’, ‘fontFamily’, ‘fontSize’, ‘fontWeight’, ‘lineHeight’ | Caixa de entrada de área de texto para notas de saída. |
| `mediaBlockBtn` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Ícone de iniciador de mídia quando estiver sobre um item de mídia (img, vídeo). |
| `mediaBlockBtnActive` | ‘fontColor’, ‘fontSize’, ‘left’, ‘position’, ‘right’, ‘top’ | Ícone de iniciador de mídia em um estado ativo. |
| `numSidenotes` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Botão clicável que mostra o número de Sidenotes na coleção. |
| `numSidenotesPopover` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Popover com uma breve explicação de Sidenotes para o usuário. |
| `popover` | &quot;backgroundColor&quot; | Popover que é criado quando o ícone de iniciador é chamado. |
| `popoverArrowLeft` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento de seta para a esquerda no portão que aponta para o elemento DOM que contém um ícone de iniciador. |
| `popoverArrorRight` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | O elemento de seta para a direita no portão que aponta para o elemento DOM que contém um ícone de iniciador. |
| `popoverArrowTop` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | O elemento de seta superior no povir que aponta para o elemento DOM que contém um ícone de iniciador. |
| `replyAvatar` | &quot;height&quot;, &quot;width&quot; | Imagem de avatar à esquerda das notas de nível de resposta. |
| `streamPoweredBy` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;lineHeight&quot; | Rodapé &quot;acionado por&quot; no portão. |
| `streamQueueButton` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Botão para indicar quando novas notas são enviadas em um portão aberto. |
| `userAvatar` | &quot;height&quot;, &quot;width&quot; | Imagem de avatar do usuário autenticada, à esquerda do editor de área de texto. |

