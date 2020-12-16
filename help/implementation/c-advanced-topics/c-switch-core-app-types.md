---
description: Erfahren Sie, wie Sie von einem Konversations-App-Typ zu einem anderen wechseln.
seo-description: Erfahren Sie, wie Sie von einem Konversations-App-Typ zu einem anderen wechseln.
seo-title: Core-App-Typen wechseln
solution: Experience Manager
title: Core-App-Typen wechseln
uuid: 442a517c-3809-46c5-bb5f-8668a29dc3e8
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---


# Core-App-Typen umschalten{#switch-core-app-types}

Erfahren Sie, wie Sie von einem Konversations-App-Typ zu einem anderen wechseln.

Mit LiveCycle können Sie Sammlungen von einem Livefyre-Core-Anwendungstyp in einen anderen ändern (Kommentare, Live-Blog oder Chat), indem Sie einfach einige Einstellungen in Ihren `collectionMeta`-Daten ändern.

Um einen bestimmten App-Typ zu implementieren, fügen Sie dem `collectionMeta`-Objekt ein neues Feld hinzu. Kommentare ist die Standardeinstellung. Daher müssen Sie diese Aktualisierungen nicht vornehmen, wenn dies Ihre gewünschte App ist. Um nach dem Erstellen einer Sammlung zu einer anderen App zu wechseln, übergeben Sie während der App-Initialisierung einen Prüfsummenwert. Lesen Sie mehr über das Erstellen eines Prüfsummenwerts in unserer Token-Dokumentation.`collectionMeta`

## Live-Blog {#section_kvj_3jj_11b}

### PHP-Beispiel

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

### Python-Beispiel

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

### Ruby-Beispiel

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

## Live-Blog {#section_bqt_cjj_11b}

### PHP-Beispiel

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

### Python-Beispiel

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

### Ruby-Beispiel

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

## Chat {#section_dqm_w3j_11b}

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

### Python-Beispiel

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

### Ruby-Beispiel

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
