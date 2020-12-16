---
description: Erfahren Sie, wie Sie die benutzergenerierten Inhalte überwachen und speichern, die über das Livefyre-System fließen.
seo-description: Erfahren Sie, wie Sie die benutzergenerierten Inhalte überwachen und speichern, die über das Livefyre-System fließen.
seo-title: Aktivitäten-Stream
solution: Experience Manager
title: Aktivitäten-Stream
uuid: f40deec1-58ab-41c9-aac4-d2d8c9192bb9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---


# Aktivität-Stream {#activity-stream}

Erfahren Sie, wie Sie die benutzergenerierten Inhalte überwachen und speichern, die über das Livefyre-System fließen.

Verwenden Sie die Aktivität Stream API, um vom Benutzer erstellte Daten zu nutzen, die über das Livefyre-System in Ihrem Netzwerk oder Ihrer Site fließen. Beispiel: Verwenden Sie Daten aus dieser API, um Ihre Suchindizes auf Grundlage von Bewertungen zu aktualisieren oder um Benutzerabzeichen in einem Drittanbietersystem auf Grundlage ihrer Aktivität zu verwalten.

Aktivität Stream-API:

Eine vollständige Liste der verfügbaren Endpunkte finden Sie im Abschnitt zur Livefyre-API-Referenz.

## Ressourcen {#section_aql_n4l_b1b}

Es gibt zwei Endpunkte: einen für die Staging-Umgebung und einen für die Produktion.

### Staging

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Produktion

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### Parameter

* **resource:** ** stringEin URN des Objekts, für das Sie Aktivitäten anfordern.

* **since:** ** integerEine 64-Bit-Ganzzahl, welche die ID des letzten Ereignisses darstellt, das Sie erhalten haben. Geben Sie &quot;0&quot;an, wenn Sie keine vorherigen Daten haben.

## URN Strings {#section_skl_q4l_b1b}

Beispiele:

* **urn:livefyre:** `example.fyre.co` Der Stream für die Aktivität  `example.fyre.co`.
* **urn:livefyre:** `example.fyre.co:site=54321` Der Stream der Aktivität für Site 54321 unter dem  `example.fyre.co` Netzwerk.

## Token-Richtlinien {#section_nwh_c5j_11b}

Die Aktivitäten-Stream-API verwendet ein OAuth-Träger-Token zur Authentifizierung. Träger-Token sind Teil der OAuth 2.0-Spezifikation und werden hier offiziell [hier](https://tools.ietf.org/html/rfc6750#section-1.2) beschrieben.

Ein Token enthält mehrere Elemente:

* Wer hat das Token erstellt.
* Wem wurde ein Token gegeben.
* Ein Zeitpunkt, zu dem er nicht mehr gültig ist.
* Das, woran wir arbeiten.
* Eine Liste der erteilten Berechtigungen.

### Schritte

Die Schritte zum Erstellen eines OAuth-Platzhalter-Tokens umfassen Folgendes:

* Erstellen Sie eine Landkarte/ein Wörterbuch, die den Aussteller, die Audience, den Betreff, den Ablauf und den Umfang enthält.
* Verwenden Sie die JWT-Bibliothek mit Ihrem geheimen Schlüssel, um ein JWT-Token zu kodieren.
* hinzufügen &quot;Authentifizierung: Bearer&quot; auf Ihre HTTP-Anforderung.

Das folgende Codebeispiel veranschaulicht die oben genannten Schritte in Python:

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

Wenn die Inhabertoken-Schlüssel wie folgt definiert werden:

* **is** *(Issuer)*  Eine Entität, die berechtigt ist, Token zu generieren. Dies kann Livefyre, eine Site oder ein Netzwerk sein. (Damit eine Nachricht zu spät in die Schule kommt, ist sie Ihr Elternteil.)
* **aud** *(Audience)*  Die Person, für die dieses Token generiert wurde. Wenn Sie das Token selbst erstellen, ist es die Website oder das Netzwerk.
* **sub** *(Subject)*  Der Gegenstand, für den Berechtigungen erteilt werden sollen. Wenn Sie beispielsweise eine Sammlung bearbeiten, muss der Betreff die ID für die Sammlung sein. (In der Beschreibung aus dem Schulbeispiel sind Sie es.)
* **exp** *(Expiration)* Ein Zeitpunkt, zu dem das Token nicht mehr gültig ist.
* **scope** *(Scope)* Dies ist eine Liste der zu dem Thema erteilten Genehmigungen. &quot;Spät für die Schule&quot; ist ein Beispiel. Der Name einer API ist ein weiteres Beispiel.

## Beispiel {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## Antwort {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

Eine Antwort mit neuen Daten seit der letzten Anforderung:

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## Hinweise {#section_hj3_crj_11b}

* Bei einem erfolgreichen Aufruf der API wird ein HTTP 200-Statuscode zurückgegeben. Alle anderen Statuscodes sollten als Fehler betrachtet werden.
* Wenn nicht null, verwenden Sie den Wert von `data.meta.cursor.next` als `since`-Parameter Ihrer nächsten Anforderung.
* Wenn der Wert von `data.meta.cursor.next` null ist, bedeutet dies, dass keine neuen Daten zu verwenden sind. Sie sollten später mit demselben `since`-Wert erneut anfordern, um zu sehen, ob neue Daten vorliegen.
* In der Praxis sollten Sie sofort weitere Daten anfordern, wenn der Wert `data.meta.cursor.next` nicht null ist.
* Über diese API stehen in der Produktion Daten im Wert von rund zwei Stunden zur Verfügung.
* Sie sollten Ihre Prozesse so einrichten, dass dieser Endpunkt häufig am Cronjob abgefragt wird, um fehlende Daten zu vermeiden. Ein Intervall von fünf Minuten sollte für die meisten Implementierungen vollkommen ausreichend sein.
