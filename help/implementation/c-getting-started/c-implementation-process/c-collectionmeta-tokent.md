---
description: Crie um token exclusivo no seu servidor que identifica cada coleção criada.
seo-description: Crie um token exclusivo no seu servidor que identifica cada coleção
  criada.
seo-title: Collectionmeta token
solution: Experience Manager
title: Collectionmeta token
uuid: d 5 db 0 b 0 f -2807-4392-874 a -94 ac 3 c 1 e 7550
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Collectionmeta token{#collectionmeta-token}

Crie um token exclusivo no seu servidor que identifica cada coleção criada.

O Livefyre atribui um identificador exclusivo a cada coleção criada. O Livefyre atribui um título, URL e outros parâmetros, incluindo:

## Parâmetros collectionmeta Token

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| Networkname | String (opcional) | O nome da rede Livefyre (disponível em {! UICONTROL Studio > Configurações > Configurações de integração > Credenciais]). Isso é opcional ao usar a biblioteca para criar um token collectionmeta. |
| Networkkey | String (opcional) | A chave secreta da rede específica (disponível em Studio > Configurações > Configurações de integração > Credenciais). Isso é opcional ao usar a biblioteca para criar um token collectionmeta. |
| Siteid | String (opcional) | A ID do site (disponível [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Opcional ao usar a biblioteca para criar um token collectionmeta. |
| Sitekey | String (opcional) | A chave secreta do site (disponível em {! UICONTROL Studio > Configurações > Configurações de integração > Credenciais]). |
| Articleid | String (opcional) | Uma ID exclusiva para a Coleção. |
| title | String (opcional) | O título que você deseja aplicar à Coleção. Geralmente, isso corresponde ao título da página que exibe o Aplicativo. <br>Por exemplo: «A integração é tão divertida! » <br>Observação: A extensão máxima de caracteres do título é de 255 caracteres. O campo de título não suporta entidades HTML. Codifice caracteres especiais usando UTF -8. |
| url | String (opcional) | O URL canônico canônico que deseja anexar a esta coleção. Esse URL será usado para gerar links de volta ao aplicativo a partir de conteúdo compartilhado no Facebook e Twitter, notificações por email e Livefyre Studio. <br>Observação: Se estiver testando localmente, use um domínio de URL base válido (por exemplo: válido: `https://customer.com`; inválido: `https://localhost:5995`). |
| tags | String (opcional) | Uma lista separada por vírgulas ou frases separadas. Pesquisar coleções por tags usando o Studio. </br>Observação: As tags não podem conter espaços. Use sublinhados se desejar que um espaço apareça na interface do usuário. |
| extensões | JSON (opcional) | Um conjunto formatado JSON de params para passar para a coleção. |

## Java {#section_orz_m4n_sz}

```
import com.livefyre.Livefyre; 
import com.livefyre.core.Network; 
import com.livefyre.core.Site; 
import com.livefyre.core.Collection; 
  
Network network = Livefyre.getNetwork("networkName", "networkKey"); 
Site site = network.getSite("siteId", "siteKey"); 
Collection collection = site.buildCommentsCollection("title", "articleId", "https://www.example.com"); 
collection.getData().setTags("tags"); 
  
String collectionMetaToken = collection.buildCollectionMetaToken();
```

## Nodejs {#section_kpk_44n_sz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken(); 
```

## PHP {#section_zmd_zbj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken();
```

## Python {#section_rdm_prj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## Ruby {#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE] {importance = "high"}
>
>O Livefyre recebe o collectionmeta token que você cria e determina singularidade combinando siteid (Livefyre fornecido) e articleid (cliente especificado).

