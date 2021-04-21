---
description: Faça o mapeamento do conteúdo do usuário para um mapa interativo.
title: Mapa
exl-id: 836b475e-0ec6-49f8-b89f-3af3209cf1f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# Mapa{#map}

Faça o mapeamento do conteúdo do usuário para um mapa interativo.

O mapa permite que você faça stream de conteúdo com tags geográficas em um mapa do mundo, permitindo que você localize o burburinho social em torno de notícias novas ou de um evento ao vivo. Todo o conteúdo aplicável será exibido, incluindo texto, comentários, fotos e tweets.

>[!NOTE]
>
>Os mapas são fornecidos por [ @ OpenStreetMap](https://www.openstreetmap.org/copyright), que fornece os dados que o Livefyre usa para renderizar seus Mapas.

## Integração {#section_w2m_db2_d1b}

A maneira mais rápida de usar o Mapa é usar a versão criada hospedada no CDN da Livefyre.

Primeiro, adicione [Livefyre.js](https://github.com/Livefyre/Livefyre.js) à sua página.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Em seguida, posicione o elemento no qual o aplicativo de mapa será exibido.

```
<div id="map" style="height: 500px;"></div>
```

Por fim, use Livefyre.require para construir o Mapa e obter uma coleção para encurtar a partir do stream-sdk. Lembre-se de que o Mapa pode mostrar somente o Conteúdo com metadados com tags. O twitter e o Instagram Preparate oferecem suporte a esse recurso. Para garantir melhor desempenho, inclua um filtro de geolocalização em todas as Regras de preparação para a coleção.

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

Confira este [live example](https://codepen.io/cheung31/pen/wkmbF).

## Configuração {#section_jc5_gxb_c1b}

`initial`

O número inicial de itens a serem carregados da Coleção e exibidos no mapa. Após o carregamento desse número, os usuários podem clicar em um botão para mostrar mais. (Opcional. O padrão é 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opções a serem passadas para o mapa subjacente [Folheto](https://leafletjs.com/), que o Mapa usa para renderização. Use esta opção para definir [Opções de mapa de folheto](https://leafletjs.com/reference.html#map-options), incluindo o ponto central inicial do mapa, e os níveis inicial e máximo de zoom. (Opcional.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```
