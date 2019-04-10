---
description: A filtragem de UGC por ID de produto permite que você incorpore exatamente
  o mesmo aplicativo em várias páginas ao mostrar um UGC específico do produto para
  cada página.
seo-description: A filtragem de UGC por ID de produto permite que você incorpore exatamente
  o mesmo aplicativo em várias páginas ao mostrar um UGC específico do produto para
  cada página.
seo-title: Filtrar UGC por ID de produto
title: Filtrar UGC por ID de produto
uuid: 98108 ddb -5710-4331-891 b -7 e 1 bbb 106059
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Filtrar UGC por ID de produto {#filter-ugc-product-id}

A filtragem de UGC por ID de produto permite que você incorpore exatamente o mesmo aplicativo em várias páginas ao mostrar um UGC específico do produto para cada página.

Para filtrar o UGC por ID de produto, siga estas etapas:

1. No Livefyre Studio, navegue até **[!UICONTROL Apps]** a guia.

1. Selecione o aplicativo que deseja modificar.

1. Selecione a guia Designer no painel esquerdo.

1. Ativar **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Selecione as pastas de produto de nível superior que contêm o produto ou produtos que você deseja filtrar para UGC.
Use CTRL/Command + clique para selecionar várias pastas.

1. Disable **[!UICONTROL Show related content]**.
Quando ativado, o conteúdo filtrado usando o `data-lf-attr-product` atributo será exibido primeiro, seguido por todos os outros conteúdos no aplicativo.

1. Clique **[!UICONTROL Publish]**em.

1. Insira as IDs de produto que deseja filtrar no código resultante.

>[!NOTE]
>
>Para localizar IDs de produtos, navegue **[!UICONTROL Settings > Products]**até. Localize o produto desejado e selecione-o e a ID será exibida.

Por exemplo, o código a seguir é gerado para um Aplicativo de firewall:

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

Para marcar um produto, substitua `<product 1>` no `data-lf-attr-product` atributo pela ID de produto desejada. Você pode marcar um produto ou mais por meio da adição de IDs de produto separadas por vírgulas. Os produtos devem estar contidos na pasta de produto ou pastas de nível superior selecionados na Etapa 5.

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

O aplicativo agora só exibirá as IDs de produto marcadas.