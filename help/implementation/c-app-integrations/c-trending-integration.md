---
description: Zeigen Sie die aktivsten Sammlungen auf Ihrer Site oder im Netzwerk an.
seo-description: Zeigen Sie die aktivsten Sammlungen auf Ihrer Site oder im Netzwerk an.
seo-title: Trends
solution: Experience Manager
title: Trends
uuid: 3031523d-b487-4eea-bba6-5d8f9971874f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Trends{#trending}

Zeigen Sie die aktivsten Sammlungen auf Ihrer Site oder im Netzwerk an.

Verwenden Sie Trendansicht, um die Sammlungen mit der neuesten Aktivität in Ihrer Site oder Ihrem Netzwerk zu präsentieren.

## Integration {#section_wtz_whb_c1b}

Die schnellste Möglichkeit zur Integration in Trending besteht darin, die auf Livefyre’s CDN gehostete Version zu verwenden.

Fügen Sie Ihrer Seite zunächst [Livefyre.js](https://github.com/Livefyre/Livefyre.js) hinzu.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Positionieren Sie dann das Element, in dem die App angezeigt wird.

```
<div id="trending"></div>
```

Verwenden Sie schließlich `Livefyre.require` zum Erstellen der Komponente.

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

Sie haben jetzt eine Trending App! Sehen Sie dies alles in Aktion in [diesem Beispiel](https://codepen.io/gobengo/pen/GijEy).

## Konfiguration {#section_k5k_qhb_c1b}

`network`

Das Netzwerk, aus dem Sammlungen abgerufen werden. (Erforderlich.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

Geben Sie die Site-ID ein, damit Sammlungen nur von einer einzigen Site in Ihrem Netzwerk angezeigt werden. (Optional.)

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

