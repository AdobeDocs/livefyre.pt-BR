---
description: Para personalizar o conteúdo de estilo para Grupos de usuários, primeiro adicione uma Tag de usuário à conta e, em seguida, estilo o conteúdo usando CSS.
seo-description: Para personalizar o conteúdo de estilo para Grupos de usuários, primeiro adicione uma Tag de usuário à conta e, em seguida, estilo o conteúdo usando CSS.
seo-title: Aplicação de estilos personalizados
solution: Experience Manager
title: Aplicação de estilos personalizados
uuid: 0556aa2f-4fcd-4bde-abb5-479ec682f573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# Aplicar estilos personalizados{#applying-custom-styles}

Para personalizar o conteúdo de estilo para Grupos de usuários, primeiro adicione uma Tag de usuário à conta e, em seguida, estilo o conteúdo usando CSS.

Para cada tag de usuário adicionada pelo Studio ou Ping for Pull, o Livefyre criará duas classes CSS, que podem ser usadas para criar o estilo do conteúdo do grupo.

Ao converter tags de usuário em classes CSS:

* Livefyre cria duas classes: tag-autor-chave-***&lt;seu_grupo>**** e fyre-tag-author-***&lt;seu_grupo>***. Ambos podem ser usados para criar o estilo do conteúdo.

* Quaisquer espaços incluídos na tag serão convertidos em sublinhados. Por exemplo: &quot;Usuário favorito&quot; se tornará o favorito_usuário.
* Os caracteres Unicode incluídos nos nomes de grupos não serão convertidos e aparecerão como Unicode nos nomes de classes. Por exemplo: O grupo de utilizadores &quot;modérateur&quot; tornar-se-á fyre-comment-author-tag-modérateur.

Depois que os grupos de usuários tiverem sido criados, use as classes CSS de Livefyre para aplicar estilização personalizada ao conteúdo.

## Conteúdo de estilo para moderadores (e proprietários) {#section_vjv_2cv_xz}

* Use a classe CSS .fyre-moderator.

   >[!NOTE]
   >
   >Os proprietários, como eles também são Moderadores, terão essa classe aplicada ao conteúdo deles no fluxo também.

* Crie uma regra CSS para mostrar ou criar um estilo para um crachá do Grupo:

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## Conteúdo de estilo para grupos de usuários {#section_ghn_s1v_xz}

Crie uma regra CSS para mostrar ou criar um estilo para um crachá do Grupo:

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

Use a marca fyre-author-author-tag da classe CSS-***&lt;your_group>**** ou fyre-tag-author-****&lt;your_group>**** para criar o estilo da fonte e do plano de fundo de cada item publicado em uma Conta associada à tag selecionada.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

