---
description: Saiba como mudar de um tipo de aplicativo de conversa para outro.
title: Alternar tipos de aplicativos principais
exl-id: f18c97e8-8f39-4831-b907-afd438097e9e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 1%

---

# Alternar tipos de aplicativos principais{#switch-core-app-types}

Saiba como mudar de um tipo de aplicativo de conversa para outro.

O Lifefyre permite alterar as Coleções de um tipo de Aplicativo Principal do Livefyre para outro (Comentários, Blog em tempo real ou Chat) simplesmente alterando algumas configurações nos seus dados `collectionMeta`.

Para implementar um tipo específico de Aplicativo, adicione um novo campo ao objeto `collectionMeta`. Os comentários são o padrão, portanto, você não precisará fazer essas atualizações se esse for o aplicativo desejado. Para alterar para um aplicativo diferente depois que uma coleção é criada, passe um valor de soma de verificação durante a inicialização do aplicativo. Leia mais sobre como criar um valor de soma de verificação na documentação do token `collectionMeta`.

## Blog ao vivo {#section_kvj_3jj_11b}

### Exemplo de PHP

```
use LivefyreLivefyre; 
  
$articleId = "1"; 
$articleTitle = "Title 1"; 
$articleURL = "https://dev.livefyre.com"; 
$articleTags = "tag1,tag2"; 
$lfType = "livecomments"; 
  
$network = Livefyre::getNetwork(networkName, networkKey); 
$site = network->getSite(siteId, siteKey); 
  
$collectionMeta = $site->buildCollectionMetaToken( 
   $articleTitle, 
   $articleURL, 
   $articleTags, 
   $lfType 
); 
  
$convConfig = array( 
   "el" => "targetElement", 
   "checksum" => $checksum, 
   "collectionMeta" => $collectionMeta, 
   "siteId" => <YOUR SITE ID>, 
   "articleId" => <ARTICLE ID> 
);
```

### Exemplo de Python

```
from livefyre import Livefyre 
  
article_id = "1" 
article_title = "Title 1" 
article_url = "https://dev.livefyre.com" 
article_tags = "tag1,tag2" 
lf_type = "livecomments" 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token( 
   article_title, 
   article_url, 
   article_tags, 
   lf_type, 
) 
  
conv_config = dict( 
   "el" = "targetElement", 
   "checksum" = checksum, 
   "collectionMeta" = collection_meta_token, 
   "siteId" = <YOUR SITE ID>, 
   "articleId" = <ARTICLE ID> 
)
```

### Exemplo de Ruby

```
require 'livefyre'  
article_id = "1"  
title = "Title 1"  
link = "https://dev.livefyre.com"  
tag_str = "tag1,tag2"  
lf_type = "livecomments"  
  
network = Livefyre.get_network(networkName, networkKey)  
site = network.get_site(siteId, siteKey)  
  
collection_meta = site.build_collection_meta_token( 
   title, 
   link, 
   tag_str || "", 
   lf_type, 
)  
  
conv_config = { 
   :el => targetElement, 
   :checksum => checksum, 
   :collectionMeta => collection_meta_token, 
   :siteId => <YOUR SITE ID>, 
   :articleId => <ARTICLE ID> 
}
```

## Blog ao vivo {#section_bqt_cjj_11b}

### Exemplo de PHP

```
use LivefyreLivefyre; 
  
$articleId = "1"; 
$articleTitle = "Title 1"; 
$articleURL = "https://dev.livefyre.com"; 
$articleTags = "tag1,tag2"; 
$lfType = "liveblog"; 
  
$network = Livefyre::getNetwork(networkName, networkKey); 
$site = network->getSite(siteId, siteKey); 
  
$collectionMeta = $site->buildCollectionMetaToken( 
   $articleTitle, 
   $articleURL, 
   $articleTags, 
   $lfType 
); 
  
$convConfig = array( 
   "el" => "targetElement", 
   "checksum" => $checksum, 
   "collectionMeta" => $collectionMeta, 
   "siteId" => <YOUR SITE ID>, 
   "articleId" => <ARTICLE ID>  
);
```

### Exemplo de Python

```
from livefyre import Livefyre 
  
article_id = "1" 
article_title = "Title 1" 
article_url = "https://dev.livefyre.com" 
article_tags = "tag1,tag2" 
lf_type = "liveblog" 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token( 
   article_title, 
   article_url, 
   article_tags, 
   lf_type, 
) 
  
conv_config = dict( 
   "el" = "targetElement", 
   "checksum" = checksum, 
   "collectionMeta" = collection_meta_token, 
   "siteId" = <YOUR SITE ID>, 
   "articleId" = <ARTICLE ID> 
)
```

### Exemplo de Ruby

```
require 'livefyre' 
  
article_id = "1" 
title = "Title 1" 
link = "https://dev.livefyre.com" 
tag_str = "tag1,tag2" 
lf_type = "liveblog" 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token( 
   title, 
   link, 
   tag_str || "", 
   lf_type, 
) 
  
conv_config = { 
   :el => targetElement, 
   :checksum => checksum, 
   :collectionMeta => collection_meta_token, 
   :siteId => <YOUR SITE ID>, 
   :articleId => <ARTICLE ID> 
}
```

## Bate-papo {#section_dqm_w3j_11b}

### PHP

```
use LivefyreLivefyre; 
  
$articleId = "1"; 
$articleTitle = "Title 1"; 
$articleURL = "https://dev.livefyre.com"; 
$articleTags = "tag1,tag2"; 
$lfType = "livechat"; 
  
$network = Livefyre::getNetwork(networkName, networkKey); 
$site = network->getSite(siteId, siteKey); 
  
$collectionMeta = $site->buildCollectionMetaToken 
   $articleTitle, 
   $articleURL, 
   $articleTags, 
   $lfType 
); 
  
$convConfig = array( 
   "el" => "targetElement", 
   "checksum" => $checksum, 
   "collectionMeta" => $collectionMeta, 
   "siteId" => <YOUR SITE ID>, 
   "articleId" => <ARTICLE ID> 
);
```

### Exemplo de Python

```
from livefyre import Livefyre 
  
article_id = "1" 
article_title = "Title 1" 
article_url = "https://dev.livefyre.com" 
article_tags = "tag1,tag2" 
lf_type = "livechat" 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token(  
   article_title,  
   article_url,  
   article_tags,  
   lf_type,  
)

conv_config = dict( "el" = "targetElement", 
   "checksum" = checksum, 
   "collectionMeta" = collection_meta_token, 
   "siteId" = <YOUR SITE ID>, 
   "articleId" = <ARTICLE ID> 
)
```

### Exemplo de Ruby

```
require 'livefyre' 
  
article_id = "1" 
title = "Title 1" 
link = "https://dev.livefyre.com" 
tag_str = 'tag1,tag2' 
lf_type = 'livechat' 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token(  
   title,  
   link, 
   tag_str || "", 
   lf_type, 
) 
  
conv_config = { 
   :el => targetElement, 
   :checksum => checksum, 
   :collectionMeta => collection_meta_token, 
   :siteId => <YOUR SITE ID>, 
   :articleId => <ARTICLE ID> 
}
```
