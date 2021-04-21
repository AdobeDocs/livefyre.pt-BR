---
description: Permita que os clientes avaliem e revisem suas ofertas de produtos.
title: Resenhas
exl-id: 2f10646e-59c4-459c-ae1b-749f951a06d2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Revisões {#reviews}

Permita que os clientes avaliem e revisem suas ofertas de produtos.

As revisões permitem que os membros de sua comunidade contribuam com classificações de estrelas e revisões qualitativas de qualquer produto ou serviço.

## Integração {#section_kk5_15b_c1b}

Para integrar um aplicativo de Revisões, siga o procedimento para Integração de um aplicativo de Conversa. Consulte [Incorporar um aplicativo](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Veja a seguir um exemplo de um aplicativo de Revisões incorporado.

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

Conforme observado na seção Criação `CollectionMeta` , `CollectionMeta` é um objeto JSON codificado. No exemplo acima, o objeto JSON usa o seguinte formato antes de ser codificado em JWT:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## Objeto do ConsoleConfig {#section_pzv_ytb_c1b}

Se você já concluiu a seção Introdução , familiarize-se com o objeto de conversãoConfig . Para ativar o Reviews, atualize a conversãoConfig com os seguintes campos:

* **** ** alwaysShowEditoroptionalboolean: Por padrão, o editor de revisões aparece somente depois que o usuário pressiona o botão &quot;write review&quot;. Defina esse parâmetro como true para sempre exibir o editor.

* **** ** apprequiredstring: O nome do aplicativo a ser usado para revisões. Deve ser &quot;resenhas&quot;.

* **** ** defaultSortoptionalstring: Permite selecionar a opção de classificação padrão para Revisões. Os valores possíveis são: maisÚtil, de maior classificação, de menor classificação, mais recente e mais antigo.

* **** ** disableTitleoptionalboolean: Desativa e oculta o campo de título no editor de revisões, que é obrigatório e visível por padrão. O padrão é verdadeiro.

* **** ** enableHalfRatingoptionalboolean: Usado para ativar meia classificação no módulo padrão de seleção de estrela. O padrão é verdadeiro.

* **** ** hideShowReviewButtonoptionalbooleano: Controla se o  [!UICONTROL Show My Review] botão será exibido. Defina como verdadeiro para permitir que seus usuários selecionem se exibem ou exibam suas próprias revisões.

* **** ** maxRatingoptionalinteger Usado para definir o número de estrelas exibidas no módulo padrão de seleção de estrelas. O padrão é 5. Isso pode ser configurado até 100.

* **** ** ratingSummaryEnabledoptionalboolean: Usado para mostrar a exibição resumida da classificação acima do Aplicativo de revisões. Isso deve ser ativado para usar o ratingSummaryDelegate. O padrão é verdadeiro.

## Revisar metadados da coleção {#section_k1s_sqb_c1b}

* **type:** ** requiredstring: Define o tipo Collection . Deve ser `reviews`.

* **** ** ratingDimensionsoptionalarray: Uma matriz de sequências de caracteres para cada tipo de dimensão que essa coleção usará. Se isso não for especificado, somente uma dimensão será permitida.

   Por exemplo, para permitir que os usuários classifiquem o produto em &quot;design&quot;, &quot;recursos&quot; e &quot;desempenho&quot;, defina o storage como: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** ratingSubpartsoptionalinteger: Número de partições a serem exibidas na caixa de texto da revisão. Os rótulos de subparte são passados com o parâmetro , como ilustrado abaixo.

   >[!NOTE]
   >Você deve definir rótulos para cada subparte.

* **** ** ratingSubPartsIdsoptionalarray: Permite definir uma ID para cada subparte na Coleção de classificações, que pode ser usada para direcionar esses elementos de subparte no CSS e no JavaScript. Quando os usuários postam revisões, cada `ratingSubpart` terá o atributo &quot;`data-lf-subpart-id`&quot;, preenchido com essa ID.

>[!NOTE]
>
>Para usar `ratingSubpartsIds`, o parâmetro `ratingSubparts` também deve ser definido e o comprimento das duas matrizes deve corresponder.

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
>Se estiver usando `ratingDimensions`, DEVE usar `ratingSelectionDelegate`, `ratingDisplayDelegate` e `ratingSummaryDelegate` (se desejar mostrar o resumo da classificação).

## Revisa a Personalização {#section_khz_xmb_c1b}

### Configurar imagens de estrelas

Para alterar a imagem para estrelas completas, a classe é `goog-ratings-star`. Altere a imagem de plano de fundo para a imagem que desejar. Por padrão, as estrelas têm 28 por 28 pixels.

### Configurar imagens estreladas com meias estrelas

Com meia estrela, há duas classes, uma para cada lado da estrela. O lado esquerdo da meia estrela é `fyre-rating-half-odd` e o lado direito é `fyre-rating-half-even`. Por padrão, meia estrela é de 28 por 14 pixels.

### Configurar os valores da dica de ferramenta para estrelas

Para configurar os valores da dica de ferramenta para as estrelas, siga o texto personalizado descrito em Personalizações de sequência de caracteres. Depois de configurar, use a chave `ratingValues` e o valor de uma matriz que contém as cadeias de caracteres da dica de ferramenta. Se você tiver meia estrela desativada, o número de elementos na matriz deverá ser o mesmo que `maxRating` (acima). Se você tiver meia estrela ativada, o número de elementos deve ser 2x `maxRating`. O primeiro elemento na matriz corresponde ao elemento de estrela mais à esquerda (ou meia estrela) e continua da esquerda para a direita.

### Ative a opção &quot;Mostrar minha revisão&quot;

Para ativar ou desativar a opção [!UICONTROL Show My Review], direcione o parâmetro `hideShowReviewButton` na configuração do aplicativo.

### Mostrar o editor de texto por padrão

O editor de revisões aparece somente depois que o usuário pressiona o botão [!UICONTROL write review]. Para mostrar este formulário por padrão, direcione o parâmetro `alwaysShowEditor` na configuração do aplicativo.
