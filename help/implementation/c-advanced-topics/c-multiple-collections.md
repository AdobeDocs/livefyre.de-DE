---
description: Zeigen Sie mehrere Sammlungen auf einer Seite an.
seo-description: Zeigen Sie mehrere Sammlungen auf einer Seite an.
seo-title: Mehrere Sammlungen
solution: Experience Manager
title: Mehrere Sammlungen
uuid: 9675ffd7-1a59-42a1-b3ba-40af1744cfd1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Mehrere Sammlungen {#multiple-collections}

Zeigen Sie mehrere Sammlungen auf einer Seite an.

Sie können mehrere Sammlungen auf einer einzelnen Seite Ihrer Site hinzufügen. Um beispielsweise ein Ereignis zu veröffentlichen, haben Sie während der Veranstaltung möglicherweise eine Live-Blog- oder Chat-Diskussion mit einer separaten App auf der Seite, die zugehörige kuratierte Inhalte aus dem gesamten Social Web anzeigt. Sie können auch eine Kommentar-App unterhalb eines Artikels mit einem Chat an der Seite einfügen.

Um mehrere Konversationen auf einer Seite abzurufen, fügen Sie eine oder mehrere Konfigurationen in einem Array hinzu und übergeben Sie das Array an den Ladeaufruf. Beispiel.

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
