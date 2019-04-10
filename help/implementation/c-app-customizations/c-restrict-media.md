---
description: Begrenzen Sie den Medientyp, der in den App-Stream gelangt.
seo-description: Begrenzen Sie den Medientyp, der in den App-Stream gelangt.
seo-title: Medien beschränken
solution: Experience Manager
title: Medien beschränken
uuid: c 470 c 985-d 221-4 f 39-8 bd 4-4 e 44 ec 14 db 95
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Medien beschränken{#restrict-media}

Begrenzen Sie den Medientyp, der in den App-Stream gelangt.

Standardmäßig können alle Medienanlagen in Apps eingebettet werden. Mit Livefyre können Sie diese Option ändern, um zu verhindern, dass Benutzer ausgewählte Anhänge in Ihre Apps veröffentlichen.

>[!NOTE]
>
>Livefyre-Partner mit Embedly for Media Integration. Weitere Informationen finden Sie unter Content Integration > Integration einbetten. Wenden Sie sich an Ihren Technical Account Manager, um Fragen zur Erweiterung von Links oder zu Quellen zu erhalten.

In diesem Beispiel werden youtube- und Vimeo-Einbettungsvorgänge aus Ihrem Kommentarstream blockiert:

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

Beim Laden der Konversation:

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

