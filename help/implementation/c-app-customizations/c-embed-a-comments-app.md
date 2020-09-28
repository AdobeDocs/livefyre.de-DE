---
description: Das Einbetten der Kommentaranwendung erfolgt nach dem Einbetten einer Core-App.
seo-description: Das Einbetten der Kommentaranwendung erfolgt nach dem Einbetten einer Core-App.
seo-title: Kommentaranwendung einbetten
solution: Experience Manager
title: Kommentaranwendung einbetten
uuid: e4982ad3-cab1-4805-a55c-594cca3b7203
translation-type: tm+mt
source-git-commit: 268dc91369d346a254b7120706264eb91da8257e

---


# Kommentaranwendung einbetten{#embed-a-comments-app}

Das Einbetten der Kommentaranwendung erfolgt nach dem Einbetten einer Core-App.

Das Einbetten der Kommentaranwendung erfolgt nach dem Einbetten einer Core-App, wie unter [Einbetten einer App beschrieben.](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

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

Wie im Abschnitt zum Erstellen von CollectionMeta angegeben, ist CollectionMeta ein kodiertes JSON-Objekt. Im obigen Beispiel nimmt das JSON-Objekt das folgende Format vor, bevor es JWT-kodiert wird:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

