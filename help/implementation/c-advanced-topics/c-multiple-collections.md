---
description: Präsentieren mehrerer Sammlungen auf einer einzelnen Seite.
seo-description: Präsentieren mehrerer Sammlungen auf einer einzelnen Seite.
seo-title: Mehrere Sammlungen
solution: Experience Manager
title: Mehrere Sammlungen
uuid: 9675 ffd 7-1 a 59-42 a 1-b 3 ba -40 af 1744 cfd 1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Mehrere Sammlungen {#multiple-collections}

Präsentieren mehrerer Sammlungen auf einer einzelnen Seite.

Sie können mehrere Sammlungen auf einer einzelnen Seite Ihrer Site einfügen. Um ein Ereignis zu veröffentlichen, können Sie beispielsweise während des Ereignisses ein Live-Blog oder eine Chat-Diskussion mit einer separaten App auf der Seite einrichten, die verwandte kuratierte Inhalte aus dem Social Web anzeigt. Sie können auch eine Kommentarapp unter einem Artikel mit einem Chat nach rechts einfügen.

Um mehrere Unterhaltungen auf einer Seite zu erhalten, fügen Sie eine oder mehrere Konfigurationen in einem Array hinzu und übergeben Sie das Array an den Ladenaufruf. Beispiel:

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
