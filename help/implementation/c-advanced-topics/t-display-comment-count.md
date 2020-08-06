---
description: Agarre as contagens de postagem e comentário para que determinadas coleções sejam exibidas em suas páginas de índice.
seo-description: Agarre as contagens de postagem e comentário para que determinadas coleções sejam exibidas em suas páginas de índice.
seo-title: Exibir contagem de comentários
solution: Experience Manager
title: Exibir contagem de comentários
uuid: 0f39b25e-11e0-4945-be71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c2594f919f153d1230b3dc0370f31d64cb698146
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Exibir contagem de comentários{#display-comment-count}

Agarre as contagens de postagem e comentário para que determinadas coleções sejam exibidas em suas páginas de índice.

O Livefyre `CommentCount.js` permite que você busque a contagem de conteúdo para coleções em seu site. Embora os Aplicativos mostrem a contagem de comentários para a coleção atual, ter essas contagens sindicalizadas no site pode ser útil. Esse recurso é especialmente útil se você não persistir no conteúdo do banco de dados (ou se o banco de dados do CMS não estiver sincronizado com o Livefyre).

1. Carregue o JavaScript.

   Para usar `CommentCount.js`, primeiro incorpore o arquivo JavaScript na `<head>` seção da página ou do modelo em que deseja usá-lo.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Vincule o elemento HTML.

   Depois que o script é carregado, ele tentará encontrar outros elementos na página com um nome de classe de `livefyre-commentcount`. Para cada um desses elementos, o script procurará por atributos `data-lf-site-id` e `data-lf-article-id` HTML, e os usará para buscar conteúdo do Livefyre e atualizar cada elemento com o valor mais recente.

   Por exemplo, o seguinte elemento seria atualizado:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >O `CommentCount.js` código verifica se há um valor numérico para atualizar com a contagem real. Certifique-se de incluir um valor numérico entre as tags.

   **Exemplo 1** (Usar o URL como a ID do artigo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Exemplo 2** (Uso de um sistema numerado como a ID do artigo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configurar opções.

   Para ter mais controle sobre como as contagens de conteúdo são substituídas, chame `LF.CommentCount()` e passe em um objeto que contém as opções de configuração. Certifique-se de chamar a função depois que todos os elementos que precisam ser substituídos estiverem no DOM. O melhor local para chamar esse método é no rodapé, portanto, isso acontece quando o DOM é carregado, mas antes dos eventos prontos para documentos e janelas.

   Permitimos as seguintes opções de configuração:

* **substituto:** Função ou Regex usado para substituir o texto de cada contagem de conteúdo.

* **função:** Usado para fazer a substituição em cada elemento. Os argumentos da função são:

   **elemento:** O elemento HTML que está sendo atualizado.
   **contagem:** A contagem de conteúdo para este elemento.

* **regex:** Usado para determinar qual parte do texto do elemento deve ser substituída pela contagem.

   **Exemplo**:

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >Use o substituto para personalizar ou internacionalizar a mensagem de contagem de comentários.
