---
description: Permita que os clientes classifiquem e revejam suas ofertas de produtos.
seo-description: Permita que os clientes classifiquem e revejam suas ofertas de produtos.
seo-title: Revisões
solution: Experience Manager
title: Revisões
uuid: b 740 ee 28-f 6 f 9-4 ae 7-9 fe 7-61 a 5 cde 97 bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Revisões {#reviews}

Permita que os clientes classifiquem e revejam suas ofertas de produtos.

As revisões permitem que membros da comunidade contribuam com classificações por estrela e revisões qualitativas para qualquer produto ou serviço.

## Integração {#section_kk5_15b_c1b}

Para integrar um Aplicativo de revisão, siga o procedimento para Integrar um aplicativo de conversa. Consulte [Incorporar um aplicativo](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). A seguir está um exemplo de um Aplicativo de revisões incorporado.

### Exemplo

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

Conforme observado na `CollectionMeta` seção Construção, `CollectionMeta` é um objeto JSON codificado. No exemplo acima, o objeto JSON pega o seguinte formato antes de ser codificado em JWT:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## Objeto convconfig {#section_pzv_ytb_c1b}

Se você já tiver completado a seção Introdução, familiarize-se com o objeto convconfig. Para habilitar Revisões, atualize a convconfig com os seguintes campos:

* **Alwaysshoweditor** *booleano opcional* : Por padrão, o editor de revisões aparece somente depois que o usuário pressiona o botão «gravar revisão». Defina esse parâmetro como verdadeiro para exibir sempre o editor.

* **sequência** *necessária* : O nome do aplicativo a ser utilizado para revisões. Deve ser «revisão».

* **Sequência** *opcional* de defaultclass:: Permite selecionar a opção de classificação padrão para Revisões. Os valores possíveis são: Mosthelpous, highestrated, lowestrated, newest e mais antigas.

* **Disabletitle** *booleano opcional* : Desativa e oculta o campo de título no editor de revisões, que é obrigatório e visível por padrão. O padrão é verdadeiro.

* **Enablehalfrating** *booleano opcional* : Usado para permitir meia classificação no módulo de seleção de estrela padrão. O padrão é verdadeiro.

* **Hideshowreviewbutton** ** booleano opcional: Controla se o [!UICONTROL Show My Review] botão será exibido. Defina como verdadeiro para permitir que os usuários selecionem mostrar ou exibir suas próprias revisões.

* **Número inteiro** *opcional* Usado para definir o número de estrelas exibidas no módulo de seleção de estrela padrão. O padrão é 5. Isso pode ser configurado até 100.

* **Ratingresumir yenabled** *opoleano opcional* : Usado para mostrar a exibição de resumo da classificação acima do Aplicativo de revisão. Isso deve ser habilitado para usar o ratingsummarydelegate. O padrão é verdadeiro.

## Revisar metadados da coleção {#section_k1s_sqb_c1b}

* **type:***string necessária* : Define o tipo de Coleção. Deve ser `reviews`.

* **Matriz** *opcional* de ratingdimensões: Uma matriz de sequências de caracteres para cada tipo de dimensão que essa coleção usará. Se isso não for especificado, apenas 1 dimensão será permitida.

   Por exemplo, para permitir que os usuários classifiquem seu produto em &quot;design&quot;, &quot;recursos&quot; e &quot;desempenho&quot;, defina a matriz como: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **Número inteiro** *opcional* de ratingsubpartes: Número de partições a serem exibidas na caixa de texto da revisão. As etiquetas de subpartes são passadas com o parâmetro conforme ilustrado abaixo.

   >[!NOTE]
   >Você deve definir rótulos para cada subparte.

* **Matriz** *opcional* de ratingids: Permite definir uma ID para cada subparte na Collection Collection, que pode ser usada para direcionar esses elementos de subparte em seu CSS e javascript. Quando os usuários postam revisões, cada um `ratingSubpart` terá o atributo « `data-lf-subpart-id`» nele preenchido, preenchido com essa ID.

>[!NOTE]
>
>Para usar `ratingSubpartsIds`, o `ratingSubparts` param também deve ser definido e o comprimento das duas matrizes deve corresponder.

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>Se estiver usando `ratingDimensions`, você deverá usar o `ratingSelectionDelegate`, `ratingDisplayDelegate`e `ratingSummaryDelegate` (se desejar exibir o resumo da classificação).

## Revisa personalização {#section_khz_xmb_c1b}

### Configurar imagens em estrela

Para alterar a imagem para estrelas completas, a classe `goog-ratings-star`é. Altere a imagem de plano de fundo para qualquer imagem desejada. Por padrão, as estrelas são de 28 em 28 pixels.

### Configurar imagens em estrela com meio estrelas

Com estrelas, há duas classes, uma para cada lado da estrela. O lado esquerdo da meia-estrela é `fyre-rating-half-odd` e o lado direito é `fyre-rating-half-even`. Por padrão, as meia-estrelas têm 28 por 14 pixels.

### Configurar os valores de dica de ferramenta para estrelas

Para configurar os valores de dica de ferramenta para as estrelas, siga o texto personalizado descrito em Personalizações de cadeia de caracteres. Após essa configuração, use a chave `ratingValues` e o valor que contém as strings de dica de ferramenta. Se você tiver estrelas desativadas, o número de elementos na matriz deve ser o mesmo ( `maxRating` acima). Se tiver estrelas ativadas, o número de elementos deve ser de 2 x `maxRating`. O primeiro elemento na matriz corresponde ao elemento da estrela mais à esquerda (ou meia estrela) e continua da esquerda para a direita.

### Alternar a opção «Mostrar minha revisão»

Para ativar ou desativar [!UICONTROL Show My Review] a opção, defina o `hideShowReviewButton` parâmetro na configuração do aplicativo.

### Mostrar o Editor de texto por padrão

O editor de revisões aparece somente depois que o usuário pressiona o [!UICONTROL write review] botão. Para mostrar este formulário por padrão, defina como meta o `alwaysShowEditor` parâmetro na configuração do aplicativo.
