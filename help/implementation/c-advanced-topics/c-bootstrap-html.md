---
description: Bereitstellung von Community-Inhalten für Suchmaschinen-Crawler.
seo-description: Bereitstellung von Community-Inhalten für Suchmaschinen-Crawler.
seo-title: Bootstrap-HTML
solution: Experience Manager
title: Bootstrap-HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Bootstrap-HTML

Bereitstellung von Community-Inhalten für Suchmaschinen-Crawler.

Eine vollständige Liste der verfügbaren Endpunkte finden Sie im Abschnitt zur Livefyre- [API-Referenz](https://api.livefyre.com/docs) .

Für Livefyre-Apps muss JavaScript auf Ihrer Seite ausgeführt werden, um Inhalte für Ihre Sammlungen anzuzeigen. Da die meisten Suchmaschinen-Crawler JavaScript nicht ausführen können, können sie den Inhalt Ihrer Community nicht sehen. Verwenden Sie die Bootstrap HTML-API, um durchsuchbare Fragmente dieses Inhalts zur ersten HTTP-Antwort Ihrer Seite hinzuzufügen, sodass Ihre Inhalte und Suchbegriffe Ihre Suchmaschinenoptimierung verbessern können.

>[!NOTE]
>
>Diese API ist nur für Kommentare und Live-Blog-Sammlungstypen verfügbar.

## Integration

Die Bootstrap HTML-API von Livefyre gibt ein HTML-Fragment Ihres Benutzerinhalts zurück, das in der HTTP-Antwort der Seite enthalten sein kann. Diese Antwort kann von Suchmaschinen-Crawlern gelesen werden, ohne JavaScript auszuführen. Sobald die Seite im Browser eines Benutzers live ist, wird das HTML-Fragment durch das vollständige interaktive Widget ersetzt, und der Benutzer kann Inhalte veröffentlichen.

So implementieren Sie die Bootstrap-HTML-API:

1. Erstellen Sie eine Server-zu-Server-API-Anforderung an den Bootstrap-HTML-Endpunkt, der unten dokumentiert ist.

   >[!NOTE]
   >
   >Wenn Sie versuchen, den Bootstrap-HTML-Code für eine Konversation zu erfassen, die noch nicht existiert (d. h., wenn Sie die App noch nicht einbetten oder die Sammlung erstellen müssen), erhalten Sie einen 200-Wert, der jedoch Folgendes enthält: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Wenn Ihre Rückkehr keine Inhalte mit der Zeichenfolge "404"enthält, speichern Sie sie in einer Zeichenfolge. Sie können diese Antwort für eine spätere Verwendung zwischenspeichern, um zu vermeiden, dass die Bootstrap HTML-API bei jeder Seitenladung angefordert wird.
1. Fügen Sie die Bootstrap-HTML-Zeichenfolge in Ihre Webseite ein, auf der der Inhalt erscheinen soll.
1. Geben Sie Ihre Webseite an den Browser (oder Suchmaschinen-Crawler) weiter.

## Ressource

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parameter

* **networkName** Ihr Livefyre-Netzwerkname angegeben. Beispiel: *Laboratorien* in `labs.fyre.co`.
* **siteId** Die Site-ID der Sammlung.
* **b64articleId** Die Artikel-ID der Sammlung mit der base64url-Kodierung.

## Beispiel 

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Antwort

```
https://gist.github.com/ec5c2457322faf9cf515 
```
