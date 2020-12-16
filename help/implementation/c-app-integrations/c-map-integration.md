---
description: Faça o plotagem do conteúdo do usuário em um mapa interativo.
seo-description: Faça o plotagem do conteúdo do usuário em um mapa interativo.
seo-title: Mapa
solution: Experience Manager
title: Mapa
uuid: 1c3e399d-a610-4b80-a3b2-a5502b31480d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 2%

---


# Mapa{#map}

Faça o plotagem do conteúdo do usuário em um mapa interativo.

O mapa permite que você faça streaming de conteúdo com tags geográficas em um mapa do mundo, permitindo que você localize o burburinho social em torno de notícias ou eventos ao vivo. Todo o conteúdo aplicável será exibido, incluindo texto, comentários, fotos e tweets.

>[!NOTE]
>
>Os mapas são capacitados por [ ©OpenStreetMap](https://www.openstreetmap.org/copyright), que fornece os dados que o Livefyre usa para renderizar seus Mapas.

## Integração {#section_w2m_db2_d1b}

A maneira mais rápida de usar o Mapa é usar a versão incorporada hospedada no CDN da Livefyre.

Primeiro, adicione [Livefyre.js](https://github.com/Livefyre/Livefyre.js) à sua página.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Em seguida, posicione o elemento no qual o aplicativo Mapa aparecerá.

```
<div id="map" style="height: 500px;"></div>
```

Por fim, use Livefyre.requirements para construir o Mapa e obter uma Coleção para encanar do stream-sdk. Lembre-se de que o Mapa pode mostrar somente o Conteúdo com metadados marcados geograficamente. O Twitter e o Instagram Curate suportam esse recurso. Para garantir melhor desempenho, inclua um filtro de localização geográfica em todas as Regras de preparação para a coleção.

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

O número inicial de itens a serem carregados da Coleção e exibidos no mapa. Depois que esse número é carregado, os usuários podem clicar em um botão para mostrar mais. (Opcional. O padrão é 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Opções para passar para o mapa subjacente [Folheto](https://leafletjs.com/), que o Mapa usa para renderização. Use essa opção para definir [Opções de mapa de folheto](https://leafletjs.com/reference.html#map-options), incluindo o ponto central inicial do mapa, e os níveis inicial e máximo de zoom. (Opcional.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

