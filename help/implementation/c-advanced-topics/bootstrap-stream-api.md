---
description: Verwenden Sie Bootstrap- und Stream-API mit Livefyre-Apps.
seo-description: Verwenden Sie Bootstrap- und Stream-API mit Livefyre-Apps.
seo-title: Bootstrap- und Stream-API mit Livefyre-Apps verwenden
solution: Experience Manager
title: Ansicht der Kontodetails
uuid: bace558f-ade8-49d6-abda-9ee754ce4ac0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# Bootstrap- und Stream-API mit Livefyre-Apps verwenden {#bootstrap-stream-api}

## Bootstrap-API {#bootstrap-api}

### Wie kann ich Inhalte abrufen, die älter als die neuesten 50 Stücke sind? {#howcontentolder}

Bootstrap enthält alle Inhalte in einer Livefyre-App. Es handelt sich um die zwischengespeicherten Daten, in der Regel 12-20 Minuten alt. Es wird in Blöcken von 50 Stück geliefert und paginiert, damit Sie Inhalte abrufen können, die älter als 50 Stück sind.

[API-Referenz](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Beispielanforderung](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

Die obige Beispielanforderung lädt die `init` Seite, die Sammlungseinstellungen und den einzigen anfänglichen Satz von etwa 50 Teilen des neuesten Inhalts enthält. Um ältere Inhalte abzurufen, müssen Sie nachfolgende Bootstrap-Seiten mit der Seitenzahl laden `N` :

Anfrage: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Eine Beispielanwendung enthält beispielsweise 120 Inhaltselemente. Content "1" ist das älteste Inhaltselement und Content "70" ist das neueste Inhaltselement.

* `Init` werden ca. 120-70 Inhaltselemente in absteigender Reihenfolge geladen: [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` werden ~ 1-50 Inhaltselemente in aufsteigender Reihenfolge geladen: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` werden ca. 51-100 Inhaltselemente in aufsteigender Reihenfolge geladen: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` werden Inhalte von ca. 101-120 Stück in aufsteigender Reihenfolge geladen:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Klicken Sie hier, um das Bootstrap-Umfrage-Flussdiagramm anzuzeigen.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## Stream-API {#stream-api}

Was ist die Stream-API?
Stream ist eine lange Umfrage, die planmäßig für ca. 30 Sekunden offen bleiben soll. Beschreibung zur Methode des langen Abrufs finden Sie hier: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Dieser lange Abruf-Endpunkt streamt neue Inhalte (z. B. Beiträge eines Benutzers), Inhaltsstatusänderungen (z. B. Löschen des Kommentars durch den Benutzer, "Gefällt mir"-Klicks) und Moderationsänderungen am Inhalt (z. B. Genehmigung eines Inhaltsstücks durch den Moderator) in eine Livefyre-App.

Die Anfrage zur Stream-API sollte ca. 30 Sekunden dauern (langes Abrufen), wobei nach 30 Sekunden ein Timeout zu erwarten ist, wenn kein neuer Inhalt einströmt.

API-Referenz: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Beispielanforderung:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Bitte beachten Sie: Die Antwort `maxEventId` in einer Stream-API ist die höchste Ereignis-ID der Aktualisierungen in dieser Antwort. Verwenden Sie diesen Wert als `lastEventId` Pfadparameter, wenn Sie die URL Ihrer nächsten Stream-API-Anforderung erstellen, um nach allen Aktualisierungen in dieser Antwort Aktualisierungen zu erhalten.

Das unten stehende Beispiel basiert auf einer Comments-App:

Kommentar "Erster Kommentar" wurde zuerst gepostet. "Second Comment"wurde nach dem Posten veröffentlicht.

Antwort auf die erste Kommentar-Stream-API:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Die Antwort `maxEventId` `lastEventId` in der Antwort lautet "1520289700953369", die verwendet wird, um den Endpunkt abzufragen, um nach allen Aktualisierungen in dieser Antwort Aktualisierungen (d. h. zweiter Kommentar) Aktualisierungen zu erhalten.

Antwort zur zweiten Kommentar-Stream-API:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Die `maxEventID` Antwort "1520289700953369"sollte wiederum als Grundlage für die `lastEventID` Erstellung der Stream-API-Antwort für das nächste Update verwendet werden.