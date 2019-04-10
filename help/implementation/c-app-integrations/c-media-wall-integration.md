---
description: Crie um mural de mídia com streaming de conteúdo em tempo real.
seo-description: Crie um mural de mídia com streaming de conteúdo em tempo real.
seo-title: Media Wall
solution: Experience Manager
title: Media Wall
uuid: c 6087 c 80-a 35 b -44 d 2-9 dd 4-ba 9 cd 471172 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Media Wall{#media-wall}

Crie um mural de mídia com streaming de conteúdo em tempo real.

O Media Wall permite criar um mural social em tempo real para seu site. Use o pacote de wallhub do Livefyre do Livefyre para exibir os feeds sociais do Livefyre como uma experiência de conteúdo visualmente envolvente, de tela cheia, que é excelente para abranger os eventos ao vivo, hospedar os concursos de fotos e aprimorar as seções sociais de seu site.

## Integração {#section_jfm_bwb_c1b}

A maneira mais rápida de adicionar um Media Wall é usar a versão incorporada hospedada no CDN do Livefyre.

Primeiro, adicione [Livefyre. js](https://github.com/Livefyre/Livefyre.js) ao seu site.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Em seguida, posicione o elemento no qual o mural de mídia será exibido.

```
<div id="wall"></div>
```

Por fim, use `Livefyre.require` para criar o componente.

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

Agora você tem um mural! Veja isso tudo em ação [neste exemplo](https://codepen.io/gobengo/pen/dFwDL).

**Encontrou um erro?** Verifique se você está transmitindo o parâmetro de ambiente correto. As opções incluem `livefyre.com` (produção) ou `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Qualquer personalização de estilo de tweets renderizados pelo seu aplicativo de Dynamic Wall deve ser feita de acordo com as Exigências [de exibição do Twitter](https://dev.twitter.com/terms/display-requirements).

## Opções de configuração {#section_ucv_qvb_c1b}

`columns`

Permite definir o número de colunas para seu mural de mídia ao construir seu mural. Se essa opção estiver definida, a largura de cada coluna será ajustada automaticamente ao tamanho do contêiner do Media Wall, mantendo o número especificado de colunas.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

O número de itens de conteúdo a serem renderizados na carga da página. Padrões para 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Permite definir a largura mínima (pixel) para cada coluna no elemento de contêiner do Wall Wall. (O seu mural de mídia seleciona automaticamente um número apropriado de colunas, dependendo da largura do elemento de contêiner. Por padrão, a largura do mural do media wall dividida pela largura mínima do conteúdo (300 px, se indefinido) determina o número de colunas.)

>[!NOTE]
>
>Não use essa opção em combinação com a opção Colunas.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Por padrão, quando há anexos para um conteúdo, os Dynamic Walls exibem uma miniatura clicável. Quando clicado, o aplicativo abrirá um modal exibindo o anexo de foto/vídeo em sua totalidade. Para desativar essa opção, defina modal como false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Define o [!UICONTROL Post Content] botão para aparecer em seu mural. Essa opção requer a passagem `opts.collection`e adição de uma integração do Livefyre. js à página.

`postButton` parâmetros:

* `false` (padrão): Não mostrar um botão Conteúdo da postagem. (Cria um mural de mídia somente leitura.)
* `true` (ou `LiveMediaWall.postButtons.contentWithPhotos`): Inclua um botão que permita aos usuários adicionar conteúdo de texto, com fotos anexadas.

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

Define o número de itens de conteúdo a serem adicionados ao mural quando o [!UICONTROL Show More] botão é clicado.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Opções de configuração de estilo {#section_ztv_dvb_c1b}

O Media Wall também oferece várias opções de configuração que permitem personalizar a cor, o estilo e o tamanho do texto. Para implementar essas opções, use a seguinte sintaxe:

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

Para entrada válida, consulte os padrões W 3 C para Família de [fontes CSS](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Tamanho da fonte](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Altura da linha e](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) [Cor de cor](https://www.w3.org/TR/css3-color/#colorunits) .

* **Bodyfontsize** *(String de tamanho da fonte CSS)* O tamanho da fonte do texto do corpo do conteúdo.

* **Bodylineheight** *(String de altura da linha CSS)* A altura da linha para o texto do corpo do conteúdo.

* **Buttonactivebackgroundcolor** *(CSS Color String)** A cor para o plano de fundo do botão ativado.

* **Buttonbordercolor** *(String de cor CSS)** A cor das bordas do botão.

* **Buttonhoverbackgroundcolor** *(CSS Color String)* A cor do plano de fundo do botão ao passar o mouse.

* **Buttontextcolor** *(String de cor CSS)* A cor dos rótulos de botão.

* **Cardbackgroundcolor** *(String de cor CSS)* A cor de fundo para cartões de conteúdo no mural de mídia.

* **Displaynamecolor** *(String de cor CSS)* A cor para nomes de exibição na linha de identificação do byte.

* **Fontfamily** *(String familiar da família de CSS)* A família de fontes do texto do corpo.

* **Footertextcolor** *(String de cor CSS)* A cor do texto secundário (como o texto do rodapé e o nome de usuário na linha de identificação do autor).

* **Linkattachmentbackgroundcolor** *(CSS Color String)* A cor de fundo para anexos de link (anexos empilhados).

* **Linkattachmentbordercolor** *(String de cor CSS)* A cor da borda dos anexos de link (anexos empilhados).

* **Linkattachmenttextcolor** *(String de cor CSS)* A cor do texto do anexo do link.

* **Linkcolor** *(String de cor CSS)* A cor para hiperlinks (como links no texto do corpo e links de nome de exibição).

* **Textcolor** *(String de cor CSS)* A cor do texto do corpo.

* **Titlefontsize** *(String de tamanho da fonte CSS)* O tamanho da fonte para títulos de conteúdo.

* **Titlelineheight** *(String de altura da linha CSS)* A altura da linha para títulos de conteúdo.

* **Sourcelogocolor** *(String de cor CSS)* A cor para o logotipo de origem.

* **Usernamecolor** *(String de cor CSS)* A cor para os nomes de usuário na linha de identificação do byte.
