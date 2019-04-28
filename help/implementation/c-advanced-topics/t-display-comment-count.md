---
description: Pegue as postagens de postagem e comentário para que determinadas coleções sejam exibidas em suas páginas de índice.
seo-description: Pegue as postagens de postagem e comentário para que determinadas coleções sejam exibidas em suas páginas de índice.
seo-title: Exibir contagem de comentário
solution: Experience Manager
title: Exibir contagem de comentário
uuid: 0 f 39 b 25 e -11 e 0-4945-be 71-55 fb 4798 b 6 c 7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# Exibir contagem de comentário{#display-comment-count}

Pegue as postagens de postagem e comentário para que determinadas coleções sejam exibidas em suas páginas de índice.

O Livefyre `CommentCount.js` permite que você busque as contagens de conteúdo para coleções no site. Embora os aplicativos mostrem a contagem de comentário para a coleção atual, ter essas contagens sincronizadas em seu site pode ser útil. Esse recurso é especialmente útil se você não persistir conteúdo no banco de dados (ou se o banco de dados CMS não estiver sincronizado com o Livefyre).

1. Carregue o javascript.

   Para usar `CommentCount.js`, primeiro integre o arquivo javascript na `<head>` seção da página ou modelo onde você gostaria de usá-lo.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Vincular o elemento HTML.

   Once the script is loaded, it will attempt to find other elements on the page with a class name of `livefyre-commentcount`. Para cada um desses elementos, o script procura `data-lf-site-id` os atributos `data-lf-article-id` HTML e os usará para buscar conteúdo do Livefyre e atualizar cada elemento com o valor mais recente.

   Por exemplo, o elemento a seguir seria atualizado:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {importance = &quot;high&quot;}
   >
   >`CommentCount.js` O código verifica se um valor numérico foi atualizado com a contagem real. Assegure-se de incluir um valor numérico entre as tags.

   **Exemplo 1** (usando o URL como a ID do artigo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Exemplo 2** (usando um sistema numerado como ID do artigo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configurar opções.

   Para obter mais controle sobre como as contagens de conteúdo são substituídas, chame `LF.CommentCount()` e passe um objeto que contém as opções de configuração. Verifique se a função depois de todos os elementos que precisam ser substituídos estão no DOM. O melhor local para chamar este método está no rodapé; portanto, ocorre quando o DOM é carregado, mas antes dos eventos de documento e janela prontos.

   Permitimos as seguintes opções de configuração:

* **replacer:** Função ou Regex usada para substituir o texto de cada contagem de conteúdo.

* **:** Usado para fazer a substituição em cada elemento. Os argumentos da função são:

   **elemento:** O elemento HTML que está sendo atualizado.
   **count:** A contagem de conteúdo para este elemento.

* **regex:** Usada para determinar qual parte do texto do elemento deve ser substituída pela contagem.

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
   >Use o replacer para personalizar ou internacionalizar a mensagem de contagem de comentário.
