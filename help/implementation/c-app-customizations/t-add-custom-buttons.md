---
description: hinzufügen Sie benutzerdefinierte Aktionen für Ihre Livefyre-Apps.
seo-description: hinzufügen Sie benutzerdefinierte Aktionen für Ihre Livefyre-Apps.
seo-title: hinzufügen benutzerdefinierter Schaltflächen
solution: Experience Manager
title: hinzufügen benutzerdefinierter Schaltflächen
uuid: 27d24c21-d83f-49df-9b3f-15d7abbd2bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '136'
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
