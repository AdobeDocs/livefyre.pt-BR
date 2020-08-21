---
description: Crie um token exclusivo no servidor que identifique cada coleção criada.
seo-description: Crie um token exclusivo no servidor que identifique cada coleção criada.
seo-title: CollectionMeta Token
solution: Experience Manager
title: CollectionMeta Token
uuid: d5db0b0f-2807-4392-874a-94ac3c1e7550
translation-type: tm+mt
source-git-commit: 6978f0f36b5698c9c599c1828edea67703423397
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 2%

---


# CollectionMeta Token{#collectionmeta-token}

Crie um token exclusivo no servidor que identifique cada coleção criada.

O Livefyre atribui um identificador exclusivo a todas as Coleções que você criar. Livefyre atribui um título, URL e outros parâmetros, incluindo:

## Parâmetros do collectionMeta Token

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| networkName | Sequência (opcional) | O nome da rede Livefyre (disponível em [!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials] ). Isso é opcional ao usar a biblioteca para criar um collectionMeta token. |
| networkKey | Sequência (opcional) | A chave secreta para a rede específica (disponível em Studio > Configurações > Configurações de integração > Credenciais ). Isso é opcional ao usar a biblioteca para criar um collectionMeta token. |
| siteId | Sequência (opcional) | A ID do site (disponível em [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Opcional ao usar a biblioteca para criar um collectionMeta token. |
| siteKey | Sequência (opcional) | A chave secreta do site (disponível em [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). |
| articleId | Sequência (opcional) | Uma ID exclusiva para a coleção. |
| title | Sequência (opcional) | O título que você deseja aplicar à Coleção. Normalmente, isso corresponde ao título da página que exibe o aplicativo. <br>Por exemplo: &quot;A integração é tão divertida!&quot; <br>Observação:  O comprimento máximo de caracteres para o título é de 255 caracteres. O campo de título não suporta entidades HTML. Codifique caracteres especiais usando UTF-8. |
| url | String (opcional) | O URL absoluto canônico que você deseja anexar a esta Coleção. Esse URL será usado para gerar links de volta ao aplicativo a partir de conteúdo compartilhado no Facebook e no Twitter, notificações por email e Livefyre Studio. <br>Observação:  Se estiver testando localmente, use um domínio de URL base válido (por exemplo: válido: `https://customer.com`; inválido: `https://localhost:5995`). |
| específicos | Sequência (opcional) | Uma lista separada por vírgulas de palavras-chave únicas ou frases. Pesquisar coleções por tags usando o Studio.  </br>Observação:  As tags não podem conter espaços. Use sublinhados se desejar que um espaço apareça na interface do usuário. |
| extensões | JSON (opcional) | Um conjunto formatado de parâmetros JSON para passar para a Coleção. |

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

## NodeJS {#section_kpk_44n_sz}

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

>[!NOTE]
>
>O Livefyre recebe a coleçãoMeta token que você cria e determina a exclusividade combinando o siteId (fornecido pelo Livefyre) e o articleId (especificado pelo cliente).
