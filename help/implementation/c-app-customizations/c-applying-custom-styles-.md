---
description: Para criar um estilo personalizado de conteúdo para grupos de usuários, primeiro adicione uma tag de usuário à conta e, em seguida, crie um estilo no conteúdo usando CSS.
title: Aplicação de estilos personalizados
exl-id: 54692525-32ce-487a-b3c3-da1261b58da1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Aplicar estilos personalizados{#applying-custom-styles}

Para criar um estilo personalizado de conteúdo para grupos de usuários, primeiro adicione uma tag de usuário à conta e, em seguida, crie um estilo no conteúdo usando CSS.

Para cada tag de usuário adicionada pelo Studio ou Ping for Pull, o Livefyre criará duas classes CSS, que podem ser usadas para criar um estilo no conteúdo do grupo.

Ao converter Tags de usuário em classes CSS:

* Livefyre cria duas classes: tag-autor-autor-***&lt;grupo_alvo>*** e fyre-tag-author-***&lt;grupo_alvo>***. Ambos podem ser usados para criar estilo no conteúdo.

* Quaisquer espaços incluídos na tag serão convertidos em sublinhados. Por exemplo: O &#39;Usuário favorito&#39; se tornará o favorito_usuário.
* Os caracteres Unicode incluídos nos nomes de grupo não serão convertidos e aparecerão como Unicode nos nomes de classe. Por exemplo: O grupo de utilizadores &quot;modérateur&quot; tornar-se-á fyre-comment-author-tag-modérateur.

Depois que os grupos de usuários tiverem sido criados, use as classes CSS do Livefyre para aplicar o estilo personalizado ao conteúdo.

## Conteúdo de estilo para Moderadores (e Proprietários) {#section_vjv_2cv_xz}

* Use a classe CSS .fyre-moderator.

   >[!NOTE]
   >
   >Os proprietários, por serem também moderadores, terão essa classe aplicada ao seu conteúdo no stream.

* Crie uma regra CSS para mostrar ou criar um estilo para um símbolo do Grupo:

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

Crie uma regra CSS para mostrar ou criar um estilo para um símbolo do Grupo:

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

Use a marca fyre-author-tag de classe CSS-***&lt;your_group>*** ou fyre-tag-author-***&lt;your_group>*** para criar um estilo com a fonte e o plano de fundo de cada item postado de uma Conta associada à tag selecionada.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```
