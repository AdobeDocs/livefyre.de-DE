---
description: Beim Einbetten der Kommentarapp wird der Vorgang zum Einbetten einer Core-App ausgeführt.
seo-description: Beim Einbetten der Kommentarapp wird der Vorgang zum Einbetten einer Core-App ausgeführt.
seo-title: Kommentarapp einbetten
solution: Experience Manager
title: Kommentarapp einbetten
uuid: e 4982 ad 3-cab 1-4805-a 55 c -594 cca 3 b 7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e

---


# Kommentarapp einbetten{#embed-a-comments-app}

Beim Einbetten der Kommentarapp wird der Vorgang zum Einbetten einer Core-App ausgeführt.

Einbetten der Kommentarapp folgt dem Einbetten einer Core-App, die unter &quot;App [einbetten&quot; beschrieben wird.](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

## Beispiel 

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Wie im Abschnitt &quot;Erstellen von collectionmeta&quot; vermerkt, ist collectionmeta ein kodiertes JSON-Objekt. Im obigen Beispiel akzeptiert das JSON-Objekt das folgende Format, bevor es JWT-kodiert ist:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

