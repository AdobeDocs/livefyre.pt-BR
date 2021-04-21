---
title: Adicionar observações a uma página
description: Adicionar observações a uma página
exl-id: 3ec089d0-3d51-4918-b510-d30ef645c9c2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Adicionar observações a uma página {#adding-sidenotes-to-a-page}

Livefyre fornece várias opções de configuração para posicionar Observações na sua página:

* A opção Seletores define os elementos nos quais as Observações devem ser exibidas.
* Âncoras representam elementos que podem ser identificados.
* O contêiner de encadeamento personalizado permite definir onde o encadeamento de Observações estará localizado em relação ao conteúdo identificado.
* A opção Sidenotes count permite exibir o número de Sidenotes adicionados no local especificado.
* Use vários objetos `ConvConfig` para adicionar Observações a várias histórias em uma única página.

## Seletores {#section_wyj_4sv_sy}

A opção seletores permite que as Observações localizem conteúdo na página. O valor dessa opção permite determinar dinamicamente os elementos que serão usados. Pode ser uma sequência de seletor (como ‘#content p, #content img’), um objeto jQuery (como `$(‘#content’)`), uma matriz de elementos DOM ou um objeto com duas propriedades: incluir e excluir. O Aplicativo de observações usará os elementos especificados ou os elementos correspondentes na página. Se as propriedades incluir e excluir forem usadas, os Observações primeiro analisarão a página para localizar todos os elementos na propriedade include e, em seguida, removerão quaisquer elementos encontrados na propriedade exclude.

## Âncoras {#section_ehq_psv_sy}

As âncoras representam um elemento cujo conteúdo pode ser identificado. Um elemento de âncora pode conter texto ou uma imagem. A opção seletores transmitida durante a construção do aplicativo determinará os elementos da âncora.

## IDs de âncora {#section_rsb_rsv_sy}

As âncoras na página são identificadas usando um `data-lf-anchor-id`.

Para definir a ID de uma âncora por conta própria, adicione o atributo `data-lf-custom-anchor-id` ao elemento que você deseja mapear para uma âncora. Isso é útil nos casos em que a detecção automática de âncoras falharia.

Por exemplo, se você planeja usar um URL diferente para as versões de desktop e dispositivos móveis de uma imagem, dois URLs diferentes podem ser mapeados para âncoras diferentes. Se, em vez disso, seu HTML fornecer um `data-lf-custom-anchor-id` que seja o mesmo em dispositivos móveis e desktops, o elemento de imagem será tratado como uma única âncora.

As âncoras têm um tipo determinado dinamicamente, mas também podem ser definidas explicitamente usando o atributo `data-lf-custom-anchor-type`.

>[!NOTE]
>
>O valor do número de enumeração deve ser usado.

Os tipos disponíveis são:

* **Texto:** 1
* **Imagem:** 2
* **Mídia:** 3
* **Rico:** 4

Consulte [updateAnchors method](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) para obter mais informações sobre como usar o método `updateAnchors` para adicionar dinamicamente conteúdo Sidenote à página.

## Contêiner de encadeamento personalizado {#section_jdh_btv_sy}

Use a opção `threadContainerEl` para especificar um local para um thread de Observações, diferente da posição padrão. Por padrão, quando uma âncora é ativada, as Observações são exibidas ao lado ou abaixo do conteúdo relevante. Para alterar esse padrão, use o `threadContainerEl` para especificar o elemento no qual o thread deve aparecer.

Esse valor para essa opção funciona como a opção seletores , exceto que somente o primeiro elemento válido será usado.

## Contagem de Observações {#section_pld_ntv_sy}

Use a opção `numSidenotesEl` para incorporar um widget de contagem opcional de observações na página. Essa opção aceita a mesma entrada que a opção seletores, mas usará apenas o primeiro elemento válido na matriz de entrada.

O widget decorará o elemento fornecido ou correspondente e incluirá o ícone de entrada Observações, o número de Observações inseridas nessa posição e um ícone de ajuda.

Clicar no widget exibirá uma portfólio com uma breve explicação das observações e como usá-las.

A explicação e o texto de exemplo são configuráveis usando strings personalizadas ( `questionExplanation` e `questionMockText`, respectivamente). A aparência do widget de contagem e do portador também podem ser configuradas usando estilos personalizados ( `numSidenotes` e `numSidenotesPopover`, respectivamente).

## Adicionar várias coleções de observações a uma única página {#section_pjl_ptv_sy}

O Livefyre permite adicionar várias Coleções de observações a uma única página. Por exemplo, se a página incluir três notícias, você pode incluir três iterações separadas do aplicativo Sidenotes. Para fazer isso, você deve definir um objeto `ConvConfig` separado para cada instância dos Observações que deseja criar. Por exemplo:

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```
