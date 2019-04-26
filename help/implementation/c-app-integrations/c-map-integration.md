---
description: Digite o conteúdo do usuário para um mapa interativo.
seo-description: Digite o conteúdo do usuário para um mapa interativo.
seo-title: Mapa
solution: Experience Manager
title: Mapa
uuid: 1 c 3 e 399 d-a 610-4 b 80-a 3 b 2-a 5502 b 31480 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mapa{#map}

Digite o conteúdo do usuário para um mapa interativo.

O mapa permite transmitir o conteúdo geotsinalizado em um mapa do mundo, permitindo localizar o buzz social em torno de notícias ou um evento ao vivo. Todo o conteúdo aplicável será exibido, incluindo texto, comentários, fotos e tweets.

>[!NOTE]
>
>Os mapas são fornecidos por [© openstreetmap](https://www.openstreetmap.org/copyright), que fornece os dados do Livefyre usados para renderizar seus Mapas.

## Integração {#section_w2m_db2_d1b}

A maneira mais rápida de usar o Mapa é usar a versão incorporada hospedada no CDN do Livefyre.

Primeiro, adicione [Livefyre. js](https://github.com/Livefyre/Livefyre.js) à sua página.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Em seguida, posicione o elemento no qual o aplicativo Mapa será exibido.

```
<div id="map" style="height: 500px;"></div>
```

Por fim, use o Livefyre. necessário para criar o Mapa e obter uma coleção com o objetivo de fazer o pipe de um sdk simplificado. Lembre-se de que o Mapa pode mostrar somente conteúdo com metadados geotmarcados. O Twitter e o Instagram Curate oferecem suporte para esse recurso. Para garantir o melhor desempenho, inclua um filtro de geolocalização em todas as Regras de preparação para a coleção.

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

Confira este [exemplo ao vivo](https://codepen.io/cheung31/pen/wkmbF).

## Configuração {#section_jc5_gxb_c1b}

`initial`

O número inicial de itens a serem carregados da coleção e exibidos no mapa. Depois que esse número for carregado, os usuários poderão clicar em um botão para mostrar mais. (Opcional. Padrões para 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opções para passar para o Mapa [de leaflet](https://leafletjs.com/) subjacente, que o Mapa usa para renderização. Use essa opção para definir [Opções do Mapa de opção](https://leafletjs.com/reference.html#map-options), incluindo o centro inicial do mapa, e os níveis de zoom inicial e máxima. (Opcional.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

