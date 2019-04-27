---
description: Integrieren Sie eine App für ein Blog-App, indem Sie einen ähnlichen Prozess wie Core Applications befolgen.
seo-description: Integrieren Sie eine App für ein Blog-App, indem Sie einen ähnlichen Prozess wie Core Applications befolgen.
seo-title: Integration von Sidenotes
solution: Experience Manager
title: Integration von Sidenotes
uuid: 4 aa 14 ada -402 a -482 d-b 43 e -96 f 37 afa 6 c 53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Integration von Sidenotes{#sidenotes-integration}

Integrieren Sie eine App für ein Blog-App, indem Sie einen ähnlichen Prozess wie Core Applications befolgen.

Allgemein gilt: Wenn die Core-Anwendungsintegration abgeschlossen ist, kann der Code, der zur Generierung des `collectionMeta` Objekts geschrieben wurde, für die Zielgruppe wiederverwendet werden.

Sie können Ihre vorhandenen `auth` Delegierten auch wiederverwenden, indem Sie einen `auth` mit `fyre.conv` den Autoren erstellten Delegieren im (optional) `authDelegate` Feld bereitstellen.

>[!NOTE]
>
>Mithilfe von Sidenotes können Sie ein `network`einzelnes Objekt einbeziehen, `siteId`und `articleId` nicht in anderen Teilen des Konstruktors weiterleiten.

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

Wie im Abschnitt &quot;Erstellen `collectionMeta` « `collectionMeta` angegeben, ist ein kodiertes JSON-Objekt. Im obigen Beispiel akzeptiert das JSON-Objekt das folgende Format, bevor es JWT-kodiert ist.

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

Weitere Informationen finden Sie im `collectionMeta` Token.

## Mobilgerät einrichten

Die Zielgruppen wurden für die Verwendung auf Mobilgeräten optimiert. Die besten Ergebnisse bei mobilen Versionen Ihrer Livefyre-App erzielen Sie, wenn Sie die Option für benutzerskalierbare Anwendungen auf Nein setzen. Beispiel:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
