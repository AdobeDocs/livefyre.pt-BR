---
description: Para o conteúdo de estilo personalizado para Grupos de usuários, você deve primeiro adicionar uma Tag de usuário à conta e, em seguida, estilo do conteúdo usando CSS.
seo-description: Para o conteúdo de estilo personalizado para Grupos de usuários, você deve primeiro adicionar uma Tag de usuário à conta e, em seguida, estilo do conteúdo usando CSS.
seo-title: Aplicação de estilos personalizados
solution: Experience Manager
title: Aplicação de estilos personalizados
uuid: 0556 aa 2 f -4 fcd -4 bde-abb 5-479 ec 682 f 573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aplicação de estilos personalizados{#applying-custom-styles}

Para o conteúdo de estilo personalizado para Grupos de usuários, você deve primeiro adicionar uma Tag de usuário à conta e, em seguida, estilo do conteúdo usando CSS.

Para cada tag de usuário adicionada por meio do Studio ou Ping para Puxar, o Livefyre criará duas classes CSS, que podem ser usadas para estilo do conteúdo do grupo.

Ao converter tags de usuário em classes CSS:

* O Livefyre cria duas classes: fyre-author-tag-*** &lt; your_ group &gt;*** e fyre-tag-***-*** &lt; your_ group &gt;***. Ambos podem ser usados para estilo do conteúdo.

* Quaisquer espaços incluídos na tag serão convertidos em sublinhados. Por exemplo: «Usuário favorito» se tornará favorite_ user.
* Os caracteres Unicode incluídos em nomes de grupos não serão convertidos e aparecerão como Unicode nos nomes de classe. Por exemplo: O grupo de usuários&#39;modérateur&#39;se tornará fyre-author-tag-tag-modérateur.

Depois de criar os grupos de usuários, use as classes CSS do Livefyre para aplicar estilo personalizado para o conteúdo.

## Conteúdo de estilo para moderadores (e proprietários) {#section_vjv_2cv_xz}

* Use o CSS class. fyre-moderator.

   >[!NOTE]
   >
   >Os proprietários, como também são Moderadores, terão essa classe aplicada ao conteúdo também no stream.

* Crie uma regra de CSS para mostrar ou estilo um selo para o grupo:

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

Crie uma regra de CSS para mostrar ou estilo um selo para o grupo:

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

Use a classe CSS fyre-tag-*** &lt; your_ group &gt;*** ou fyre-tag-author-*** &lt; your_ group &gt;*** para estilo da fonte e do plano de fundo para cada item postado de uma conta associada à tag selecionada.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

