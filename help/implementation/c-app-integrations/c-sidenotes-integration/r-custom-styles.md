---
description: Os estilos personalizados são aplicados por meio de um objeto inserido no construtor de Sidenotes.
seo-description: Os estilos personalizados são aplicados por meio de um objeto inserido no construtor de Sidenotes.
seo-title: Auxiliar estilos personalizados
title: Auxiliar estilos personalizados
uuid: 0 f 6 d 7 ad 6-1 f 6 a -4 ed 2-b 86 a -0 d 03782 e 591 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Auxiliar estilos personalizados{#sidenotes-custom-styles}

Os estilos personalizados são aplicados por meio de um objeto inserido no construtor de Sidenotes.

As «teclas» são chaves de objeto que representam elementos DOM, enquanto «propriedades» são propriedades CSS suportadas para a chave específica. Por exemplo, para personalizar o estilo do blockbtn (que é o botão que inicia o popover de sidenotes), uma seria construir um objeto como:

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
| `anonymousAvatar` | «height», «width» | Imagem de avatar anônima, à esquerda do editor de área de texto. |
| `blockBtn` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | O «ícone do iniciador» foi colocado ao lado dos elementos especificados como sidenote-able. |
| `blockBtnActive` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Ícone Inicializador quando em um estado ativo. |
| `commentAvatar` | «height», «width» | Imagem de avatar à esquerda das notas de nível superior. |
| `commentBody` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Corpo de texto de notas encadeadas. |
| `commentDisplayName` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Nome de exibição do usuário que deixou uma nota. |
| `commentDownvote` | &#39; Fontcolor &#39;,&#39; fontsize &#39; | Botão Votar em uma nota. |
| `commentReplyExpand` | &#39; Backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Botão para expandir threads com um grande número de respostas. |
| `commentTags` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Tags sobre um usuário em uma nota. |
| `commentUpvote` | &#39; Fontcolor &#39;,&#39; fontsize &#39; | Botão Upvotar em uma nota. |
| `editorTextarea` | «height», «width», «fontcolor», «fontfamily», «fontsize», «fontweight», «lineheight» | Caixa de entrada de textarea para deixar notas. |
| `mediaBlockBtn` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Ícone de inicialização de mídia quando um item de mídia é colocado na parte superior (img, vídeo). |
| `mediaBlockBtnActive` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Ícone de inicialização de mídia em um estado ativo. |
| `numSidenotes` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39;,&#39; backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; height &#39;,&#39; width &#39; | Botão clicável que mostra o número de auxiliares na coleção. |
| `numSidenotesPopover` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39;,&#39; backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; height &#39;,&#39; width &#39; | Popover com uma breve explicação de Sidenotes para o usuário. |
| `popover` | &#39; Backgroundcolor &#39; | Popover que é levantado quando o ícone do iniciador é chamado. |
| `popoverArrowLeft` | &#39; Backgroundimage &#39;,&#39; height &#39;,&#39; left &#39;,&#39; right &#39;,&#39; top &#39;,&#39; width &#39; | Elemento de seta para a esquerda no popover que aponta para o elemento DOM contendo um ícone de inicialização. |
| `popoverArrorRight` | &#39; Backgroundimage &#39;,&#39; height &#39;,&#39; left &#39;,&#39; right &#39;,&#39; top &#39;,&#39; width &#39; | Elemento de seta para a direita no popover que aponta para o elemento DOM contendo um ícone de inicialização. |
| `popoverArrowTop` | &#39; Backgroundimage &#39;,&#39; height &#39;,&#39; left &#39;,&#39; right &#39;,&#39; top &#39;,&#39; width &#39; | Elemento de seta superior no popover que aponta para o elemento DOM contendo um ícone de inicialização. |
| `replyAvatar` | «height», «width» | Imagem de avatar à esquerda das notas de nível de resposta. |
| `streamPoweredBy` | &#39; Backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; lineheight &#39; | «Ativado por» no popover. |
| `streamQueueButton` | &#39; Backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Botão para indicar quando o fluxo de notas novas em um popover aberto. |
| `userAvatar` | «height», «width» | Imagem de avatar do usuário autenticado, à esquerda do editor de área de texto. |

