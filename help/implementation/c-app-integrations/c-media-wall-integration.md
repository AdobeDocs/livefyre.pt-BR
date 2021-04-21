---
description: Crie um mural de mídia, com transmissão de conteúdo em tempo real.
title: Mural de mídia
exl-id: 597af7e1-9ada-4893-9071-e17c21ef0d04
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Mural de mídia{#media-wall}

Crie um mural de mídia, com transmissão de conteúdo em tempo real.

Mural de mídia permite que você crie um mural social em tempo real para seu site. Use o pacote de fluxo do Livefyre JavaScript SDK para exibir os feeds sociais do Livefyre como uma experiência de conteúdo com tela cheia, envolvente visualmente, excelente para cobrir eventos ao vivo, hospedar concursos de fotos e ativar seções sociais do seu site.

## Integração {#section_jfm_bwb_c1b}

A maneira mais rápida de adicionar um Mural de mídia é usar a versão criada hospedada no CDN da Livefyre.

Primeiro, adicione [Livefyre.js](https://github.com/Livefyre/Livefyre.js) ao seu site.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Em seguida, posicione o elemento no qual o Mural de mídia será exibido.

```
<div id="wall"></div>
```

Finalmente, use `Livefyre.require` para construir o componente.

```
<script> 
Livefyre.require([ 
    'streamhub-wall#5' 
], function(MediaWall) {     
    var wall = window.wall = new MediaWall({ 
        el: document.getElementById("wall"), 
        collection: { 
            "network": "client-solutions.fyre.co", 
            "siteId": "364309", 
            "articleId": "answers-mediawall" 
        } 
    }); 
}); 
</script>
```

Agora você tem um mural! Veja tudo isso em ação em [este exemplo](https://codepen.io/gobengo/pen/dFwDL).

**Ocorreu um erro?** Verifique se você está transmitindo o parâmetro de ambiente correto. As opções incluem `livefyre.com` (produção) ou `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Qualquer personalização de estilo de Tweets renderizados pelo seu Aplicativo de mural de mídia deve ser feita de acordo com os [Requisitos de exibição](https://dev.twitter.com/terms/display-requirements) da Twitter.

## Opções de configuração {#section_ucv_qvb_c1b}

`columns`

Permite definir o número de colunas para o Mural de mídia ao construir o mural. Se essa opção estiver definida, a largura de cada coluna será automaticamente adaptada ao tamanho do contêiner do Mural de mídia, mantendo o número especificado de colunas.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

O número de itens de Conteúdo a serem renderizados no carregamento da página. O padrão é 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Permite definir a largura mínima (pixel) de cada coluna dentro do elemento de contêiner do Mural de mídia. (O mural de mídia selecionará automaticamente um número apropriado de colunas, dependendo da largura do elemento do contêiner. Por padrão, a largura do mural de mídia dividida pela largura mínima do conteúdo (300px, se indefinido) determina o número de colunas.

>[!NOTE]
>
>Não use essa opção em combinação com a opção de colunas.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Por padrão, quando há anexos para um conteúdo, os Mural de mídia exibirão uma miniatura clicável. Quando clicado, o aplicativo abrirá uma modal que exibe o anexo de foto/vídeo na totalidade. Para desativar essa opção, defina modal como false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Define o botão [!UICONTROL Post Content] para aparecer no mural. Essa opção requer que você passe `opts.collection` e adicione uma integração Livefyre.js Auth à página.

`postButton` parâmetros:

* `false` (padrão): Não mostrar um botão Publicar conteúdo . (Cria um mural de mídia somente leitura.)
* `true` (ou  `LiveMediaWall.postButtons.contentWithPhotos`): Inclua um botão que permita aos usuários adicionar conteúdo de texto, com fotos anexadas.

* `LiveMediaWall.postButtons.content`: Inclua um botão que permita aos usuários adicionar conteúdo de texto, mas não anexar fotos.
* `LiveMediaWall.postButtons.photo`: Inclua um botão que permita aos usuários adicionar uma foto, mas sem texto.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Define o número de itens de Conteúdo a serem adicionados ao mural quando o botão [!UICONTROL Show More] for clicado.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Opções de configuração de estilo {#section_ztv_dvb_c1b}

O Mural de mídia também oferece várias opções de configuração que permitem personalizar a cor, o estilo e o tamanho do texto. Para implementar essas opções, use a seguinte sintaxe:

```
var wall2 = window.wall2 = new MediaWall({ 
   el: document.getElementById("listView1"), 
   collection: collection, 
   cardBackgroundColor: '#333', 
   textColor: 'magenta', 
   linkColor: 'orange', 
   footerTextColor: 'lime', 
   displayNameColor: 'cyan', 
   usernameColor: 'red', 
   fontFamily: 'Helvetica, Arial', 
   linkAttachmentBackgroundColor: '#555', 
   linkAttachmentBorderColor: '#888' 
}); 
```

Para entrada válida, consulte os padrões W3C para as propriedades CSS [Família de Fontes](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Tamanho da Fonte](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Altura da Linha,](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) e [Cor](https://www.w3.org/TR/css3-color/#colorunits).

* **bodyFontSize** *(CSS Font Size String)* O tamanho da fonte do texto do corpo do conteúdo.

* **bodyLineHeight** *(CSS Line Height String)* A altura da linha para o texto do corpo do conteúdo.

* **buttonAtiveBackgroundColor** *(CSS Color String)** A cor do plano de fundo do botão no ativo.

* **buttonBorderColor** *(CSS Color String)** A cor das bordas do botão.

* **buttonHoverBackgroundColor** *(CSS Color String)* A cor do plano de fundo do botão ao passar o mouse.

* **buttonTextColor** *(CSS Color String)* A cor dos rótulos de botão.

* **cardBackgroundColor** *(CSS Color String)* A cor de fundo dos cartões de conteúdo no mural de mídia.

* **displayNameColor** *(CSS Color String)* A cor dos nomes de exibição na linha de bytes.

* **fontFamily** *(CSS Font Family String)* A família da fonte para o texto do corpo.

* **footerTextColor** *(CSS Color String)* A cor do texto secundário (como o texto do rodapé e o nome de usuário na linha de bytes).

* **linkAttachmentBackgroundColor** *(CSS Color String)* A cor de fundo dos anexos do link (anexos empilhados).

* **linkAttachmentBorderColor** *(CSS Color String)* A cor da borda dos anexos do link (anexos empilhados).

* **linkAttachmentTextColor** *(CSS Color String)* A cor do texto do anexo do link.

* **linkColor** *(CSS Color String)* A cor dos hiperlinks (como links no texto do corpo e links de nome de exibição).

* **textColor** *(CSS Color String)* A cor do texto do corpo.

* **titleFontSize** *(CSS Font Size String)* O tamanho da fonte para títulos de conteúdo.

* **titleLineHeight** *(CSS Line Height String)* A altura da linha para títulos de conteúdo.

* **sourceLogoColor** *(CSS Color String)* A cor do logotipo de origem.

* **usernameColor** *(CSS Color String)* A cor dos nomes de usuário na linha de bytes.
