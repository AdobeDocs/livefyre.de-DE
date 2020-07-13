---
description: Erstellen Sie ein eindeutiges Token auf Ihrem Server, das jede von Ihnen erstellte Sammlung identifiziert.
seo-description: Erstellen Sie ein eindeutiges Token auf Ihrem Server, das jede von Ihnen erstellte Sammlung identifiziert.
seo-title: CollectionMeta-Token
solution: Experience Manager
title: CollectionMeta-Token
uuid: d5db0b0f-2807-4392-874a-94ac3c1e7550
translation-type: tm+mt
source-git-commit: acba83da6abd919062025322beeced500a3db662
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 2%

---


# CollectionMeta-Token{#collectionmeta-token}

Erstellen Sie ein eindeutiges Token auf Ihrem Server, das jede von Ihnen erstellte Sammlung identifiziert.

Livefyre weist jeder erstellten Sammlung einen eindeutigen Bezeichner zu. Livefyre weist einen Titel, eine URL und andere Parameter zu, darunter:

## collectionMeta-Token-Parameter

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| networkName | Zeichenfolge (optional) | Der Name des Livefyre-Netzwerks (verfügbar unter {!UICONTROL Studio > Einstellungen > Integrationseinstellungen > Berechtigungen] ). Dies ist optional, wenn Sie mit der Bibliothek ein collectionMeta-Token erstellen. |
| networkKey | Zeichenfolge (optional) | Der geheime Schlüssel für das spezifische Netzwerk (verfügbar unter Studio > Einstellungen > Integrationseinstellungen > Anmeldeinformationen ). Dies ist optional, wenn Sie mit der Bibliothek ein collectionMeta-Token erstellen. |
| siteId | Zeichenfolge (optional) | Die ID für die Site (verfügbar unter [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Optional, wenn Sie mit der Bibliothek ein collectionMeta-Token erstellen. |
| siteKey | Zeichenfolge (optional) | Der geheime Schlüssel für die Site (verfügbar unter {!UICONTROL Studio > Einstellungen > Integrationseinstellungen > Berechtigungen] ). |
| articleId | Zeichenfolge (optional) | Eine eindeutige ID für die Sammlung. |
| title | Zeichenfolge (optional) | Der Titel, den Sie auf die Sammlung anwenden möchten. Normalerweise entspricht dies dem Titel der Seite, auf der die App angezeigt wird. <br>Beispiel: &quot;Integration macht so viel Spaß!&quot; <br>Hinweis:  Die maximale Zeichenlänge für den Titel beträgt 255 Zeichen. Das Titelfeld unterstützt keine HTML-Entitäten. Bitte kodieren Sie Sonderzeichen mit UTF-8. |
| url | Zeichenfolge (optional) | Die kanonische absolute URL, die Sie dieser Sammlung hinzufügen möchten. Diese URL wird verwendet, um aus Inhalten, die auf Facebook und Twitter freigegeben wurden, E-Mail-Benachrichtigungen und Livefyre Studio Links zur App zu generieren. <br>Hinweis:  Verwenden Sie bei lokalen Tests eine gültige Basis-URL-Domäne (z. B.: gültig: `https://customer.com`; ungültig: `https://localhost:5995`). |
| Tags | Zeichenfolge (optional) | Eine kommagetrennte Liste von einzelnen Suchbegriffen oder Ausdrücken. Sammlungen mit Studio nach Tags durchsuchen  </br>Hinweis:  Tags dürfen keine Leerzeichen enthalten. Verwenden Sie Unterstriche, wenn ein Leerzeichen in der Benutzeroberfläche angezeigt werden soll. |
| Erweiterungen | JSON (optional) | Ein JSON-formatierter Satz von Parametern, die an die Sammlung übergeben werden. |

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
>Livefyre empfängt das von Ihnen erstellte collectionMeta-Token und bestimmt die Eindeutigkeit durch Kombination von siteId (Livefyre bereitgestellt) und articleId (kundenspezifisch).
