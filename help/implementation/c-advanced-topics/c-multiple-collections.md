---
description: Zeigen Sie mehrere Sammlungen auf einer Seite an.
title: Mehrere Sammlungen
exl-id: 748b6ca6-635e-4bae-9b95-cfbd4651751f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 1%

---

# Mehrere Sammlungen {#multiple-collections}

Zeigen Sie mehrere Sammlungen auf einer Seite an.

Sie können mehrere Sammlungen auf einer einzelnen Seite Ihrer Site hinzufügen. Um beispielsweise ein Ereignis zu veröffentlichen, können Sie während des Ereignisses eine Live-Blog- oder Chat-Diskussion mit einer separaten App auf Ihrer Seite führen, in der zugehörige kuratierte Inhalte aus dem gesamten Social Web angezeigt werden. Sie können auch eine Kommentar-App unterhalb eines Artikels mit einem Chat an der Seite einfügen.

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
