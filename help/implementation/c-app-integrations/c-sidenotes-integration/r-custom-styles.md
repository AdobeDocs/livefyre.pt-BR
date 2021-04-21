---
description: Os estilos personalizados são aplicados por meio de um objeto inserido no construtor Sidenotes .
title: Indica Estilos Personalizados
exl-id: 846605b7-a21e-4600-bf17-18841d2ed96d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Indica Estilos Personalizados{#sidenotes-custom-styles}

Os estilos personalizados são aplicados por meio de um objeto inserido no construtor Sidenotes .

As &quot;chaves&quot; são chaves de objeto que representam elementos DOM, enquanto as &quot;propriedades&quot; são propriedades CSS compatíveis com a chave específica. Por exemplo, para personalizar o estilo do blockBtn (que é o botão que inicia o portátil Sidenotes), é possível construir um objeto como:

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
| `anonymousAvatar` | &quot;altura&quot;, &quot;largura&quot; | Imagem de avatar anônima, à esquerda do editor de área de texto. |
| `blockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | O &quot;ícone do Iniciador&quot; posicionado ao lado dos elementos especificados como compatíveis com observações. |
| `blockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Ícone do Iniciador quando em um estado ativo. |
| `commentAvatar` | &quot;altura&quot;, &quot;largura&quot; | Imagem de avatar à esquerda das notas de nível superior. |
| `commentBody` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Corpo de texto das notas encadeadas. |
| `commentDisplayName` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Exibir nome do usuário que deixou uma nota. |
| `commentDownvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Botão Baixar a votação em uma nota. |
| `commentReplyExpand` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Botão para expandir threads com um grande número de respostas. |
| `commentTags` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Tags sobre um usuário em uma nota. |
| `commentUpvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Botão Votar em cima de uma nota. |
| `editorTextarea` | &quot;height&quot;, &quot;width&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Caixa de entrada de área de texto para deixar notas. |
| `mediaBlockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Ícone do Media Launch quando exibido sobre um item de mídia (img, vídeo). |
| `mediaBlockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Ícone Media launcher em um estado ativo. |
| `numSidenotes` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Botão Clicável que mostra o número de Observações na coleção. |
| `numSidenotesPopover` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Pover com uma breve explicação de observações para o usuário. |
| `popover` | &quot;backgroundColor&quot; | Pop-ver que é criado quando o ícone do iniciador é chamado. |
| `popoverArrowLeft` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento de seta para a esquerda na janela que aponta para o elemento DOM que contém um ícone de iniciador. |
| `popoverArrorRight` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento de seta para a direita no portão que aponta para o elemento DOM que contém um ícone do iniciador. |
| `popoverArrowTop` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Elemento de seta superior no portão que aponta para o elemento DOM que contém um ícone de iniciador. |
| `replyAvatar` | &quot;altura&quot;, &quot;largura&quot; | Imagem de avatar à esquerda das notas de nível de resposta. |
| `streamPoweredBy` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;lineHeight&quot; | Rodapé &quot;Powered by&quot; na tomada. |
| `streamQueueButton` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Botão para indicar quando novas notas são transmitidas em uma janela aberta. |
| `userAvatar` | &quot;altura&quot;, &quot;largura&quot; | Imagem de avatar do usuário autenticado, à esquerda do editor de área de texto. |
