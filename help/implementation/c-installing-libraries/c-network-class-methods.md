---
description: Erstellen Sie ein Netzwerkobjekt.
seo-description: Erstellen Sie ein Netzwerkobjekt.
seo-title: Netzwerkklassenmethoden
solution: Experience Manager
title: Netzwerkklassenmethoden
uuid: 4130 beda-dd 9-49 ae-aafb-f 6 b 956 e 30 b 51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Netzwerkklassenmethoden{#network-class-methods}

Erstellen Sie ein Netzwerkobjekt.

Sobald Sie ein Netzwerkobjekt erstellt haben, geht der Rest der Seite davon aus, dass Sie in Ihrer Sitzung ein instanziiertes Netzwerkobjekt haben.

## Netzwerkobjekt

| Parameter | Typ | Beschreibung |
|---|---|---|
| *`network`* | Zeichenfolge | Ihr Livefyre-Netzwerk. Beispiel: «`labs.fyre.co`». |
| *`networkKey`* | Zeichenfolge | Der geheime geheime Schlüssel für das Netzwerk. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## Nodejs {#section_nyk_dzs_kbb}

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
