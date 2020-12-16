---
description: Beschränken Sie den Medientyp, der in den App-Stream gelangt.
seo-description: Beschränken Sie den Medientyp, der in den App-Stream gelangt.
seo-title: Medien beschränken
solution: Experience Manager
title: Medien beschränken
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Medien beschränken{#restrict-media}

Beschränken Sie den Medientyp, der in den App-Stream gelangt.

Standardmäßig können alle Medienanlagen in Apps eingebettet werden. Mit Livefyre können Sie diese Option ändern, um zu verhindern, dass Benutzer ausgewählte Anlagentypen in Ihren Apps veröffentlichen.

>[!NOTE]
>
>Livefyre arbeitet mit Embedly zusammen, um Medienintegration zu ermöglichen. Weitere Informationen finden Sie unter Inhaltsintegration > Einbetten-Integration. Wenden Sie sich an Ihren technischen Kundenbetreuer, wenn Sie Fragen zur Linkerweiterung oder zu den Quellen haben.

In diesem Beispiel werden YouTube- und Vimeo-Einbettungen aus Ihrem Kommentarstream blockiert:

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

