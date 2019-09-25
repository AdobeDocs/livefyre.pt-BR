---
description: 'null'
seo-description: 'null'
seo-title: Adicionar notas de identidade a uma página
solution: Experience Manager
title: Adicionar notas de identidade a uma página
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Adicionar notas de identidade a uma página {#adding-sidenotes-to-a-page}

O Livefyre fornece várias opções de configuração para posicionar as Sidenotes em sua página:

* A opção Seletores define os elementos nos quais as Sidenotes devem aparecer.
* Âncoras representam elementos que podem ser identificados.
* O contêiner de encadeamento personalizado permite definir onde o encadeamento de Sidenotes será localizado em relação ao conteúdo identificado.
* A opção de contagem de Sidenotes permite exibir o número de Sidenotes adicionados no local especificado.
* Use vários `ConvConfig` objetos para adicionar Sidenotes a várias histórias em uma única página.

## Seletores {#section_wyj_4sv_sy}

A opção seletores permite que o Sidenotes localize conteúdo na página. O valor dessa opção permite que você determine dinamicamente os elementos que serão usados. Pode ser uma string de seletor (como ‘#content p, #content img’), um objeto jQuery (como `$(‘#content’)`), uma matriz de elementos DOM ou um objeto com duas propriedades: incluir e excluir. O aplicativo Sidenotes usará os elementos especificados ou os elementos correspondentes na página. Se as propriedades include e exclude forem usadas, os Sidenotes primeiro analisarão a página para localizar todos os elementos na propriedade include e, em seguida, removerão quaisquer elementos encontrados na propriedade exclude.

## Âncoras {#section_ehq_psv_sy}

As âncoras representam um elemento cujo conteúdo pode ser identificado. Um elemento de âncora pode conter texto ou uma imagem. A opção de seletores transmitida durante a construção do aplicativo determinará os elementos de ancoragem.

## IDs de âncora {#section_rsb_rsv_sy}

As âncoras na página são identificadas usando um `data-lf-anchor-id`.

Para definir a ID de uma âncora, adicione o atributo `data-lf-custom-anchor-id` ao elemento que você deseja mapear para uma âncora. Isso é útil nos casos em que a detecção automática de âncoras falhasse.

Por exemplo, se você planeja usar um URL diferente para as versões para desktop e dispositivos móveis de uma imagem, dois URLs diferentes podem ser mapeados para âncoras diferentes. Se, em vez disso, seu HTML fornecer uma `data-lf-custom-anchor-id` que seja a mesma em dispositivos móveis e desktop, o elemento de imagem será tratado como uma única âncora.

Âncoras têm um tipo que é determinado dinamicamente, mas que também pode ser definido explicitamente usando o `data-lf-custom-anchor-type` atributo.

>[!NOTE]
>
>O valor do número de enumeração deve ser usado.

Os tipos disponíveis são:

* **** Texto: 1
* **** Imagem: 2
* **** Mídia: 3
* **** Rico: 4

Consulte o método [updateAnchors](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) para obter mais informações sobre como usar o `updateAnchors` método para adicionar conteúdo Sidenote à página dinamicamente.

## Contêiner de thread personalizado {#section_jdh_btv_sy}

Use a `threadContainerEl` opção para especificar um local para um thread Sidenotes, diferente da posição padrão. Por padrão, quando uma âncora é ativada, as Sidenotes serão exibidas ao lado ou abaixo do conteúdo relevante. Para alterar esse padrão, use o para especificar o elemento no qual o thread deve aparecer. `threadContainerEl`

Esse valor para essa opção funciona como a opção de seletores, exceto que apenas o primeiro elemento válido será usado.

## Contagem de votos {#section_pld_ntv_sy}

Use a `numSidenotesEl` opção para incorporar um widget de contagem de Sidenotes opcional à sua página. Essa opção aceita a mesma entrada que a opção de seletores, mas usará apenas o primeiro elemento válido na matriz de entrada.

O widget decorará o elemento fornecido ou correspondente e incluirá o ícone de entrada Sidenotes, o número de Sidenotes digitados nesta posição e um ícone de ajuda.

Clicar no widget exibirá uma publicação com uma breve explicação de Sidenotes e como usá-los.

Tanto a explicação quanto o texto de exemplo são configuráveis usando strings personalizadas ( `questionExplanation` e `questionMockText`, respectivamente). A aparência do widget de contagem e do portátil também pode ser configurada usando estilos personalizados ( `numSidenotes` e `numSidenotesPopover`, respectivamente).

## Adicionar várias coleções de notas de identidade a uma única página {#section_pjl_ptv_sy}

O Livefyre permite que você adicione várias Coleções de Sidenotes a uma única página. Por exemplo, se a página incluir três notícias, você pode desejar incluir três iterações separadas do aplicativo Sidenotes. Para fazer isso, você deve definir um `ConvConfig` objeto separado para cada instância de Sidenotes que deseja criar. Por exemplo:

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
