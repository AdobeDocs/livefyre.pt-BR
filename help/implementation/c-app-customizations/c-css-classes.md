---
description: Use as classes CSS disponíveis para personalizar a exibição dos aplicativos.
seo-description: Use as classes CSS disponíveis para personalizar a exibição dos aplicativos.
seo-title: Classes CSS
solution: Experience Manager
title: Classes CSS
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 1%

---


# Classes CSS{#css-classes}

Use as classes CSS disponíveis para personalizar a exibição dos aplicativos.

Disponível para Bate-papo, Comentários, Blog ao vivo, Revisões e Sidenotes.

Use o CSS para personalizar seus aplicativos Livefyre para obter uma integração mais completa com sua página, simplesmente substituindo o CSS padrão do aplicativo por sua própria folha de estilos. Esta seção descreve as personalizações de CSS disponíveis.

* [Editor CSS](#c_css_classes/section_edx_prh_xz)
* [CSS de opções de classificação](#c_css_classes/section_btq_4rh_xz)
* [Comentário CSS](#c_css_classes/section_mlv_nrh_xz)
* [Comentários em destaque CSS](#c_css_classes/section_m2v_mrh_xz)
* [Comentários arquivados CSS](#c_css_classes/section_bs5_lrh_xz)
* [CSS do Notificador de Comentários](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS Classes](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editor CSS {#section_edx_prh_xz}

Use essas classes para alterar a interface do editor de postagens.

| Classe | Descrição |
|---|---|
| .fyre-comment-count | O texto que exibe o número de comentários. |
| .fyre-login-bar | A caixa delimitadora que contém a barra de logon e as opções. |
| .fyre-live-container | A caixa delimitadora em torno do número de pessoas ouvindo e seus avatares. |
| .fyre-editor | A caixa delimitadora em torno do container .fyre-login-bar, .fyre-live-bar e a área de texto onde os usuários escrevem seus comentários. |
| .fyre-stream-sort | A caixa delimitadora em torno das opções de classificação. |

Você também pode editar estilos na própria configuração do aplicativo, incluindo a cor de fundo do campo do editor e a cor, o tamanho e a família da fonte do texto que aparece dentro do editor.

Para personalizar o editor de comentários, adicione o objeto editorCss:{} a fyre.console.load() e inclua o estilo desejado. Por exemplo, para atualizar o editor com seu CSS personalizado:

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## Opções de classificação CSS {#section_btq_4rh_xz}

| Classe | Descrição |
|---|---|
| .fyre-stream-sort | Todas as opções de classificação div. |
| .fyre-stream-sort-newest | A opção &quot;Mais recente&quot;. |
| .fyre-stream-sort-dest | A opção &quot;Mais antigo&quot;. |
| .fyre-stream-sort-bar | A barra separadora entre as opções. |
| .fyre-stream-sort-seleted | A opção de classificação atualmente selecionada. |

Estrutura HTML:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Ocultar as opções de classificação ‘|’ que separam as opções.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Comentário CSS {#section_mlv_nrh_xz}

| Classe | Descrição |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | O Livefyre criará uma classe CSS neste formato para cada tag de usuário adicionada pelo Livefyre’s Studio, [Perfil Sync](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Essa classe pode ser usada para criar o estilo do plano de fundo de qualquer conteúdo publicado por contas de usuário, incluindo essa tag. |
| .fyre-tag-content-icon- *`tag name`* | O Livefyre criará uma classe CSS neste formato para cada tag de conteúdo adicionada por meio do Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Essa classe pode ser usada para criar o estilo de qualquer conteúdo ao qual você tenha adicionado a tag. |
| .fyre-comment-user | A caixa delimitadora que contém a imagem de perfil do usuário. |
| .fyre-comment-username | O nome de usuário. |
| .fyre-moderador | A caixa delimitadora do moderador. |
| .fyre-comment | Caixa delimitadora em torno do texto/link do comentário. |
| .fyre-comment-article | A caixa delimitadora para todo o conteúdo do comentário. |
| .fyre-comment-date | A tag anexada ao elemento &quot;tempo desde a publicação&quot;. |
| .fyre-comment-media | A caixa delimitadora em torno do conteúdo de mídia. |
| .fyre-comment-actions | A caixa delimitadora em torno das ações disponíveis para fazer um comentário. |
| .fyre-comment-like | A caixa delimitadora em torno do link &quot;Curtir&quot;. |
| .fyre-comment-reply | A caixa delimitadora em torno do link &quot;Responder&quot;. |

## Comentários em destaque CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>Todas as classes CSS de Comentários também podem ser aplicadas ao Conteúdo em destaque.

| Classe | Descrição |
|---|---|
| .fyre-feature-content-wrapper | O container div para o leitor. |
| .fyre-feature-header | A barra de título à esquerda. |
| .fyre-feature-header-icon | O ícone de preenchimento do cabeçalho. |
| .fyre-feature-title | O texto do cabeçalho. |
| .fyre-feature-body | O container div para conteúdo em destaque no leitor. |
| .fyre-feature-quote | O ícone de citação que inicia cada item de conteúdo. |

## Comentários arquivados CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>Todas as classes CSS de conteúdo também podem ser aplicadas ao conteúdo arquivado.

| Classe | Descrição |
|---|---|
| .fyre-archive-stream-title | O texto &quot;Do Arquivo&quot;. |
| .fyre-archive-stream-title-icon | O logotipo do cabeçalho &quot;Do arquivo&quot;. |

## Notificador de comentários CSS {#section_dy4_krh_xz}

Essas classes permitem que você personalize o Livefyre Comment Notifier.

| Classe | Descrição |
|---|---|
| .fyre-notification | O div para o item de lista (tanto novo quanto conteúdo de arquivamento). |
| .fyre-notificador | O invólucro do conteúdo do Notificador. |
| .fyre-notificador-archive | O invólucro para todo o novo conteúdo que não seja a publicação mais recente. |
| .fyre-notificador-avatar | A imagem do avatar. |
| .fyre-notificador-avatar-container | O container div para o avatar do usuário. Permite definir o posicionamento. |
| .fyre-notificador-sombreamento de avatar | O sombreamento para o avatar div. |
| .fyre-notificador-banner | O container para o conteúdo de pré-visualização do Notificador, que exibe o avatar do usuário e um trecho de conteúdo para o item postado mais recentemente. |
| .fyre-notificador-base | O container da parte informativa do Notificador, que lista o número de novos comentários, a legenda do Notificador e o botão Fechar. |
| .fyre-notificador-base-close | O container div para o botão Fechar (x) do Notificador. |
| .fyre-notificador-sombra base | O sombreamento para a base do Notificador. |
| .fyre-notificador-caption | O texto apresentado ao notificador. &quot;Novo(s) comentário(s)&quot; por padrão. |
| .fyre-notificador-close | Botão que fecha o notificador. |
| .fyre-notificador-container | O container para o Notificador inclui o banner e a base. |
| .fyre-notificador-counter | O container do número listado no Notificador. |
| .fyre-notificador-lista | O container do conteúdo mais recente. |
| .fyre-notificador-message | Os primeiros ~30 caracteres do conteúdo exibido. |
| .fyre-notificador-message-container | O container div para a mensagem de cabeçalho. |
