---
description: Criar um objeto de rede.
seo-description: Criar um objeto de rede.
seo-title: Métodos de classe de rede
solution: Experience Manager
title: Métodos de classe de rede
uuid: 4130 beda-dd 09-49 ae-aafb-f 6 b 956 e 30 b 51
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Métodos de classe de rede{#network-class-methods}

Criar um objeto de rede.

Após a criação de um objeto de rede, o restante da página pressuporá que você tenha um objeto de rede instanciado na sua sessão.

## Objeto de rede

| Parâmetro | Tipo | Descrição |
|---|---|---|
| *`network`* | String | Sua rede do Livefyre. Por exemplo: «`labs.fyre.co`». |
| *`networkKey`* | String | A chave secreta fornecida pelo Livefyre para a rede. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## Nodejs {#section_nyk_dzs_kbb}

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
