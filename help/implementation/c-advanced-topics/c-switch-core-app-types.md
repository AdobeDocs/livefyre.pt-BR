---
description: Saiba como mudar de um tipo de aplicativo de conversa para outro.
seo-description: Saiba como mudar de um tipo de aplicativo de conversa para outro.
seo-title: Alternar tipos de aplicativo principal
solution: Experience Manager
title: Alternar tipos de aplicativo principal
uuid: 442 a 517 c -3809-46 c 5-bb 5 f -8668 a 29 dc 3 e 8
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Alternar tipos de aplicativo principal{#switch-core-app-types}

Saiba como mudar de um tipo de aplicativo de conversa para outro.

O Lifefyre permite alterar Coleções de um tipo de Aplicativo principal do Livefyre para outro (Comentários, Blog ao vivo ou Bate-papo) simplesmente alterando algumas configurações em seus `collectionMeta` dados.

Para implementar um tipo específico de aplicativo, adicione um novo campo ao `collectionMeta` seu objeto. Os comentários são o padrão para que você não precise fazer essas atualizações se esse for o seu aplicativo desejado. Para mudar para um aplicativo diferente após a criação de uma coleção, passe um valor de soma de verificação durante a inicialização do aplicativo. Leia mais sobre como criar um valor de soma de verificação na documentação `collectionMeta` do token.

## Blog ao vivo {#section_kvj_3jj_11b}

### Exemplo PHP

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

### Rupor exemplo

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

### Exemplo PHP

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

### Rupor exemplo

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

### Rupor exemplo

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