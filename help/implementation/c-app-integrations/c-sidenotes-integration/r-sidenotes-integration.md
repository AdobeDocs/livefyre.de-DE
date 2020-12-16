---
description: Integrieren Sie eine SIR-App, indem Sie einen ähnlichen Prozess wie Core-Anwendungen ausführen.
seo-description: Integrieren Sie eine SIR-App, indem Sie einen ähnlichen Prozess wie Core-Anwendungen ausführen.
seo-title: Integration von Sizilien
solution: Experience Manager
title: Integration von Sizilien
uuid: 4aa14ada-402a-482d-b43e-96f37afa6c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---


# Integration von Siegels{#sidenotes-integration}

Integrieren Sie eine SIR-App, indem Sie einen ähnlichen Prozess wie Core-Anwendungen ausführen.

Wenn Ihre Core-Anwendungsintegration abgeschlossen ist, kann der Code, der zum Generieren des `collectionMeta`-Objekts geschrieben wurde, in der Regel für Siegels wiederverwendet werden.

Sie können Ihre vorhandenen `auth`-Delegaten auch wiederverwenden, indem Sie einen `auth`-Delegaten bereitstellen, der mit `fyre.conv` erstellt wurde, um im (optionalen) `authDelegate`-Feld anzugeben.

>[!NOTE]
>
>Mit Sidentifizierung können Sie `network`, `siteId` und `articleId` in ein einzelnes Objekt einschließen, anstatt sie separat in andere Teile des Konstruktors zu übergeben.

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

Wie im Abschnitt Erstellen `collectionMeta` angegeben, ist `collectionMeta` ein kodiertes JSON-Objekt. Im obigen Beispiel nimmt das JSON-Objekt das folgende Format vor, bevor es JWT-kodiert wird.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Weitere Informationen finden Sie im Token `collectionMeta`.

## Mobileinrichtung

Sidentin wurde für die Verwendung auf Mobilgeräten optimiert. Um optimale Ergebnisse mit mobilen Versionen Ihrer Livefyre-App zu erzielen, setzen Sie die Option &quot;Benutzerskalierbar&quot;auf &quot;Nein&quot;. Beispiel:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
