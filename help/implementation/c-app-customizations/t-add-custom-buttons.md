---
description: hinzufügen Sie benutzerdefinierte Aktionen für Ihre Livefyre-Apps.
title: hinzufügen benutzerdefinierter Schaltflächen
exl-id: a62d8605-59c2-4214-af26-805c1989aca1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# hinzufügen benutzerspezifische Schaltflächen{#add-custom-buttons}

hinzufügen Sie benutzerdefinierte Aktionen für Ihre Livefyre-Apps.

Mit Livefyre können Sie benutzerdefinierte Schaltflächen neben den vorhandenen Aktionsschaltflächen (z. B. **[!UICONTROL Share]** und **[!UICONTROL Flag]**) zu einem Inhaltselement hinzufügen.

Verwenden Sie das mobile Argument, um zu definieren, ob die Schaltfläche auf Mobilgeräten angezeigt wird.

So fügen Sie beispielsweise eine benutzerdefinierte Aktionsschaltfläche für die Benutzeroberfläche Ihres Mobilgeräts hinzu:

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. Übergeben Sie ein zusätzliches Argument im ConvConfig-Objekt mit dem Namen actionButtons, das ein Array von Objekten enthält, das die einzelnen Schaltflächen beschreibt, die Sie hinzufügen möchten.
1. Definieren Sie einen Schlüssel für den Text, der für jede Schaltfläche angezeigt werden soll.
1. hinzufügen einen Rückruf, der bei einem click-Ereignis für jede Schaltfläche aufgerufen wird.

Der Rückruf wird mit einem Objekt mit zwei Schlüsseln aufgerufen: `authorId` und `contentId`.
