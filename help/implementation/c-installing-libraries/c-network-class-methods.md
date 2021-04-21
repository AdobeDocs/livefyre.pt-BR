---
description: Crie um objeto Rede.
title: Métodos de classe de rede
exl-id: 5a011120-05d0-4768-9038-6a312e8c5dd1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 14%

---

# Métodos de Classe de Rede{#network-class-methods}

Crie um objeto Rede.

Depois de criar um objeto de rede, o restante da página presumirá que você tem um objeto de rede instanciado em sua sessão.

## Objeto de rede

| Parâmetro | Tipo | Descrição |
|---|---|---|
| *`network`* | String   | Sua rede Livefyre. Por exemplo: “`labs.fyre.co`”. |
| *`networkKey`* | String   | A chave secreta fornecida pelo Livefyre para a rede. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## NodeJS {#section_nyk_dzs_kbb}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork(network, networkKey); 
```

## PHP {#section_oyk_dzs_kbb}

```
use Livefyre\Livefyre; 
  
$network = Livefyre::getNetwork(network, networkKey); 
```

## Python {#section_pyk_dzs_kbb}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network(network, networkKey) 
```

## Ruby {#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
