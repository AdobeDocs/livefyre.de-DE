---
description: Das Einbetten der Kommentaranwendung erfolgt nach dem Einbetten einer Core-App.
title: Kommentaranwendung einbetten
exl-id: 5eb191f8-ee52-4a9d-9180-90457a49fd4e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# Kommentaranwendung{#embed-a-comments-app} einbetten

Das Einbetten der Kommentaranwendung erfolgt nach dem Einbetten einer Core-App.

Das Einbetten der Kommentaranwendung erfolgt nach dem Einbetten einer Core-App, wie unter [Eine App](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) einbetten beschrieben.

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
