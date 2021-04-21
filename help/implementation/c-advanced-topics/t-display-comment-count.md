---
description: Pegue as contagens de postagem e comentário para determinadas coleções a serem exibidas em suas páginas de índice.
title: Exibir Contagem de Comentários
exl-id: 03c911f0-1fdd-4d5c-9262-9ff7485b7b14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Exibir Contagem de Comentários{#display-comment-count}

Pegue as contagens de postagem e comentário para determinadas coleções a serem exibidas em suas páginas de índice.

O `CommentCount.js` de Livefyre permite buscar as contagens de conteúdo para as coleções no site. Embora os aplicativos mostrem a contagem de comentários para a coleção atual, ter essas contagens sindicado em seu site pode ser útil. Esse recurso é especialmente útil se você não persistir conteúdo no banco de dados (ou se o banco de dados do CMS não estiver sincronizado com o Livefyre).

1. Carregue o JavaScript.

   Para usar `CommentCount.js`, primeiro incorpore o arquivo JavaScript na seção `<head>` da página ou do modelo em que deseja usá-lo.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Vincule o elemento HTML.

   Após carregar o script, ele tentará localizar outros elementos na página com um nome de classe de `livefyre-commentcount`. Para cada um desses elementos, o script procurará `data-lf-site-id` e `data-lf-article-id` atributos HTML e os usará para buscar conteúdo do Livefyre e atualizar cada elemento com o valor mais recente.

   Por exemplo, o seguinte elemento seria atualizado:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >O código `CommentCount.js` verifica se há um valor numérico a ser atualizado com a contagem real. Certifique-se de incluir um valor numérico entre as tags .

   **Exemplo 1**  (usando o URL como a ID do artigo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Exemplo 2**  (uso de um sistema numerado como a ID do artigo):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Configurar opções.

   Para ter mais controle sobre como as contagens de conteúdo são substituídas, chame `LF.CommentCount()` e passe em um objeto que contenha as opções de configuração. Certifique-se de chamar a função depois que todos os elementos que precisam ser substituídos estiverem no DOM. O melhor lugar para chamar esse método é no rodapé, portanto, isso acontece quando o DOM é carregado, mas antes dos eventos prontos para documento e janela.

   Permitimos as seguintes opções de configuração:

* **replacer:** função ou Regex usado para substituir o texto de cada contagem de conteúdo.

* **função:** usada para fazer a substituição em cada elemento. Os argumentos da função são:

   **element:** o elemento HTML que está sendo atualizado.
   **contagem:** a contagem de conteúdo para esse elemento.

* **regex:** usado para determinar qual parte do texto do elemento deve ser substituída pela contagem.

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
