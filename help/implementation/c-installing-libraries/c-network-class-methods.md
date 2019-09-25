---
description: Erstellen Sie ein Netzwerkobjekt.
seo-description: Erstellen Sie ein Netzwerkobjekt.
seo-title: Methoden der Netzwerkklasse
solution: Experience Manager
title: Methoden der Netzwerkklasse
uuid: 4130beda-dd09-49ae-aafb-f6b956e30b51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Methoden der Netzwerkklasse{#network-class-methods}

Erstellen Sie ein Netzwerkobjekt.

Nachdem Sie ein Netzwerkobjekt erstellt haben, geht die restliche Seite davon aus, dass Sie ein instanziiertes Netzwerkobjekt in Ihrer Sitzung haben.

## Netzwerkobjekt

| Parameter | Typ | Beschreibung |
|---|---|---|
| *`network`* | Zeichenfolge | Ihr Livefyre-Netzwerk. Beispiel: “`labs.fyre.co`”. |
| *`networkKey`* | Zeichenfolge | Der Livefyre-geheime Schlüssel für das Netzwerk. |

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
