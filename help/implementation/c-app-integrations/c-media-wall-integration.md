---
description: Crie um mural de mídia, com streaming de conteúdo em tempo real.
seo-description: Crie um mural de mídia, com streaming de conteúdo em tempo real.
seo-title: Mídia
solution: Experience Manager
title: Mídia
uuid: c6087c80-a35b-44d2-9dd4-ba9cd471172d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---


# Media Wall{#media-wall}

Crie um mural de mídia, com streaming de conteúdo em tempo real.

O Media Wall permite que você crie um mural social em tempo real para seu site. Use o pacote simplificado do Livefyre JavaScript SDK para exibir feeds sociais do Livefyre como uma experiência de conteúdo envolvente, em tela cheia e lado a lado, excelente para cobrir eventos ao vivo, hospedar concursos de fotos e acionar seções sociais do seu site.

## Integração {#section_jfm_bwb_c1b}

A maneira mais rápida de adicionar um mural de mídia é usar a versão incorporada hospedada no CDN da Livefyre.

Primeiro, adicione [Livefyre.js](https://github.com/Livefyre/Livefyre.js) ao seu site.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Em seguida, posicione o elemento no qual o mural de mídia aparecerá.

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

Agora você tem um Muro! Veja tudo isso em ação em [este exemplo](https://codepen.io/gobengo/pen/dFwDL).

**Ocorrência de um erro?** Verifique se você está transmitindo o parâmetro de ambiente correto. As opções incluem `livefyre.com` (produção) ou `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Qualquer personalização de estilo de Tweets renderizados pelo aplicativo Media Wall deve ser feita de acordo com os [Requisitos de exibição](https://dev.twitter.com/terms/display-requirements) do Twitter.

## Opções de configuração {#section_ucv_qvb_c1b}

`columns`

Permite que você defina o número de colunas para seu mural de mídia ao construir seu mural. Se essa opção estiver definida, a largura de cada coluna será automaticamente adaptada ao tamanho do container do Media Wall, mantendo o número especificado de colunas.

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

Permite definir a largura mínima (pixel) de cada coluna dentro do elemento de container do Media Wall. (O mural de mídia selecionará automaticamente um número apropriado de colunas, dependendo da largura do elemento de container. Por padrão, a largura do mural de mídia dividida pela largura mínima do conteúdo (300px, se indefinido) determina o número de colunas.

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

Por padrão, quando há anexos para um conteúdo, o Media Walls exibirá uma miniatura clicável. Quando clicado, o aplicativo abrirá um modal que exibe o anexo de foto/vídeo na íntegra. Para desativar essa opção, defina modal como false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Define o botão [!UICONTROL Post Content] para aparecer no mural. Essa opção exige que você passe `opts.collection` e adicione uma integração Livefyre.js Auth à página.

`postButton` parâmetros:

* `false` (padrão): Não mostrar um botão Publicar conteúdo. (Cria um mural de mídia somente leitura.)
* `true` (ou  `LiveMediaWall.postButtons.contentWithPhotos`): Inclua um botão que permite aos usuários adicionar conteúdo de texto, com fotos anexadas.

* `LiveMediaWall.postButtons.content`: Inclua um botão que permite aos usuários adicionar conteúdo de texto, mas não anexar fotos.
* `LiveMediaWall.postButtons.photo`: Inclua um botão que permite aos usuários adicionar uma foto, mas sem texto.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Define o número de itens de Conteúdo a serem adicionados ao mural quando seu botão [!UICONTROL Show More] for clicado.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Opções de configuração de estilo {#section_ztv_dvb_c1b}

O Media Wall também oferta várias opções de configuração que permitem personalizar a cor, o estilo e o tamanho do texto. Para implementar essas opções, use a seguinte sintaxe:

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

Para uma entrada válida, consulte os padrões W3C para as propriedades CSS [Família de Fontes](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Tamanho da Fonte](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Altura da Linha,](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) e [Cor](https://www.w3.org/TR/css3-color/#colorunits).

* **bodyFontSize** *(CSS Font Size String)* O tamanho da fonte do texto do corpo do conteúdo.

* **bodyLineHeight** *(CSS Line Height String)* A altura da linha para o texto do corpo do conteúdo.

* **buttonActiveBackgroundColor** *(CSS Color String)** A cor do fundo do botão no ativo.

* **buttonBorderColor** *(CSS Color String)** A cor das bordas do botão.

* **buttonHoverBackgroundColor** *(CSS Color String)* A cor do plano de fundo do botão ao passar o mouse.

* **buttonTextColor** *(CSS Color String)* A cor dos rótulos dos botões.

* **cardBackgroundColor** *(CSS Color String)* A cor de fundo dos cartões de conteúdo no mural de mídia.

* **displayNameColor** *(CSS Color String)* A cor dos nomes de exibição na linha de bytes.

* **fontFamily** *(CSS Font Family String)* A família de fontes para o texto do corpo.

* **footerTextColor** *(CSS Color String)* A cor do texto secundário (como o texto do rodapé e o nome de usuário na linha de bytes).

* **linkAttachmentBackgroundColor** *(CSS Color String)* A cor de fundo para anexos de link (anexos empilhados).

* **linkAttachmentBorderColor** *(CSS Color String)* A cor da borda dos anexos do link (anexos empilhados).

* **linkAttachmentTextColor** *(CSS Color String)* A cor do texto do anexo do link.

* **linkColor** *(CSS Color String)* A cor para hiperlinks (como links no texto do corpo e links de nome de exibição).

* **textColor** *(CSS Color String)* A cor do texto do corpo.

* **titleFontSize** *(CSS Font Size String)* O tamanho da fonte para títulos de conteúdo.

* **titleLineHeight** *(CSS Line Height String)* A altura da linha para títulos de conteúdo.

* **sourceLogoColor** *(CSS Color String)* A cor do logotipo de origem.

* **usernameColor** *(CSS Color String)* A cor dos nomes de usuário na linha de bytes.
