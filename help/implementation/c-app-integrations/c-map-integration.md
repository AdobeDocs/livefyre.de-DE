---
description: Plotten Sie Benutzerinhalte zu einer interaktiven Map.
seo-description: Plotten Sie Benutzerinhalte zu einer interaktiven Map.
seo-title: Landkarte
solution: Experience Manager
title: Landkarte
uuid: 1c3e399d-a610-4b80-a3b2-a5502b31480d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 2%

---


# Landkarte{#map}

Plotten Sie Benutzerinhalte zu einer interaktiven Map.

Mit der Karte können Sie geotaggte Inhalte auf eine Weltkarte übertragen, sodass Sie das Social Buzz rund um aktuelle Nachrichten oder ein Live-Ereignis finden können. Alle relevanten Inhalte werden angezeigt, einschließlich Text, Kommentaren, Fotos und Tweets.

>[!NOTE]
>
>Karten werden mit [© OpenStreetMap](https://www.openstreetmap.org/copyright) betrieben, das die Daten bereitstellt, die Livefyre zum Rendern seiner Maps verwendet.

## Integration {#section_w2m_db2_d1b}

Die schnellste Möglichkeit, Map zu verwenden, ist die auf Livefyres CDN gehostete Version zu verwenden.

Fügen Sie zunächst [Livefyre.js](https://github.com/Livefyre/Livefyre.js) zu Ihrer Seite hinzu.

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

Positionieren Sie dann das Element, in dem die Map-App angezeigt wird.

```
<div id="map" style="height: 500px;"></div>
```

Schließlich verwenden Sie Livefyre.require, um die Map zu erstellen und eine Sammlung zu entnehmen, die von streamub-sdk eingeleitet wird. Beachten Sie, dass Map nur Inhalte mit geotageten Metadaten anzeigen kann. Diese Funktion wird von Twitter und Instagram Curate unterstützt. Um eine optimale Leistung zu gewährleisten, fügen Sie in allen Kuratierungsregeln für die Sammlung einen Geolocation-Filter ein.

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

Sehen Sie sich dieses [Live-Beispiel](https://codepen.io/cheung31/pen/wkmbF) an.

## Konfiguration {#section_jc5_gxb_c1b}

`initial`

Die anfängliche Anzahl der Elemente, die aus der Sammlung geladen und auf der Map angezeigt werden sollen. Nach dem Laden dieser Nummer können Benutzer auf eine Schaltfläche klicken, um weitere anzuzeigen. (Optional. Der Standardwert ist 50.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

Optionen, die an die zugrunde liegende [Gebrauchsinformation](https://leafletjs.com/)-Map weitergegeben werden, welche Map zum Rendern verwendet. Verwenden Sie diese Option, um [Optionen für die Imagemap](https://leafletjs.com/reference.html#map-options) festzulegen, einschließlich des anfänglichen Zentrums der Map sowie der Anfangs- und Maximalzoomwerte. (Optional.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

