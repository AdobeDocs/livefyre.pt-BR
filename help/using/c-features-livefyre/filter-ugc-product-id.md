---
description: Filtrar o UGC por ID de produto permite incorporar exatamente o mesmo aplicativo em várias páginas, além de mostrar diferentes UGC específicos do produto para cada página.
seo-description: Filtrar o UGC por ID de produto permite incorporar exatamente o mesmo aplicativo em várias páginas, além de mostrar diferentes UGC específicos do produto para cada página.
seo-title: Filtrar UGC por ID de produto
title: Filtrar UGC por ID de produto
uuid: 98108db-5710-4331-891b-7e1bb106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816

---


# Filtrar UGC por ID de produto {#filter-ugc-product-id}

Filtrar o UGC por ID de produto permite incorporar exatamente o mesmo aplicativo em várias páginas, além de mostrar diferentes UGC específicos do produto para cada página.

Para filtrar o UGC por ID de produto, siga estas etapas:

1. No Livefyre Studio, navegue até a **[!UICONTROL Apps]** guia.

1. Selecione o aplicativo que deseja modificar.

1. Selecione a guia Designer no painel esquerdo.

1. Enable **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Selecione as pastas de produtos de nível superior que contêm o produto ou produtos pelo qual deseja filtrar o UGC.
Use CTRL/Command + clique para selecionar várias pastas.

1. Disable **[!UICONTROL Show related content]**.
Quando ativado, o conteúdo filtrado usando o `data-lf-attr-product` atributo será exibido primeiro, seguido por todo o outro conteúdo no aplicativo.

1. Clique em **[!UICONTROL Publish]**.

1. Insira as IDs de produto que deseja filtrar no código resultante.

>[!NOTE]
>
>Para localizar IDs de produto, navegue até **[!UICONTROL Settings > Products]**. Localize o produto desejado e selecione-o e a ID será exibida.

Por exemplo, o código a seguir é gerado para um aplicativo Media Wall:

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

Para marcar um produto, substitua `<product 1>` `data-lf-attr-product` o atributo pela ID de produto desejada. Você pode marcar um ou mais produtos adicionando IDs de produtos separados por vírgula adicionais. Os produtos devem estar contidos na pasta ou pastas de produto de nível superior selecionadas na Etapa 5.

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