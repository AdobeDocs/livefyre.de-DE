---
description: Fügen Sie Ihren Livefyre-Apps benutzerdefinierte Aktionen hinzu.
seo-description: Fügen Sie Ihren Livefyre-Apps benutzerdefinierte Aktionen hinzu.
seo-title: Benutzerdefinierte Schaltflächen hinzufügen
solution: Experience Manager
title: Benutzerdefinierte Schaltflächen hinzufügen
uuid: 27d24c21-d83f-49df-9b3f-15d7abbd2bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Benutzerdefinierte Schaltflächen hinzufügen{#add-custom-buttons}

Fügen Sie Ihren Livefyre-Apps benutzerdefinierte Aktionen hinzu.

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
1. Definieren Sie einen Schlüssel für den für jede Schaltfläche anzuzeigenden Text.
1. Fügen Sie für jede Schaltfläche einen Rückruf hinzu, der bei einem click-Ereignis aufgerufen wird.

Der Rückruf wird mit einem Objekt mit zwei Schlüsseln aufgerufen: `authorId` und `contentId`.
