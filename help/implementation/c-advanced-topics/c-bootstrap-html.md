---
description: Stellen Sie Community-Inhalte für Suchmaschinen-Crawler zur Verfügung.
seo-description: Stellen Sie Community-Inhalte für Suchmaschinen-Crawler zur Verfügung.
seo-title: Bootstrap-HTML
solution: Experience Manager
title: Bootstrap-HTML
uuid: 137 e 4382-4 e 7 b -4124-9 d 35-1 d 872 a 497 bc 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Bootstrap-HTML

Stellen Sie Community-Inhalte für Suchmaschinen-Crawler zur Verfügung.

Eine vollständige Liste der verfügbaren Endpunkte finden Sie im Abschnitt &quot;Livefyre [-API-Referenz](https://api.livefyre.com/docs) &quot; .

Livefyre-Apps erfordern, dass Sie javascript auf Ihrer Seite ausführen, um Inhalte für Ihre Sammlungen anzuzeigen. Da die meisten Suchmaschinen-Crawler javascript nicht ausführen können, können sie den Inhalt Ihrer Community-Beiträge nicht sehen. Verwenden Sie die Bootstrap HTML API, um durchsuchbare Fragmente dieses Inhalts zur ursprünglichen HTTP-Antwort Ihrer Seite hinzuzufügen, wodurch Ihre Inhalte und Suchbegriffe Ihre Suchmaschinenoptimierung verbessern können.

>[!NOTE]
>
>Diese API ist nur für die Typen &quot;Kommentare&quot; und&quot; Live Blog&quot; verfügbar.

## Integration

Die Bootstrap-HTML-API von Livefyre gibt ein HTML-Fragment Ihres Benutzerinhalts zurück, das möglicherweise in die HTTP-Antwort der Seite aufgenommen wird. Diese Antwort kann von Suchmaschinen-Crawlern gelesen werden, ohne javascript auszuführen. Sobald die Seite im Browser eines Benutzers live ist, wird das HTML-Fragment durch das vollständige interaktive Widget ersetzt und der Benutzer kann Inhalte veröffentlichen.

Implementieren der Bootstrap-HTML-API:

1. Erstellen Sie einen Server zur Server-API-Anfrage an den Bootstrap-HTML-Endpunkt, der unten dokumentiert ist.

   >[!NOTE]
   >
   >Wenn Sie versuchen, das Bootstrap-HTML für eine Unterhaltung zu erfassen, die noch nicht vorhanden ist (d. h. wenn Sie die App noch nicht einbetten oder die Sammlung erstellen), erhalten Sie eine 200-Prozendure, aber mit Inhalt, der etwas ähnelt: `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. Wenn Ihre Rendite keine Inhalte mit &quot;404&quot; enthält, speichern Sie sie in einer Zeichenfolge. Sie können diese Antwort für später zwischenspeichern, um zu verhindern, dass die Bootstrap-HTML-API auf jeder Pageloanzeige angefordert wird.
1. Fügen Sie die Bootstrap-HTML-Zeichenfolge in Ihre Webseite ein, auf der der Inhalt angezeigt werden soll.
1. Stellen Sie Ihre Webseite dem Browser (oder dem Suchmaschinen-Crawler) bereit.

## Ressource

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## Parameter

* **Networkname** Ihr Livefyre-bereitgestellter Netzwerkname. Beispiel: *in*`labs.fyre.co`.
* **Siteid** Die Site-ID der Sammlung.
* **b 64 articleid** Die Artikel-ID der Sammlung mit der Base 64-URL-Kodierung.

## Beispiel 

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## Antwort

```
https://gist.github.com/ec5c2457322faf9cf515 
```
