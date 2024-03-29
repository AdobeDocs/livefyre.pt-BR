---
description: Filtrar o UGC por ID de produto permite incorporar exatamente o mesmo aplicativo em várias páginas, ao mostrar diferentes UGC específicos do produto para cada página.
title: Filtrar UGC por ID de produto
exl-id: c98ee899-fcac-45dd-a26a-f678814776fd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Filtrar UGC por ID de produto {#filter-ugc-product-id}

Filtrar o UGC por ID de produto permite incorporar exatamente o mesmo aplicativo em várias páginas, ao mostrar diferentes UGC específicos do produto para cada página.

Para filtrar o UGC por ID de produto, siga estas etapas:

1. No Livefyre Studio, navegue até a guia **[!UICONTROL Apps]** .

1. Selecione o aplicativo que deseja modificar.

1. Selecione a guia Designer no painel esquerdo.

1. Ativar **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Selecione as pastas de produto de nível superior que contêm o produto ou produtos para os quais deseja filtrar o UGC.
Use CTRL/Command + clique para selecionar várias pastas.

1. Desative **[!UICONTROL Show related content]**.
Quando ativado, o conteúdo filtrado usando o atributo `data-lf-attr-product` será exibido primeiro, seguido por todos os outros conteúdos no aplicativo.

1. Clique em **[!UICONTROL Publish]**.

1. Insira as IDs de produto que você deseja filtrar no código resultante.

>[!NOTE]
>
>Para localizar IDs de produto, navegue até **[!UICONTROL Settings > Products]**. Localize o produto desejado, selecione-o e a ID será exibida.

Por exemplo, o código a seguir é gerado para um Aplicativo de mural de mídia:

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published" datalf-
env="prod" data-lf-read-only="" data-lf-attr-product="<product
 1>,<product 2>"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

Para marcar um produto, substitua `<product 1>` no atributo `data-lf-attr-product` pela ID de produto desejada. É possível marcar um ou mais produtos ao adicionar outras IDs de produtos separadas por vírgulas. Os produtos devem estar contidos na pasta ou pastas de produto de nível superior selecionadas na Etapa 5.

O segmento de código modificado apareceria como:

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published"
 data-lf-env="prod" data-lf-read-only="" data-lf-attrproduct="
109,47"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

O aplicativo agora exibirá somente as IDs de produto marcadas.
