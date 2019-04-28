---
description: Forneça UGC específico do produto em pontos específicos da jornada do cliente para aumentar o propósito de compra e a conversão com o recurso de Comércio UGC.
seo-description: Forneça UGC específico do produto em pontos específicos da jornada do cliente para aumentar o propósito de compra e a conversão com o recurso de Comércio UGC.
seo-title: Comércio UGC
solution: Experience Manager
title: Comércio UGC
uuid: 71 e 64901-a 2 b 6-4957-ba 88-058 e 4 eaca 537
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Comércio UGC{#ugc-commerce}

Forneça UGC específico do produto em pontos específicos da jornada do cliente para aumentar o propósito de compra e a conversão com o recurso de Comércio UGC.

Use o recurso Comércio UGC para influenciar o propósito de compra e conversão em páginas de detalhes de UGC e produtos. Acelere o tempo de comercialização associando perfeitamente UGC ao inventário de produtos. Crie fidelidade de marca ao criar a comunidade usando o UGC para destacar as histórias autênticas do cliente.

O AEM Livefyre fornece várias maneiras de importar informações de catálogo de produtos, incluindo SKU, imagens em miniatura, preço e nome do produto. Gerencie facilmente a associação de produtos com UGC usando solicitações de direitos do AEM Livefyre, marcação de regras de fluxo automático e fluxos de trabalho de moderação.

Além de influenciar a compra, os recursos na oferta de comércio UGC do AEM Livefyre podem ser aproveitados para impulsionar conversões de outras formas, incluindo:

* Geração de lead B 2 B: colocar botões de chamada de chamada sob UGC para capturar clientes potenciais
* Downloads do aplicativo B 2 C: solicitar que os usuários baixem um aplicativo
* Referências de artigo: vincular usuários a artigos relacionados a partes de UGC

Insira chamadas de produto a partir de UGC para impulsionar a conversão. Você pode:

* Adicione UGC específico do produto em escala a milhares de páginas de detalhes do produto.
* Incorpore os aplicativos de visualização do AEM Livefyre que oferecem suporte para recursos de comércio do UGC, como Media Wall e Mosaic, em páginas de detalhes do produto.
* Use códigos de rastreamento de referências configuráveis com uma solução de análise para medir as conversões de ctas do produto colocados em UGC e UGC colocados em páginas de detalhes do produto.

Os usuários do AEM Commerce podem integrar perfeitamente seu catálogo de produtos existente no Livefyre para impulsionar o envolvimento do usuário nos aplicativos de visualização do Livefyre. Os usuários do Livefyre que não usam o AEM Commerce podem importar manualmente seus catálogos de produtos para o Livefyre. Consulte [Carregar produtos para o Livefyre usando o carregamento de arquivo](/help/using/c-features-livefyre/c-ugc-commerce.md), para mais.

Aplicativos que usam este recurso:

* [Cartão de recursos](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app). Para obter informações sobre como usar o Comércio UGC em um Cartão de recursos, consulte [Personalizações do cartão de recursos](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y).

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Para obter informações sobre como usar o Comércio UGC em uma Película fotográfica, consulte [Personalizações de película fotográfica](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Media Wall](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app). Para obter informações sobre como usar o Comércio UGC em um mural de mídia, consulte [Personalizações do Media Wall](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations).

* [Mosaico](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Para obter informações sobre como usar o Comércio UGC em um Mosaico, consulte [Personalizações em mosaico](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Visão geral: Como usar o botão de chamada de chamada de comércio UGC {#section_s2d_tln_n1b}

1. Criar um aplicativo com um botão de ação de chamada. Consulte [Adicionar um botão de chamada a um aplicativo](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Adicione o catálogo de produtos ao Livefyre. É possível importar conteúdo de uma das duas maneiras:

   * [Importe produtos para o Livefyre usando o AEM Commerce](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) se você usar o AEM Commerce.
   * [Faça upload de produtos para o Livefyre](/help/using/c-features-livefyre/c-ugc-commerce.md) se você não usar o AEM Commerce.

1. Associar produtos com conteúdo. Você pode fazer isso de uma das quatro maneiras:

   * Da Biblioteca. Consulte [Associar produtos com conteúdo usando a biblioteca](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * De modq. Consulte [Moderar conteúdo usando modq](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * Do conteúdo do aplicativo. Consulte [Adicionar um botão de chamada a um aplicativo](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * De um Fluxo. Consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

## Carregar produtos para o Livefyre usando o carregamento de arquivo {#section_n1s_4hz_m1b}

Carregue produtos para usar com seu botão de chamada de ação para adicionar produtos a serem associados com conteúdo ou para editar e excluir arquivos existentes.

>[!NOTE]
>
>Carregar um arquivo em uma pasta com arquivos existentes excluirá todos os arquivos dessa pasta e substituirá-os pelo novo arquivo.

1. Navegue até **[!UICONTROL Network Settings > Products.]**
1. Crie **[!UICONTROL Product Folder]** um ou use um **[!UICONTROL Product Folder]** existente.

1. Clique em para **[!UICONTROL Product Folder]** selecioná-lo.
1. Clique no **[!UICONTROL Upload Products]** botão.
1. Carregue um arquivo de produto em um dos seguintes formatos:

   * Formato de arquivo de Produtos do Google
   * Formato Livefyre (veja abaixo)
   Carregue um arquivo JSON no formato padrão. É possível baixar um modelo para ver um exemplo do formato padrão. A seguir está um exemplo de uma linha de produto em um modelo. Ele segue a sequência `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   A tabela explica os pares de chaves e valores necessários para carregar produtos:

## Pares de chave/valor para o formato padrão de upload do catálogo de produtos

| Chave | Tipo | Descrição |
|--- |--- |--- |
| id | String | ID exclusiva do produto. |
| oembed | Objeto | Anexo de imagem `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | String | Título do produto. |
| Isfolder | Booliano | Se verdadeiro, o produto é tratado como uma pasta (por exemplo, masculino, mulheres, etc.). |
| Parentid | String | Define a pasta em que o produto está. |
| descrição | String | Descrição do produto. |
| price | String | Valor do produto em dólar. Por exemplo, «23.36». |
| sku | String | Unidade de manutenção do Stock (SKU) do produto. |
| url | String | Link para a página do produto. |
| enabled | Booliano | Um valor Verdadeiro significa que o produto está ativo. |
| atributos | Matriz | Tipos e valores que definem o produto (por exemplo, cor, tamanho etc.). Essa é uma matriz de objetos.</br>**Propriedades:**</br>type </br>Type: Stringdescription</br>: Tipo de cor, </br></br>Tipo de tamanho: </br>Descrição da string: Verde, XS |
| tags | Matriz | Tags que definem categorias de conteúdo (por exemplo, carros, sapatos etc.). Essa é uma matriz de strings. |

## Modq {#section_os1_v4t_n1b}

É possível associar conteúdo a produtos do catálogo de produtos em modq em consonância com os fluxos de trabalho de moderação existentes. Para obter informações sobre como usar o Comércio UGC com modq, consulte [Moderar conteúdo usando modq](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Fluxos {#section_qtj_v4t_n1b}

Você pode associar automaticamente os produtos ao conteúdo usando regras de fluxo, em seguida, publicar o conteúdo automaticamente em um aplicativo, salvá-lo na biblioteca ou moderá-lo usando modq. Para obter mais informações sobre como usar o Comércio UGC com Regras de fluxo, consulte [Opções de regras de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
