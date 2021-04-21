---
description: Crie um token exclusivo em seu servidor que identifique todas as coleções que você criar.
title: CollectionMeta Token
exl-id: 52edfe75-5ce6-40c9-9afe-c34a3812f1e7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 3%

---

# CollectionMeta Token{#collectionmeta-token}

Crie um token exclusivo em seu servidor que identifique todas as coleções que você criar.

O Livefyre atribui um identificador exclusivo a cada coleção que você criar. Livefyre atribui um título, URL e outros parâmetros, incluindo:

## Parâmetros de token collectionMeta

| Parâmetro | Tipo | Descrição |
|--- |--- |--- |
| networkName | String (opcional) | O nome da rede Livefyre (disponível em [!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials] ). Isso é opcional ao usar a biblioteca para criar um token collectionMeta. |
| networkKey | String (opcional) | A chave secreta para a rede específica (disponível em Studio > Configurações > Configurações de integração > Credenciais ). Isso é opcional ao usar a biblioteca para criar um token collectionMeta. |
| siteId | String (opcional) | A ID do site (disponível em [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Opcional ao usar a biblioteca para criar um token collectionMeta. |
| siteKey | String (opcional) | A chave secreta do site (disponível em [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). |
| articleId | String (opcional) | Uma ID exclusiva para a coleção. |
| title | String (opcional) | O título que deseja aplicar à Coleção. Geralmente, isso corresponde ao título da página que exibe o aplicativo. <br>Por exemplo: &quot;A integração é tão divertida!&quot; <br>Observação: O comprimento máximo de caracteres do título é de 255 caracteres. O campo de título não é compatível com entidades HTML. Codifique caracteres especiais usando UTF-8. |
| url | String (opcional) | O URL absoluto canônico que você deseja anexar a essa coleção. Esse URL será usado para gerar links para o aplicativo a partir de conteúdo compartilhado no Facebook e no Twitter, notificações por email e o Livefyre Studio. <br>Observação: Se estiver testando localmente, use um domínio de URL de base válido (por exemplo: válido:  `https://customer.com`; inválido:  `https://localhost:5995`). |
| específicos | String (opcional) | Uma lista separada por vírgulas de palavras-chave ou frases únicas. Pesquise coleções por tags usando o Studio.  </br>Observação: As tags não podem conter espaços. Use sublinhados se quiser que um espaço apareça na interface do usuário. |
| extensões | JSON (opcional) | Um conjunto de parâmetros formatado por JSON para transmitir à Coleção. |

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
>O Livefyre recebe o collectionMeta token criado e determina a exclusividade ao combinar o siteId (fornecido pelo Livefyre) e o articleId (especificado pelo cliente).
