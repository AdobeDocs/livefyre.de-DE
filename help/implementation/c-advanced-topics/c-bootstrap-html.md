---
description: Bereitstellung von Community-Inhalten für Suchmaschinen-Crawler.
seo-description: Bereitstellung von Community-Inhalten für Suchmaschinen-Crawler.
seo-title: Bootstrap-HTML
solution: Experience Manager
title: Bootstrap-HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 1%

---


# Bootstrap-HTML

Bereitstellung von Community-Inhalten für Suchmaschinen-Crawler.

Eine vollständige Liste der verfügbaren Endpunkte finden Sie im Abschnitt Livefyre [API-Referenz](https://api.livefyre.com/docs).

Für Livefyre-Apps muss JavaScript auf Ihrer Seite ausgeführt werden, um Inhalte für Ihre Sammlungen anzuzeigen. Da die meisten Suchmaschinen-Crawler JavaScript nicht ausführen können, können sie den Inhalt Ihrer Community nicht sehen. Verwenden Sie die Bootstrap-HTML-API, um durchsuchbare Fragmente dieses Inhalts zur ersten HTTP-Antwort Ihrer Seite hinzuzufügen, sodass Ihre Inhalte und Suchbegriffe Ihre Suchmaschinenoptimierung verbessern können.

>[!NOTE]
>
>Diese API ist nur für Kommentare und Live-Blog-Sammlungstypen verfügbar.

## Integration

Livefyres Bootstrap-HTML-API gibt ein HTML-Fragment Ihres Benutzerinhalts zurück, das in der HTTP-Antwort der Seite enthalten sein kann. Diese Antwort kann von Suchmaschinen-Crawlern gelesen werden, ohne JavaScript auszuführen. Sobald die Seite im Browser eines Benutzers live ist, wird das HTML-Fragment durch das vollständige interaktive Widget ersetzt, und der Benutzer kann Inhalte veröffentlichen.

So implementieren Sie die Bootstrap-HTML-API:

1. Erstellen Sie eine Server-zu-Server-API-Anforderung an den unten dokumentierten HTML-Endpunkt des Bootstrap.

   >[!NOTE]
   >
   >Wenn Sie versuchen, den Bootstrap-HTML-Code für eine Konversation zu erfassen, die noch nicht vorhanden ist (d. h. wenn Sie die App noch nicht einbetten oder die Sammlung erstellen müssen), erhalten Sie einen 200-Wert, der jedoch wie folgt aussieht: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Wenn Ihre Rückkehr keine Inhalte mit der Zeichenfolge &quot;404&quot;enthält, speichern Sie sie in einer Zeichenfolge. Sie können diese Antwort für eine spätere Verwendung zwischenspeichern, um zu vermeiden, dass die HTML-API des Bootstrap auf jeder Seite angefordert wird.
1. Fügen Sie die HTML-Zeichenfolge des Bootstrap in Ihre Webseite ein, auf der der Inhalt angezeigt werden soll.
1. Geben Sie Ihre Webseite an den Browser (oder Suchmaschinen-Crawler) weiter.

## Ressource

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parameter

* **Netzwerkname** Ihre Livefyre-Netzwerkname angegeben. Beispiel: *labs* in `labs.fyre.co`.
* **** siteIdDie Site-ID der Sammlung.
* **b64** articleIdDie Artikel-ID der Sammlung mit der base64url-Kodierung.

## Beispiel 

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Antwort

```
https://gist.github.com/ec5c2457322faf9cf515 
```
