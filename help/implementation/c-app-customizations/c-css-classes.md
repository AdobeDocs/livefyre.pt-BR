---
description: Use classes CSS disponíveis para personalizar seus aplicativos.
seo-description: Use classes CSS disponíveis para personalizar seus aplicativos.
seo-title: Classes CSS
solution: Experience Manager
title: Classes CSS
uuid: 8714 e 7 e 5-3858-458 f-a 464-de 87 fd 2 f 0 ff 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Classes CSS{#css-classes}

Use classes CSS disponíveis para personalizar seus aplicativos.

Disponível para bate-papo, comentários, blog ao vivo, revisões e auxiliares.

Use o CSS para personalizar seus aplicativos do Livefyre para obter uma integração mais completa com sua página, substituindo simplesmente o CSS de aplicativo padrão pela sua própria folha de estilo. Esta seção descreve as personalizações de CSS disponíveis.

* [Editor CSS](#c_css_classes/section_edx_prh_xz)
* [CSS de opções de classificação](#c_css_classes/section_btq_4rh_xz)
* [CSS de comentário](#c_css_classes/section_mlv_nrh_xz)
* [CSS de comentários em destaque](#c_css_classes/section_m2v_mrh_xz)
* [CSS de comentários arquivados](#c_css_classes/section_bs5_lrh_xz)
* [CSS do notificador do comentário](#c_css_classes/section_dy4_krh_xz)
* [Classes CSS de Storify](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editor CSS {#section_edx_prh_xz}

Use essas classes para alterar a interface do editor de postagem.

| Classe | Descrição |
|---|---|
| . fyre-comment-count | O texto exibindo o número de comentários. |
| . fyre-login-bar | A caixa delimitadora que contém a barra de logon e as opções. |
| . fyre-live-container | A caixa delimitadora em torno do número de pessoas que escutam e seus avatars. |
| . fyre-editor | A caixa delimitadora em torno da barra de login. fyre-live. fyre-live-container e a área de texto em que os usuários gravam seus comentários. |
| . fyre-stream-sort | A caixa delimitadora ao redor das opções de classificação. |

Você também pode editar estilos na própria configuração do aplicativo, incluindo a cor de fundo do campo do editor, e a cor, o tamanho e a família da fonte do texto que aparece dentro do editor.

Para personalizar o editor de comentários, adicione editorcss: {} objeto a fyre. conv. load () e inclua o estilo desejado. Por exemplo, para atualizar o editor com o CSS personalizado:

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

## CSS de opções de classificação {#section_btq_4rh_xz}

| Classe | Descrição |
|---|---|
| . fyre-stream-sort | As opções de classificação inteira div. |
| . fyre-stream-sort-newest | A opção «Mais recentes». |
| . fyre-stream-sort-older | A opção «Mais antiga». |
| . fyre-stream-bar-bar | A barra separadora entre as opções. |
| . fyre-stream-sort-selected | A opção de classificação atualmente selecionada. |

Estrutura HTML:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Ocultar o|' separando as opções de classificação.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## CSS de comentário {#section_mlv_nrh_xz}

| Classe | Descrição |
|---|---|
| . fyre-comment-author-tag- *`custom tag name`* | O Livefyre criará uma classe CSS nesse formato para cada tag de usuário adicionada por meio do Studio Yre, Sincronização [de perfil](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Essa classe pode ser usada para estilo do plano de fundo para qualquer conteúdo postado por contas de usuário incluindo essa tag. |
| . fyre-tag-content-icon- *`tag name`* | O Livefyre criará uma classe CSS nesse formato para cada tag de conteúdo adicionada por meio do Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Essa classe pode ser usada para estilo de qualquer conteúdo ao qual você tenha adicionado a tag. |
| . fyre-comment-user | A caixa delimitadora que contém a foto do perfil do usuário. |
| . fyre-comment-username | O nome do usuário. |
| . fyre-moderator | A caixa delimitadora do moderador. |
| . fyre-comment | Caixa delimitadora em torno do texto/link do comentário. |
| . fyre-comment-article | A caixa delimitadora para todo o conteúdo do comentário. |
| . fyre-comment-date | A tag anexada ao elemento «time desde postado». |
| . fyre-comment-media | A caixa delimitadora em torno do conteúdo da mídia. |
| . fyre-comment-actions | A caixa delimitadora ao redor das ações disponíveis para realizar um comentário. |
| . fyre-comment-like | A caixa delimitadora em torno do link «Curtir». |
| . fyre-comment-response | A caixa delimitadora em torno do link «Responder». |

## CSS de comentários em destaque {#section_m2v_mrh_xz}

>[!NOTE]
>
>Todas as classes CSS de comentário também podem ser aplicadas ao Conteúdo em destaque.

| Classe | Descrição |
|---|---|
| . fyre-feem-content-wrapper | O contêiner div para o leitor. |
| . fyre-feer-header | A barra de título principal. |
| . fyre-feer-icon | O ícone do questionário do cabeçalho. |
| . fyre-feem-título | O texto do cabeçalho. |
| . fyre-feem-body | O contêiner div para conteúdo em destaque no leitor. |
| . fyre-featured-quote | O ícone de aspas que inicia cada item de conteúdo. |

## CSS de comentários arquivados {#section_bs5_lrh_xz}

>[!NOTE]
>
>Todas as classes CSS de conteúdo também podem ser aplicadas ao conteúdo arquivado.

| Classe | Descrição |
|---|---|
| . fyre-archive-stream-title | O texto «Do arquivo morto». |
| . fyre-archive-stream-title-ícone | O logotipo para o cabeçalho «No arquivo morto». |

## CSS do notificador do comentário {#section_dy4_krh_xz}

Essas classes permitem personalizar o Notificador do comentário do Livefyre.

| Classe | Descrição |
|---|---|
| . fyre-notification | Div para o item de lista (novo e arquivamento de conteúdo). |
| . fyre-notificador | O invólucro do conteúdo do notificador. |
| . fyre-notificador-archive | O invólucro para todos os novos conteúdos que não sejam a publicação mais recente. |
| . fyre-notificador-avatar | A imagem para o avatar. |
| . fyre-notificador-avatar-container | O contêiner div para o avatar do usuário. Permite definir o posicionamento. |
| . fyre-notificador-avatar-shading | O sombreamento para o avatar div. |
| . fyre-notificador-banner | O contêiner do conteúdo de visualização do notificador, que exibe o avatar do usuário e um trecho de conteúdo do item publicado mais recentemente. |
| . fyre-notificador-base | O contêiner para a parte de informações do notificador, que lista o número de novos comentários, a legenda do notificador e o botão Fechar. |
| . fyre-notificador-base-close | O contêiner div para o botão fechar (x) para o notificador. |
| . fyre-notificador-base-shadow | O sombreamento para a base de notificador. |
| . fyre-notificador-caption | O texto exibido para o notificador. «Novo comentário (s)» por padrão. |
| . fyre-notificador-close | Um botão que fecha o notificador. |
| . fyre-notificador-container | O contêiner do notificador inclui o banner e a base. |
| . fyre-notificador-counter | O contêiner do número listado no Notificador. |
| . fyre-notificador-list | O contêiner do conteúdo mais recente. |
| . fyre-notificador-message | Os primeiros ~ 30 caracteres do conteúdo exibidos. |
| . fyre-notificador-message-container | O contêiner div para a mensagem do cabeçalho. |
