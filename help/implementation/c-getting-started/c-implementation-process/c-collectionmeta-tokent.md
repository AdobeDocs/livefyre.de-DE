---
description: Erstellen Sie auf Ihrem Server ein eindeutiges Token, das jede von Ihnen
  erstellte Sammlung kennzeichnet.
seo-description: Erstellen Sie auf Ihrem Server ein eindeutiges Token, das jede von
  Ihnen erstellte Sammlung kennzeichnet.
seo-title: Collectionmeta Token
solution: Experience Manager
title: Collectionmeta Token
uuid: d 5 db 0 b 0 f -2807-4392-874 a -94 ac 3 c 1 e 7550
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Collectionmeta Token{#collectionmeta-token}

Erstellen Sie auf Ihrem Server ein eindeutiges Token, das jede von Ihnen erstellte Sammlung kennzeichnet.

Livefyre weist jeder erstellten Sammlung einen eindeutigen Bezeichner zu. Livefyre weist einen Titel, eine URL und andere Parameter zu, einschließlich:

## Collectionmeta Token-Parameter

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| Networkname | Zeichenfolge (optional) | Der Name des Livefyre-Netzwerks (verfügbar unter {! UICONTROL Studio > Einstellungen > Integrationseinstellungen > Anmeldeinformationen]). Dies ist optional, wenn Sie mit der Bibliothek ein collectionmeta-Token erstellen. |
| Networkkey | Zeichenfolge (optional) | Der geheime Schlüssel für das spezifische Netzwerk (verfügbar unter Studio > Einstellungen > Integrationseinstellungen > Anmeldeinformationen). Dies ist optional, wenn Sie mit der Bibliothek ein collectionmeta-Token erstellen. |
| Siteid | Zeichenfolge (optional) | Die ID für die Site (verfügbar ab [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Optional, wenn Sie die Bibliothek verwenden, um ein collectionmeta-Token zu erstellen. |
| Sitekey | Zeichenfolge (optional) | Der geheime Schlüssel für die Site (verfügbar unter {! UICONTROL Studio > Einstellungen > Integrationseinstellungen > Anmeldeinformationen]). |
| Articleid | Zeichenfolge (optional) | Eine eindeutige ID für die Sammlung. |
| Titel | Zeichenfolge (optional) | Der Titel, den Sie auf die Sammlung anwenden möchten. Normalerweise entspricht dies dem Titel der Seite, auf der die App angezeigt wird. <br>Beispiel: " Integration ist so viel Spaß! » <br>Hinweis: Die maximale Zeichenlänge für den Titel beträgt 255 Zeichen. Das Titelfeld unterstützt keine HTML-Entitäten. Bitte Sonderzeichen mit UTF -8 kodieren. |
| url | Zeichenfolge (optional) | Die kanonische absolute URL, die an diese Sammlung angehängt werden soll. Diese URL wird verwendet, um Links aus Inhalten, die auf Facebook und Twitter, E-Email-Benachrichtigungen und Livefyre Studio freigegeben wurden, wiederherzustellen. <br>Hinweis: Wenn Sie lokal testen, verwenden Sie eine gültige Basis-URL-Domäne (z. B.: valid: `https://customer.com`; ungültig: `https://localhost:5995`). |
| Tags | Zeichenfolge (optional) | Eine kommagetrennte Liste mit einzelnen Suchbegriffen oder -phrasen. Suchen Sie Sammlungen nach Tags mit Studio. </br>Hinweis: Tags dürfen keine Leerzeichen enthalten. Verwenden Sie Unterstriche, wenn in der Benutzeroberfläche ein Leerzeichen angezeigt werden soll. |
| Erweiterungen | JSON (optional) | Ein JSON-formatierter Satz von Parametern, die an die Sammlung weitergegeben werden. |

## Java {#section_orz_m4n_sz}

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

>[!NOTE] {important = "high"}
>
>Livefyre empfängt das von Ihnen erstellte collectionmeta-Token und ermittelt Eindeutigkeit durch Kombinieren von siteid (Livefyre bereitgestellt) und articleid (Kunde angegeben).

