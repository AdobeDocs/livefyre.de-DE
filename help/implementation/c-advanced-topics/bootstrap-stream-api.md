---
description: Verwenden Sie Bootstrap und Stream-API mit Livefyre-Apps.
seo-description: Verwenden Sie Bootstrap und Stream-API mit Livefyre-Apps.
seo-title: Bootstrap und Stream-API mit Livefyre-Apps verwenden
solution: Experience Manager
title: Ansicht von Kontodetails
uuid: bace 558 f-ade 8-49 d 6-abda -9 ee 754 ce 4 ac 0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# Bootstrap und Stream-API mit Livefyre-Apps verwenden {#bootstrap-stream-api}

## Bootstrap-API {#bootstrap-api}

### Wie kann ich Inhalte, die älter als die neuesten 50 sind, abrufen? {#howcontentolder}

Bootstrap ist der gesamte Inhalt einer Livefyre-App. Es sind die zwischengespeicherten Daten, normalerweise 12–20 Minuten alt. Es wird in 50 Bereichen bereitgestellt und paginiert, damit Sie Inhalte mit älter als 50 Elementen abrufen können.

[API-Referenz](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Beispielanforderung](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

Die obige Beispielanforderung lädt die `init` Seite, die Sammlungseinstellungen enthält, und den einzigen anfänglichen Satz von ~ 50 neuem Inhalt. Um ältere Inhalte abzurufen, müssen Sie folgende Bootstrap-Seiten mit `N` der Seitenzahl laden:

Anforderung: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Beispiel: Eine Beispiel-App hat 120 Inhaltselemente. Inhalt "1" ist der älteste Inhalt und der Inhalt" 70" ist das neueste Inhaltselement.

* `Init` lädt ~ 120 bis 70 Inhaltselemente in absteigender Reihenfolge: [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` ~ 1-50 Inhaltselemente in aufsteigender Reihenfolge laden: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` lädt ~ 51 bis 100 Inhaltselemente in aufsteigender Reihenfolge: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` lädt ~ 101 bis 120 Inhaltselemente in aufsteigender Reihenfolge:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Klicken Sie hier, um das Bootstrap-Abstimmungs-Ablaufdiagramm anzuzeigen.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## Stream-API {#stream-api}

Was ist Stream-API?
Stream ist eine lange Umfrage, die nach Design für ungefähr 30 Sekunden geöffnet bleiben soll. Beschreibung der Langfachabstimmung finden Sie hier: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Dieser Endpunkt für den langen Abruf streamt neue Inhalte (z. B. ein Benutzer postet einen Kommentar), Statusstatusänderungen (z. B. Benutzer löscht ihren Kommentar, ihre Vorlieben) und Moderationsänderungen an Inhalten (z. B. durch Moderatoren genehmigt ein Inhaltselement) einer Livefyre-App.

Die Anfrage an die Stream-API sollte etwa 30 Sekunden (lange Abfrage) mit erwarteten Timeouts nach 30 Sekunden betragen, wenn keine neuen Inhaltsstreams in eingehen.

API-Referenz: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Beispielanforderung:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Bitte beachten: Bei `maxEventId` einer Stream-API-Antwort handelt es sich um die höchste Ereignis-ID der Aktualisierungen in dieser Antwort. Verwenden Sie diesen Wert als `lastEventId` Pfadparameter, wenn Sie die URL Ihrer nächsten Stream-API-Anfrage erstellen, um Updates nach allen Aktualisierungen in dieser Antwort zu erhalten.

Das folgende Beispiel basiert auf einer Kommentarapp:

Kommentar "Erster Kommentar" wurde zuerst veröffentlicht. " Zweiter Kommentar" wurde danach veröffentlicht.

First Comment Stream API response:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

In `maxEventId` der Antwort ist "1520289700953369" angegeben, die zum `lastEventId` Abrufen des Endpunktes verwendet wird, um Aktualisierungen abzurufen (d. h. Zweiter Kommentar), der nach allen Aktualisierungen in dieser Antwort auftrat.

Zweite Kommentarstream-API-Antwort:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Die `maxEventID` "1520289700953369" in der Antwort sollte wiederum als die `lastEventID` Stream-API-Antwort für das nächste Update verwendet werden.