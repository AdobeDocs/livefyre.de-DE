---
description: Verwenden Sie die Bootstrap- und Stream-API mit Livefyre-Apps.
title: Anzeigen von Kontodetails
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Verwenden der Bootstrap- und Stream-API mit Livefyre-Apps {#bootstrap-stream-api}

## Bootstrap-API {#bootstrap-api}

### Wie kann ich Inhalte abrufen, die älter als die neuesten 50 Teile sind? {#howcontentolder}

Bootstrap ist der gesamte Inhalt einer Livefyre-App. Hierbei handelt es sich um die zwischengespeicherten Daten, in der Regel 12 bis 20 Minuten alt. Es wird in Blöcken von 50 Stück bereitgestellt und paginiert, sodass Sie Inhalte abrufen können, die älter als 50 Stück sind.

[API-Referenz](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Beispielanfrage](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

Die obige Beispielanfrage lädt die `init`-Seite, die Sammlungseinstellungen und den einzigen anfänglichen Satz von ca. 50 Elementen des neuesten Inhalts enthält. Um ältere Inhalte abzurufen, müssen Sie nachfolgende Bootstrap-Seiten laden, wobei `N` die Seitennummer ist:

Anfrage: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Beispiel: Eine Beispielanwendung enthält 120 Inhaltselemente. Inhalt &quot;1&quot;ist das älteste Inhaltselement und Inhalt &quot;70&quot;ist das neueste Inhaltselement.

* `Init` lädt ca. 120-70 Inhaltselemente in absteigender Reihenfolge:  [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` lädt ~ 1-50 Inhaltselemente in aufsteigender Reihenfolge:  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json`
* `1.json` wird ~ 51-100 Inhaltselemente in aufsteigender Reihenfolge laden:  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json`
* `2.json` lädt ca. 101-120 Inhaltselemente in aufsteigender Reihenfolge:`https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json`

[Klicken Sie hier , um das Diagramm zum Bootstrap-Umfrage-Fluss anzuzeigen.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## Stream-API {#stream-api}

Was ist die Stream-API?
Stream ist eine lange Umfrage, die standardmäßig für ca. 30 Sekunden offen bleiben soll. Eine Beschreibung der langgezogenen Technik finden Sie hier: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Dieser lange Abruf-Endpunkt streamt neue Inhalte (z. B. ein Benutzer veröffentlicht einen Kommentar), Inhaltsstatus-Änderungen (z. B. Löschen des Kommentars durch den Benutzer, &quot;Gefällt mir&quot;-Klicks) und Moderationsänderungen an Inhalten (z. B. Genehmigung eines Inhalts durch Moderator) in eine Livefyre-App.

Die Anfrage an die Stream-API sollte ca. 30 Sekunden (lange Abruf) mit einem erwarteten Timeout nach 30 Sekunden betragen, wenn kein neuer Inhalt gestreamt wird.

API-Referenz: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Beispielanfrage:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Bitte beachten Sie: Die `maxEventId` in einer Stream-API-Antwort ist die höchste Ereignis-ID der Aktualisierungen in dieser Antwort. Verwenden Sie diesen Wert als Pfadparameter `lastEventId` beim Erstellen der URL Ihrer nächsten Stream-API-Anfrage, um nach allen Aktualisierungen in dieser Antwort Aktualisierungen Aktualisierungen zu erhalten.

Das folgende Beispiel basiert auf einer Kommentar-App:

Kommentar &quot;Erster Kommentar&quot;wurde zuerst veröffentlicht. &quot;Zweiter Kommentar&quot;wurde veröffentlicht.

Erste Kommentar-Stream-API-Antwort:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Der `maxEventId` in der Antwort ist &quot;1520289700953369&quot;, der als `lastEventId` verwendet wird, um den Endpunkt abzufragen und Updates (d. h. den zweiten Kommentar) zu erhalten, die nach allen Aktualisierungen in dieser Antwort auftreten.

Zweite Kommentar-Stream-API-Antwort:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Die `maxEventID` &quot;1520289700953369&quot;in der Antwort sollte wiederum als `lastEventID` verwendet werden, um die Stream-API-Antwort für das nächste Update zu erstellen.
