---
description: Crie um objeto de rede.
seo-description: Crie um objeto de rede.
seo-title: Métodos de classe de rede
solution: Experience Manager
title: Métodos de classe de rede
uuid: 4130beda-dd09-49ae-aafb-f6b956e30b51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Métodos de classe de rede{#network-class-methods}

Crie um objeto de rede.

Depois que você criar um objeto de rede, o restante da página presumirá que você tem um objeto de rede instanciado em sua sessão.

## Objeto de rede

| Parâmetro | Tipo | Descrição |
|---|---|---|
| *`network`* | String   | Sua rede Livefyre. Por exemplo: “`labs.fyre.co`”. |
| *`networkKey`* | String   | A chave secreta fornecida pela Livefyre para a rede. |

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
