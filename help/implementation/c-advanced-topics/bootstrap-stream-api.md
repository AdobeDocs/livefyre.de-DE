---
description: Verwenden Sie die Bootstrap- und Stream-API mit Livefyre-Apps.
title: Ansicht der Kontodetails
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Bootstrap- und Stream-API mit Livefyre-Apps {#bootstrap-stream-api} verwenden

## Bootstrap-API {#bootstrap-api}

### Wie kann ich Inhalte abrufen, die älter als die neuesten 50 Stücke sind? {#howcontentolder}

Bootstrap enthält alle Inhalte in einer Livefyre-App. Es handelt sich um die zwischengespeicherten Daten, in der Regel 12-20 Minuten alt. Es wird in Blöcken von 50 Stück geliefert und paginiert, damit Sie Inhalte abrufen können, die älter als 50 Stück sind.

[API-Referenz](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Beispielanforderung](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

Die obige Beispielanforderung lädt die Seite `init`, die Sammlungseinstellungen und den einzigen anfänglichen Satz von ~50 Elementen des neuesten Inhalts enthält. Um ältere Inhalte abzurufen, müssen Sie nachfolgende Bootstrap-Seiten laden, wobei `N` die Seitenzahl ist:

Anfrage: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Eine Beispielanwendung enthält beispielsweise 120 Inhaltselemente. Content &quot;1&quot; ist das älteste Inhaltselement und Content &quot;70&quot; ist das neueste Inhaltselement.

* `Init` werden ca. 120-70 Inhaltselemente in absteigender Reihenfolge geladen:  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` werden ~ 1-50 Inhaltselemente in aufsteigender Reihenfolge geladen:  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` werden ca. 51-100 Inhaltselemente in aufsteigender Reihenfolge geladen:  [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` werden Inhalte von ca. 101-120 Stück in aufsteigender Reihenfolge geladen:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Klicken Sie hier, um das Flussdiagramm für die Bootstrap-Umfrage anzuzeigen.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## Stream-API {#stream-api}

Was ist die Stream-API?
Stream ist eine lange Umfrage, die planmäßig für ca. 30 Sekunden offen bleiben soll. Beschreibung zur Methode des langen Abrufs finden Sie hier: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Dieser lange Abruf-Endpunkt streamt neue Inhalte (z. B. Beiträge eines Benutzers), Inhaltsstatusänderungen (z. B. Löschen des Kommentars durch den Benutzer, &quot;Gefällt mir&quot;-Klicks) und Moderationsänderungen am Inhalt (z. B. Genehmigung eines Inhaltsstücks durch den Moderator) in eine Livefyre-App.

Die Anfrage zur Stream-API sollte ca. 30 Sekunden dauern (langes Abrufen), wobei nach 30 Sekunden ein Timeout zu erwarten ist, wenn kein neuer Inhalt einströmt.

API-Referenz: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Beispielanforderung:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Bitte beachten Sie: Die `maxEventId` in einer Stream-API-Antwort ist die höchste Ereignis-ID der Aktualisierungen in dieser Antwort. Verwenden Sie diesen Wert als Pfadparameter `lastEventId`, wenn Sie die URL Ihrer nächsten Stream-API-Anforderung erstellen, um nach allen Aktualisierungen in dieser Antwort Aktualisierungen zu erhalten.

Das unten stehende Beispiel basiert auf einer Comments-App:

Kommentar &quot;Erster Kommentar&quot; wurde zuerst gepostet. &quot;Second Comment&quot;wurde nach dem Posten veröffentlicht.

Antwort auf die erste Kommentar-Stream-API:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Das `maxEventId` in der Antwort ist &quot;1520289700953369&quot;, das als `lastEventId` verwendet wird, um den Endpunkt abzufragen, um nach allen Aktualisierungen in dieser Antwort Aktualisierungen (d.h. zweiter Kommentar) Aktualisierungen zu erhalten.

Antwort zur zweiten Kommentar-Stream-API:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Die Antwort `maxEventID` &quot;1520289700953369&quot;sollte wiederum als `lastEventID` verwendet werden, um die Stream-API-Antwort für das nächste Update zu erstellen.
