---
description: null
seo-description: null
seo-title: Adicionar sidias a uma página
solution: Experience Manager
title: Adicionar sidias a uma página
uuid: 6499 c 45 a -3773-4 adb-a 6 c 7-22 a 628309 afd
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Adicionar sidias a uma página {#adding-sidenotes-to-a-page}

O Livefyre fornece várias opções de configuração para posicionar os Sidenotes na página:

* A opção Seletores define os elementos nos quais as sidenotes devem aparecer.
* As âncoras representam elementos que podem ser agrupados.
* O contêiner de encadeamento personalizado permite definir onde o encadeamento de sidenotes estará localizado em relação ao conteúdo sidenado.
* A opção de contagem de Sidenotes permite exibir o número de Soluções adicionadas no local determinado.
* Use vários `ConvConfig` objetos para adicionar Sidenotes a várias histórias em uma única página.

## Seletores {#section_wyj_4sv_sy}

A opção de seletores permite que os colegas localizem conteúdo na página. O valor para essa opção permite determinar dinamicamente os elementos que serão usados. Pode ser uma sequência do seletor (como «# content p, # content img»), um objeto jquery (como `$(‘#content’)`), uma matriz de elementos DOM ou um objeto com duas propriedades: incluir e excluir. O aplicativo de sidenotes usará os elementos especificados ou os elementos correspondentes na página. Se incluir e excluir propriedades são usadas, as Sidenotes analisarão primeiro a página para encontrar todos os elementos na propriedade incluir e, em seguida, removem quaisquer elementos encontrados na propriedade delete.

## Âncoras {#section_ehq_psv_sy}

As âncoras representam um elemento cujo conteúdo pode ser agrupado. Um elemento de âncora pode conter texto ou imagem. A opção de seletores transmitida durante a construção do aplicativo determinará os elementos de ancoragem.

## IDs de âncora {#section_rsb_rsv_sy}

As âncoras na página são identificadas usando `data-lf-anchor-id`a.

Para definir a ID de uma âncora própria, adicione o atributo `data-lf-custom-anchor-id` ao elemento que você deseja mapear para uma âncora. Isso é útil nos casos em que a detecção automática de âncoras falhava.

Por exemplo, se você planeja usar um URL diferente para as versões de desktop e móveis de uma imagem, dois urls diferentes podem ser mapeados para âncoras diferentes. Se, em vez disso, o HTML fornecer a `data-lf-custom-anchor-id` mesma coisa em dispositivos móveis e desktop, o elemento da imagem será tratado como uma única âncora.

As âncoras têm um tipo determinado dinamicamente, mas também podem ser explicitamente definidas usando o `data-lf-custom-anchor-type` atributo.

>[!NOTE]
>
>O valor do número de enumeração deve ser usado.

Os tipos disponíveis são:

* **Texto:** 1
* **Imagem:** 2
* **Mídia:** 3
* **Avançado:** 4

Consulte [Método updateanchors](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) para saber mais sobre como usar o `updateAnchors` método para adicionar o conteúdo de Sidenote à página dinamicamente.

## Contêiner personalizado de encadeamento {#section_jdh_btv_sy}

Use a `threadContainerEl` opção para especificar um local para uma thread de Sidenota, diferente da posição padrão. Por padrão, quando uma âncora é ativada, as Sidenotes aparecerão ao lado ou abaixo do conteúdo relevante. Para alterar esse padrão, use o `threadContainerEl` para especificar o elemento onde o encadeamento deve aparecer.

Esse valor para essa opção funciona da mesma forma que a opção de seletores, exceto que apenas o primeiro elemento válido será usado.

## Contagem de auxiliares {#section_pld_ntv_sy}

Use a `numSidenotesEl` opção para incorporar um widget de contagem opcional de Sidenotes na sua página. Essa opção aceita a mesma entrada da opção de seletores, mas usará apenas o primeiro elemento válido na matriz de entrada.

O widget irá decorar o elemento fornecido ou combinado, e incluirá o ícone de entrada de Sidenotes, o número de Sidenotes inseridos nesta posição e um ícone de ajuda.

Clicar no widget exibirá um popover com uma breve explicação de Sidenotes e como usá-los.

A explicação e o texto do exemplo são configuráveis usando strings personalizadas ( `questionExplanation` e `questionMockText`, respectivamente). A aparência do widget de contagem e do popover também pode ser configurada usando estilos personalizados ( `numSidenotes` e `numSidenotesPopover`, respectivamente).

## Adicionar várias coleções de sidecotes a uma página única {#section_pjl_ptv_sy}

O Livefyre permite que você adicione várias Coleções de sidecotes a uma única página. Por exemplo, se a página incluir três histórias de notícias, você pode incluir três iterações separadas do Aplicativo de sidenotes. Para fazer isso, você deve definir um `ConvConfig` objeto separado para cada instância de Sidenotes que deseja criar. Por exemplo:

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
