---
description: Ziehen Sie Benutzerinhalte auf eine interaktive Karte.
seo-description: Ziehen Sie Benutzerinhalte auf eine interaktive Karte.
seo-title: Map
solution: Experience Manager
title: Map
uuid: 1 c 3 e 399 d-a 610-4 b 80-a 3 b 2-a 5502 b 31480 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Map{#map}

Ziehen Sie Benutzerinhalte auf eine interaktive Karte.

Mit der Map können Sie mit Geotags getaggte Inhalte auf eine Weltkarte streamen, wodurch Sie die Social Buzz um das Umbrechen von Nachrichten oder ein Live-Ereignis suchen können. Es werden alle relevanten Inhalte angezeigt, einschließlich Text, Kommentare, Fotos und Tweets.

>[!NOTE]
>
>Imagemaps werden von [© openstreetmap platziert](https://www.openstreetmap.org/copyright), was die Daten bereitstellt, die Livefyre zum Rendern der Maps verwendet.

## Integration{#section_w2m_db2_d1b}

Die schnelle Verwendung der Map ist die Verwendung der erstellten Version, die auf dem CDN von Livefyre gehostet wird.

Fügen Sie [zunächst Livefyre. js](https://github.com/Livefyre/Livefyre.js) zu Ihrer Seite hinzu.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Positionieren Sie dann das Element, in dem die Map-App angezeigt wird.

```
<div id="map" style="height: 500px;"></div>
```

Verwenden Sie zum Schluss Livefyre. müssen Sie die Map erstellen und eine Sammlung von streamhub-sdk abrufen. Denken Sie daran, dass die Zuordnung nur Inhalte mit Geotagged-Metadaten anzeigen kann. Diese Funktion unterstützt Twitter und Instagram Kurate. Um die beste Leistung sicherzustellen, fügen Sie einen Geolocation-Filter für alle Ihre Kurate-Regeln für die Sammlung ein.

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

Sehen Sie sich dieses [Live-Beispiel](https://codepen.io/cheung31/pen/wkmbF)an.

## Konfiguration {#section_jc5_gxb_c1b}

`initial`

Die erste Anzahl der aus der Sammlung zu ladenden Elemente und die Anzeige auf der Karte. Nachdem diese Zahl geladen wurde, können Benutzer auf eine Schaltfläche klicken, um mehr anzuzeigen. (Optional. Der Standardwert ist 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Optionen für die Übergabe an die zugrunde liegende [Leaflet](https://leafletjs.com/) -Map, die für die Wiedergabe verwendet wird. Verwenden Sie diese Option, um Optionen für [die Leaflet-Zuordnung](https://leafletjs.com/reference.html#map-options)festzulegen, einschließlich des anfänglichen Mittelpunkts der Map sowie der anfänglichen und maximalen Zoomstufen. (Optional.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

