---
description: Beschränken Sie den Medientyp, der in den App-Stream gelangt.
title: Medien beschränken
exl-id: ae09a058-41de-4b63-8654-cc82f5abad14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Medien beschränken{#restrict-media}

Beschränken Sie den Medientyp, der in den App-Stream gelangt.

Standardmäßig können alle Medienanlagen in Apps eingebettet werden. Mit Livefyre können Sie diese Option ändern, um zu verhindern, dass Benutzer ausgewählte Anlagentypen in Ihren Apps veröffentlichen.

>[!NOTE]
>
>Livefyre arbeitet mit Embedly zusammen, um Medienintegration zu ermöglichen. Weitere Informationen finden Sie unter Inhaltsintegration > Einbetten-Integration. Wenden Sie sich an Ihren technischen Kundenbetreuer, wenn Sie Fragen zur Linkerweiterung oder zu den Quellen haben.

Dieses Beispiel blockiert YouTube- und Vimeo-Einbettung aus Ihrem Kommentar-Stream:

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
