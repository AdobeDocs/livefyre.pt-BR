---
description: Mostre as Coleções mais ativas em seu Site ou Rede.
title: Tendência
exl-id: a3129e95-90e7-4107-bfd9-ed3b0dce20aa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---

# Tendência{#trending}

Mostre as Coleções mais ativas em seu Site ou Rede.

Use as Tendências para mostrar as Coleções com a atividade mais recente em seu Site ou Rede.

## Integração {#section_wtz_whb_c1b}

A maneira mais rápida de integrar com as Tendências é usar a versão criada hospedada no CDN da Livefyre.

Primeiro, adicione [Livefyre.js](https://github.com/Livefyre/Livefyre.js) à sua página.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Em seguida, posicione o elemento no qual o aplicativo será exibido.

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

A Rede da qual as Coleções serão extraídas. (Obrigatório.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Forneça a ID do site para mostrar as Coleções somente de um único site em sua Rede. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Forneça uma única tag Collection para mostrar apenas Coleções com essa tag. (Opcional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```
