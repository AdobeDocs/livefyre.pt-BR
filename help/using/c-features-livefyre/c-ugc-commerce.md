---
description: Forneça UGC específico do produto em pontos específicos da jornada do cliente para aumentar a intenção de compra e a conversão usando o recurso Comércio UGC.
title: Comércio UGC
exl-id: ba95e150-ccb1-4076-b3d5-3f31dbf45761
source-git-commit: 669a0a7d61dbf0697c2f48fa7feac6eba89d2815
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 2%

---

# Comércio UGC{#ugc-commerce}

Forneça UGC específico do produto em pontos específicos da jornada do cliente para aumentar a intenção de compra e a conversão usando o recurso Comércio UGC.

Use o recurso de Comércio UGC para influenciar a intenção de compra e a conversão nas páginas de detalhes do produto e UGC. Acelere o tempo de comercialização, associando o UGC sem interrupções ao inventário de produtos. Crie fidelidade à marca criando uma comunidade usando o UGC para destacar histórias autênticas de clientes.

AEM Livefyre fornece várias maneiras de importar informações do catálogo de produtos, incluindo SKU, imagens em miniatura, preço e nome do produto. Gerencie facilmente a associação de produtos com o UGC usando AEM solicitações de direitos da Livefyre, marcação de regra de fluxo automático e fluxos de trabalho de moderação.

Além de influenciar a compra, os recursos na oferta de comércio UGC AEM Livefyre podem ser aproveitados para gerar conversões de outras maneiras, incluindo:

* Geração de leads B2B: colocar botões de chamada para ação em UGC para capturar leads
* Downloads de aplicativos B2C: solicitar que os usuários baixem um aplicativo
* Remessas para o artigo: vincular usuários a artigos relacionados a partes de UGC

Coloque chamadas para ações do produto junto ao UGC para impulsionar a conversão. É possível:

* Adicione UGC específico do produto em escala para milhares de páginas de detalhes do produto.
* Incorpore AEM aplicativos de visualização do Livefyre que oferecem suporte a recursos de comércio UGC, como o Media Wall e o Mosaic, nas páginas de detalhes do produto.
* Use códigos de rastreamento de referências configuráveis com uma solução de análise para medir as conversões dos CTAs de produtos colocados em UGC e UGC colocados nas páginas de detalhes do produto.

AEM usuários do Commerce podem integrar facilmente seu catálogo de produtos existente ao Livefyre para impulsionar a participação do usuário nos aplicativos de visualização do Livefyre. Os usuários do Livefyre que não usam AEM Commerce podem importar manualmente seus catálogos de produtos para o Livefyre. Consulte [Faça upload de produtos para o Livefyre usando o upload de arquivo](/help/using/c-features-livefyre/c-ugc-commerce.md), para obter mais informações.

Aplicativos que usam este recurso:

* [Placa de recurso](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app). Para obter informações sobre como usar o Comércio UGC em um Cartão de Recurso, consulte [Personalizações da placa de recurso](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y).

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Para obter informações sobre como usar o Comércio UGC em uma Tira de Arquivo, consulte [Personalizações da faixa de filtros](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Mural de mídia](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app). Para obter informações sobre como usar o Comércio UGC em um Mural de mídia, consulte [Personalizações do mural de mídia](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations).

* [Mosaico](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Para obter informações sobre como usar o Comércio UGC em um Mosaic, consulte [Personalizações do Mosaic](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Visão geral: Como usar o botão de ação Chamar para comércio UGC {#section_s2d_tln_n1b}

1. Crie um aplicativo com um botão de ação. Consulte [Adicionar um botão de ação de chamada a um aplicativo](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Adicione o catálogo de produtos ao Livefyre. É possível importar conteúdo de uma das duas formas a seguir:

   * [Importação de produtos para o Livefyre usando AEM Commerce](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) se você usar AEM Commerce.
   * [Faça upload de produtos para o Livefyre](/help/using/c-features-livefyre/c-ugc-commerce.md) se você não usar AEM Commerce.

1. Associe produtos ao conteúdo. Você pode fazer isso de uma das quatro maneiras:

   * Da Biblioteca. Consulte [Associar produtos ao conteúdo usando a biblioteca](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * Do ModQ. Consulte [Moderar conteúdo usando ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * Do Conteúdo Do Aplicativo. Consulte [Adicionar um botão de ação de chamada a um aplicativo](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * De um fluxo. Consulte [Opções de regra de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

## Faça upload de produtos para o Livefyre usando o upload de arquivo {#section_n1s_4hz_m1b}

Faça upload dos produtos a serem usados com o botão de ação Chamada para adicionar produtos para associar ao conteúdo ou editar e excluir arquivos existentes.

>[!NOTE]
>
>Fazer upload de um arquivo para uma pasta com arquivos existentes excluirá todos os arquivos dessa pasta e os substituirá pelo novo arquivo.

1. Navegar para **[!UICONTROL Network Settings > Products.]**
1. Crie um **[!UICONTROL Product Folder]** ou usar um **[!UICONTROL Product Folder]**.

1. Clique no botão **[!UICONTROL Product Folder]** para selecioná-lo.
1. Clique no botão **[!UICONTROL Upload Products]** botão.
1. Faça upload de um arquivo de produto em um dos seguintes formatos:

   * Formato de arquivo de produtos Google
   * Formato Livefyre (ver abaixo)

   Faça upload de um arquivo JSON no formato padrão. Você pode baixar um modelo para ver um exemplo do formato padrão. Veja a seguir um exemplo de uma linha de produto em um modelo. Ele segue a sequência `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   A tabela explica os pares de chave e valor necessários para fazer upload de produtos:

## Pares de valor/chave para o formato padrão de upload do catálogo de produtos

| Chave | Tipo | Descrição |
|--- |--- |--- |
| id | String   | ID exclusiva do produto. |
| oembed | Objeto | Anexo de imagem `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | String   | Título do produto. |
| isFolder | Booleano | Se verdadeiro, o produto é tratado como uma pasta (por exemplo, homens, mulheres etc.). |
| parentId | String   | Define em qual pasta o produto está. |
| descrição | String   | Descrição do produto. |
| preço | String   | Valor do produto em dólares. Por exemplo, &#39;23.36.&#39; |
| sku | String   | Unidade de manutenção de estoque (SKU) do produto. |
| url | String | Link para a página do produto. |
| ativado | Booleano | Um valor True significa que o produto está ativo. |
| atributos | Matriz | Tipos e valores que definem o produto (por exemplo, cor, tamanho, etc.). Esta é uma matriz de objetos.</br>**Propriedades:** </br>type </br>Tipo: String</br>Descrição: Cor, tamanho </br>value </br>Tipo: String </br>Descrição: Verde, XS |
| específicos | Matriz | Tags que definem categorias de conteúdo (por exemplo, carros, sapatos, etc.). Esta é uma matriz de sequências de caracteres. |

## ModQ {#section_os1_v4t_n1b}

Você pode associar conteúdo a produtos do seu catálogo de produtos no ModQ, de acordo com seus fluxos de trabalho de moderação existentes. Para obter informações sobre como usar o UGC Commerce com o ModQ, consulte [Moderar conteúdo usando ModQ](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Fluxos {#section_qtj_v4t_n1b}

Você pode associar produtos automaticamente ao conteúdo usando regras de fluxo, publicar o conteúdo automaticamente em um aplicativo, salvá-lo na Biblioteca ou Moderá-lo usando o ModQ. Para obter mais informações sobre como usar o Comércio UGC com regras de fluxo, consulte [Opções de regra de fluxo para todas as regras de fluxo](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
