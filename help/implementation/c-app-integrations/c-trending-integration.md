---
description: Mostre as Coleções mais ativas em seu site ou rede.
seo-description: Mostre as Coleções mais ativas em seu site ou rede.
seo-title: Tendência
solution: Experience Manager
title: Tendência
uuid: 3031523 d-b 487-4 eea-bba 6-5 d 8 f 9971874 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Tendência{#trending}

Mostre as Coleções mais ativas em seu site ou rede.

Use Tendência para mostrar as Coleções com a atividade mais recente em seu site ou rede.

## Integração {#section_wtz_whb_c1b}

A maneira mais rápida de integrar com a Tendência é usar a versão incorporada hospedada no CDN do Livefyre.

Primeiro, adicione [Livefyre. js](https://github.com/Livefyre/Livefyre.js) à sua página.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Em seguida, posicione o elemento no qual o aplicativo será exibido.

```
<div id="trending"></div>
```

Por fim, use `Livefyre.require` para criar o componente.

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

Agora você tem um Aplicativo de tendência! Veja isso tudo em ação [neste exemplo](https://codepen.io/gobengo/pen/GijEy).

## Configuração {#section_k5k_qhb_c1b}

`network`

A rede a partir da qual coleções serão obtidas. (Obrigatório.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Forneça a ID do site para mostrar coleções somente de um único site dentro da rede. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Forneça uma tag de coleção única para mostrar apenas coleções com essa tag. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

