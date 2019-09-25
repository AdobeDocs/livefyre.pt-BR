---
description: Permita que os clientes avaliem e revejam suas ofertas de produtos.
seo-description: Permita que os clientes avaliem e revejam suas ofertas de produtos.
seo-title: Resenhas
solution: Experience Manager
title: Resenhas
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Resenhas {#reviews}

Permita que os clientes avaliem e revejam suas ofertas de produtos.

As revisões permitem que os membros de sua comunidade contribuam com classificações por estrelas e revisões qualitativas de qualquer produto ou serviço.

## Integração {#section_kk5_15b_c1b}

Para integrar um aplicativo de revisões, siga o procedimento de integração de um aplicativo de conversa. Consulte [Incorporar um aplicativo](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). A seguir está um exemplo de um aplicativo de revisões incorporado.

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

Conforme observado na `CollectionMeta` seção Construção, `CollectionMeta` é um objeto JSON codificado. No exemplo acima, o objeto JSON usa o seguinte formato antes de ser codificado em JWT:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## Objeto de Confusão {#section_pzv_ytb_c1b}

Se você já tiver concluído a seção Introdução, familiarize-se com o objeto de consoleConfig. Para habilitar Revisões, atualize a consoleConfig com os seguintes campos:

* **booleano alwaysShowEditor** *opcional* : Por padrão, o editor de revisões aparece somente depois que o usuário pressiona o botão "write review". Defina esse parâmetro como true para sempre exibir o editor.

* **sequência de caracteres** necessária *do aplicativo* : O nome do aplicativo a ser usado para revisões. Deve ser "resenhas".

* **string defaultSort** *opcional* : Permite selecionar a opção de classificação padrão para Revisões. Os valores possíveis são: maisÚtil, mais altoClassificado, mais baixoClassificado, mais recente e mais antigo.

* **disableTitle** booleano *opcional* : Desativa e oculta o campo de título no editor de revisões, que é obrigatório e visível por padrão. O padrão é verdadeiro.

* **enableHalfRating** booleano *opcional* : Usado para ativar meia classificação no módulo de seleção de estrela padrão. O padrão é verdadeiro.

* **hideShowReviewButton** booleano *opcional* : Controla se o [!UICONTROL Show My Review] botão será exibido. Defina como true para permitir que os usuários selecionem se devem mostrar ou exibir suas próprias revisões.

* **Número inteiro** opcional ** maxRating Usado para definir o número de estrelas que são mostradas no módulo padrão de seleção de estrelas. O padrão é 5. Isso pode ser configurado em até 100.

* **ratingSummaryEnabled** booleano *opcional* : Usado para mostrar a exibição resumida da classificação acima do aplicativo de revisões. Isso deve estar habilitado para usar a ratingSummaryDelegate. O padrão é verdadeiro.

## Analisar metadados da coleção {#section_k1s_sqb_c1b}

* **** tipo: string *necessária* : Define o tipo de Coleção. Deve ser `reviews`.

* **array** opcional ** ratingDimensions: Uma matriz de strings para cada tipo de dimensão que esta Coleção usará. Se isso não for especificado, somente uma dimensão será permitida.

   Por exemplo, para permitir que os usuários avaliem seu produto em "design", "recursos" e "desempenho", defina o storage como: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **ratingSubparts** inteiro *opcional* : Número de partições a serem exibidas na caixa de texto da revisão. Os rótulos de subparte são passados com o parâmetro, conforme ilustrado abaixo.

   >[!NOTE]
   >Você deve definir rótulos para cada subparte.

* **matriz ratingSubpartsIds** *opcional* : Permite definir uma ID para cada subparte na Coleção de classificações, que pode ser usada para direcionar esses elementos de subparte no CSS e no JavaScript. Quando os usuários postam revisões, cada um `ratingSubpart` terá o atributo " `data-lf-subpart-id`" nele, preenchido com essa ID.

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
>Se estiver usando `ratingDimensions`, VOCÊ DEVE usar o `ratingSelectionDelegate`, `ratingDisplayDelegate`e `ratingSummaryDelegate` (se quiser mostrar o resumo da classificação).

## Revisa a Personalização {#section_khz_xmb_c1b}

### Configurar imagens de estrela

Para mudar a imagem para estrelas completas, a classe é `goog-ratings-star`. Altere a imagem de plano de fundo para a imagem que desejar. Por padrão, as estrelas têm 28 por 28 pixels.

### Configurar imagens de estrelas com meia estrela

Com meia estrela, há duas classes, uma para cada lado da estrela. O lado esquerdo da meia estrela é `fyre-rating-half-odd` e o lado direito é `fyre-rating-half-even`. Por padrão, meia estrela tem 28 por 14 pixels.

### Configurar os valores da dica de ferramenta para estrelas

Para configurar os valores da dica de ferramenta para as estrelas, siga o texto personalizado descrito em Personalizações de sequência de caracteres. Depois de configurá-la, use a chave `ratingValues` e o valor de uma matriz que contenha as strings da dica de ferramenta. Se metade das estrelas estiver desativada, o número de elementos na matriz deverá ser o mesmo `maxRating` (acima). Se você tiver meia estrela ativada, o número de elementos deverá ser 2x `maxRating`. O primeiro elemento na matriz corresponde ao elemento de estrela mais à esquerda (ou meia estrela) e continua da esquerda para a direita.

### Alternar a opção "Mostrar minha revisão"

Para ativar ou desativar a [!UICONTROL Show My Review] opção, direcione o `hideShowReviewButton` parâmetro na configuração do aplicativo.

### Mostrar o Editor de texto por padrão

O editor de revisões aparece somente depois que o usuário pressiona o [!UICONTROL write review] botão. Para mostrar esse formulário por padrão, direcione o `alwaysShowEditor` parâmetro na configuração do aplicativo.
