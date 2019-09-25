---
description: Entregue UGC específico do produto em pontos específicos da jornada do cliente para aumentar o propósito de compra e a conversão usando o recurso Comércio UGC.
seo-description: Entregue UGC específico do produto em pontos específicos da jornada do cliente para aumentar o propósito de compra e a conversão usando o recurso Comércio UGC.
seo-title: Comércio UGC
solution: Experience Manager
title: Comércio UGC
uuid: 71e64901-a2b6-4957-ba88-058e4eaca537
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Comércio UGC{#ugc-commerce}

Entregue UGC específico do produto em pontos específicos da jornada do cliente para aumentar o propósito de compra e a conversão usando o recurso Comércio UGC.

Use o recurso Comércio UGC para influenciar o propósito de compra e a conversão em páginas UGC e detalhes do produto. Acelere o tempo de comercialização associando perfeitamente o UGC ao inventário de produtos. Crie fidelidade à marca ao criar comunidade usando o UGC para destacar histórias autênticas de clientes.

O AEM Livefyre fornece várias maneiras de importar informações do catálogo de produtos, incluindo SKU, imagens em miniatura, preço e nome do produto. Gerencie facilmente a associação de produtos ao UGC usando solicitações de direitos do AEM Livefyre, marcação automática de regras de fluxo e fluxos de trabalho de moderação.

Além de influenciar a compra, os recursos na oferta de comércio UGC do AEM Livefyre podem ser aproveitados para gerar conversões de outras formas, incluindo:

* Geração de lead B2B: coloque os botões de chamada para ação em UGC para capturar clientes potenciais
* Downloads de aplicativos B2C: solicitar que os usuários baixem um aplicativo
* Remessas nos termos do artigo: vincular usuários a artigos relacionados a peças de UGC

Coloque as chamadas de produto para ações ao lado do UGC para direcionar a conversão. É possível:

* Adicione o UGC específico do produto em escala a milhares de páginas de detalhes do produto.
* Incorpore os aplicativos de visualização do AEM Livefyre que oferecem suporte aos recursos de comércio UGC, como Media Wall e Mosaic, nas páginas de detalhes do produto.
* Use códigos de rastreamento de referências configuráveis com uma solução de análise para medir as conversões dos CTAs do produto colocados no UGC e no UGC colocados nas páginas de detalhes do produto.

Os usuários do AEM Commerce podem integrar perfeitamente seu catálogo de produtos existente ao Livefyre para incentivar a participação dos usuários nos aplicativos de visualização do Livefyre. Os usuários do Livefyre que não usam o AEM Commerce podem importar manualmente seus catálogos de produtos para o Livefyre. Consulte [Fazer upload de produtos para o Livefyre usando o upload](/help/using/c-features-livefyre/c-ugc-commerce.md)de arquivos, para obter mais informações.

Aplicativos que usam este recurso:

* [Cartão](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)de recurso. Para obter informações sobre como usar o Comércio UGC em um Cartão de Recurso, consulte Personalizações [de Cartão de](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y)Recurso.

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Para obter informações sobre como usar o Comércio UGC em uma Película fotográfica, consulte Personalizações da [película fotográfica](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Mídia](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app). Para obter informações sobre como usar o comércio UGC em um mural de mídia, consulte Personalizações [do mural de](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations)mídia.

* [Mosaico](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Para obter informações sobre como usar o Comércio UGC em um mosaico, consulte Personalizações [mosaicas](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Visão geral: Como usar o botão de ação Chamada para Comércio UGC {#section_s2d_tln_n1b}

1. Crie um aplicativo com um botão de chamada para ação. Consulte [Adicionar um botão de ação de chamada a um aplicativo](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Adicione seu catálogo de produtos ao Livefyre. É possível importar conteúdo de uma das duas maneiras:

   * [Importe produtos para o Livefyre usando o AEM Commerce](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) se você usar o AEM Commerce.
   * [Carregue produtos no Livefyre](/help/using/c-features-livefyre/c-ugc-commerce.md) se você não usar o AEM Commerce.

1. Associe produtos ao conteúdo. Você pode fazer isso de uma das quatro maneiras:

   * Da Biblioteca. Consulte [Associar produtos ao conteúdo usando a biblioteca](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * Do ModQ. Consulte [Moderar conteúdo usando o ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * Do conteúdo do aplicativo. Consulte [Adicionar um botão de chamada para ação a um aplicativo](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * De um Fluxo. Consulte Opções de regra de [fluxo para todas as regras](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de fluxo.

## Carregue produtos no Livefyre usando o upload de arquivo {#section_n1s_4hz_m1b}

Faça upload de produtos para usar com seu botão de ação para adicionar produtos para associar ao conteúdo ou para editar e excluir arquivos existentes.

>[!NOTE]
>
>Carregar um arquivo em uma pasta com arquivos existentes excluirá todos os arquivos dessa pasta e os substituirá pelo novo arquivo.

1. Navegue até **[!UICONTROL Network Settings > Products.]**
1. Crie um **[!UICONTROL Product Folder]** ou use um existente **[!UICONTROL Product Folder]**.

1. Clique no botão **[!UICONTROL Product Folder]** para selecioná-lo.
1. Click the **[!UICONTROL Upload Products]** button.
1. Carregue um arquivo de produto em um dos seguintes formatos:

   * Formato de arquivo de produtos Google
   * Formato Livefyre (ver abaixo)
   Carregue um arquivo JSON no formato padrão. Você pode baixar um modelo para ver um exemplo do formato padrão. A seguir está um exemplo de uma linha de produto em um modelo. Segue a sequência `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   A tabela explica os pares de chave e valor necessários para carregar os produtos:

## Pares de chave/valor para o formato padrão de upload de catálogo de produtos

| Chave | Tipo | Descrição |
|--- |--- |--- |
| id | String   | ID exclusiva do produto. |
| oembed | Objeto | Image attachment `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | String   | Título do produto. |
| isFolder | Booleano | Se verdadeiro, o produto é tratado como uma pasta (por exemplo, homens, mulheres etc.). |
| parentId | String   | Define em qual pasta o produto está. |
| descrição | String   | Descrição do produto. |
| preço | String   | Valor do produto em dólares. Por exemplo, '23.36.' |
| sku | String   | Unidade de manutenção de existências (SKU) do produto. |
| url | String | Link para a página do produto. |
| ativado | Booleano | Um valor Verdadeiro significa que o produto está ativo. |
| atributos | Matriz | Tipos e valores que definem o produto (por exemplo, cor, tamanho etc.). Isto é uma matriz de objetos.</br>**** Propriedades: </br>tipo </br>Tipo: Descrição</br>da string: Cor, </br>valor do tamanho </br>Tipo: Descrição </br>da string: Verde, XS |
| específicos | Matriz | Tags que definem categorias de conteúdo (por exemplo, carros, sapatos, etc.). Isto é uma série de cordas. |

## ModQ {#section_os1_v4t_n1b}

Você pode associar conteúdo a produtos do catálogo de produtos no ModQ, de acordo com os fluxos de trabalho de moderação existentes. Para obter informações sobre como usar o Comércio UGC com o ModQ, consulte [Moderar conteúdo usando o ModQ](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Fluxos {#section_qtj_v4t_n1b}

Você pode associar produtos automaticamente ao conteúdo usando regras de fluxo, publicar o conteúdo automaticamente em um aplicativo, salvá-lo na biblioteca ou Moderá-lo usando o ModQ. Para obter mais informações sobre como usar o Comércio UGC com regras de fluxo, consulte Opções de regra de [fluxo para todas as regras](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)de fluxo.
