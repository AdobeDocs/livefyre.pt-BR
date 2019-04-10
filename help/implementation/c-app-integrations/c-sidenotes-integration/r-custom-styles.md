---
description: Os estilos personalizados são aplicados por meio de um objeto inserido
  no construtor de Sidenotes.
seo-description: Os estilos personalizados são aplicados por meio de um objeto inserido
  no construtor de Sidenotes.
seo-title: Auxiliar estilos personalizados
title: Auxiliar estilos personalizados
uuid: 0 f 6 d 7 ad 6-1 f 6 a -4 ed 2-b 86 a -0 d 03782 e 591 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

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
| `blockBtn` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | O «ícone do iniciador» foi colocado ao lado dos elementos especificados como sidenote-able. |
| `blockBtnActive` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Ícone Inicializador quando em um estado ativo. |
| `commentAvatar` | «height», «width» | Imagem de avatar à esquerda das notas de nível superior. |
| `commentBody` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Corpo de texto de notas encadeadas. |
| `commentDisplayName` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Nome de exibição do usuário que deixou uma nota. |
| `commentDownvote` | ' Fontcolor ',' fontsize ' | Botão Votar em uma nota. |
| `commentReplyExpand` | ' Backgroundcolor ',' bordercolor ',' borderwidth ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Botão para expandir threads com um grande número de respostas. |
| `commentTags` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Tags sobre um usuário em uma nota. |
| `commentUpvote` | ' Fontcolor ',' fontsize ' | Botão Upvotar em uma nota. |
| `editorTextarea` | «height», «width», «fontcolor», «fontfamily», «fontsize», «fontweight», «lineheight» | Caixa de entrada de textarea para deixar notas. |
| `mediaBlockBtn` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Ícone de inicialização de mídia quando um item de mídia é colocado na parte superior (img, vídeo). |
| `mediaBlockBtnActive` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Ícone de inicialização de mídia em um estado ativo. |
| `numSidenotes` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ',' backgroundcolor ',' bordercolor ',' borderwidth ',' height ',' width ' | Botão clicável que mostra o número de auxiliares na coleção. |
| `numSidenotesPopover` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ',' backgroundcolor ',' bordercolor ',' borderwidth ',' height ',' width ' | Popover com uma breve explicação de Sidenotes para o usuário. |
| `popover` | ' Backgroundcolor ' | Popover que é levantado quando o ícone do iniciador é chamado. |
| `popoverArrowLeft` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | Elemento de seta para a esquerda no popover que aponta para o elemento DOM contendo um ícone de inicialização. |
| `popoverArrorRight` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | Elemento de seta para a direita no popover que aponta para o elemento DOM contendo um ícone de inicialização. |
| `popoverArrowTop` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | Elemento de seta superior no popover que aponta para o elemento DOM contendo um ícone de inicialização. |
| `replyAvatar` | «height», «width» | Imagem de avatar à esquerda das notas de nível de resposta. |
| `streamPoweredBy` | ' Backgroundcolor ',' bordercolor ',' lineheight ' | «Ativado por» no popover. |
| `streamQueueButton` | ' Backgroundcolor ',' bordercolor ',' borderwidth ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Botão para indicar quando o fluxo de notas novas em um popover aberto. |
| `userAvatar` | «height», «width» | Imagem de avatar do usuário autenticado, à esquerda do editor de área de texto. |

