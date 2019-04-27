---
description: Präsentieren Sie die aktivsten Sammlungen auf Ihrer Site oder Ihrem Netzwerk.
seo-description: Präsentieren Sie die aktivsten Sammlungen auf Ihrer Site oder Ihrem Netzwerk.
seo-title: Trends
solution: Experience Manager
title: Trends
uuid: 3031523 d-b 487-4 eea-bba 6-5 d 8 f 9971874 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Trends{#trending}

Präsentieren Sie die aktivsten Sammlungen auf Ihrer Site oder Ihrem Netzwerk.

Verwenden Sie Trend, um die Sammlungen mit der neuesten Aktivität in Ihrer Site oder Ihrem Netzwerk anzuzeigen.

## Integration{#section_wtz_whb_c1b}

Die schnelle Integration mit der Trendansicht ist die Verwendung der erstellten Version, die auf dem CDN von Livefyre gehostet wird.

Fügen Sie [zunächst Livefyre. js](https://github.com/Livefyre/Livefyre.js) zu Ihrer Seite hinzu.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Positionieren Sie dann das Element, in dem die App angezeigt wird.

```
<div id="trending"></div>
```

Zum Erstellen `Livefyre.require` der Komponente verwenden.

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

Sie haben jetzt eine Trendapp! Sehen Sie sich dies in diesem [Beispiel alles](https://codepen.io/gobengo/pen/GijEy)an.

## Konfiguration {#section_k5k_qhb_c1b}

`network`

Das Netzwerk, aus dem Sammlungen gezogen werden. (Erforderlich.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Geben Sie die Site-ID an, um Sammlungen nur von einer einzelnen Site innerhalb Ihres Netzwerks anzuzeigen. (Optional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

Geben Sie ein einzelnes Collection-Tag an, um nur Sammlungen mit diesem Tag anzuzeigen. (Optional.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

