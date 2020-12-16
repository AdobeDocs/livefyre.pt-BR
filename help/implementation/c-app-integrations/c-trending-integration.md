---
description: Mostre as coleções mais ativas em seu site ou rede.
seo-description: Mostre as coleções mais ativas em seu site ou rede.
seo-title: Tendência
solution: Experience Manager
title: Tendência
uuid: 3031523d-b487-4eea-bba6-5d8f9971874f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# Tendência{#trending}

Mostre as coleções mais ativas em seu site ou rede.

Use Tendências para mostrar as Coleções com a atividade mais recente em seu Site ou Rede.

## Integração {#section_wtz_whb_c1b}

A maneira mais rápida de integrar com o Trending Topics é usar a versão incorporada hospedada no CDN da Livefyre.

Primeiro, adicione [Livefyre.js](https://github.com/Livefyre/Livefyre.js) à sua página.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Em seguida, posicione o elemento no qual o aplicativo aparecerá.

```
<div id="trending"></div>
```

Finalmente, use `Livefyre.require` para construir o componente.

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

Agora você tem um aplicativo de tendência! Veja tudo isso em ação em [este exemplo](https://codepen.io/gobengo/pen/GijEy).

## Configuração {#section_k5k_qhb_c1b}

`network`

A rede da qual as coleções serão extraídas. (Obrigatório.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Forneça a ID do site para mostrar as coleções somente de um único site na sua rede. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Forneça uma única tag Coleção para mostrar somente as Coleções com essa tag. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

