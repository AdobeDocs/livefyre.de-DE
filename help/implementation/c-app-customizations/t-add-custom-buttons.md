---
description: Fügen Sie Ihren Livefyre-Apps benutzerdefinierte Aktionen hinzu.
seo-description: Fügen Sie Ihren Livefyre-Apps benutzerdefinierte Aktionen hinzu.
seo-title: Benutzerdefinierte Schaltflächen hinzufügen
solution: Experience Manager
title: Benutzerdefinierte Schaltflächen hinzufügen
uuid: 27 d 24 c 21-d 83 f -49 df -9 b 3 f -15 d 7 abbd 2 bd 7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Benutzerdefinierte Schaltflächen hinzufügen{#add-custom-buttons}

Fügen Sie Ihren Livefyre-Apps benutzerdefinierte Aktionen hinzu.

Mit Livefyre können Sie benutzerdefinierte Schaltflächen neben den vorhandenen Aktionsschaltflächen (z **[!UICONTROL Share]**. B. und **[!UICONTROL Flag]**) auf einem Inhaltselement hinzufügen.

Verwenden Sie das Argument Mobilgerät, um festzulegen, ob die Schaltfläche auf Mobilgeräten angezeigt werden soll.

Um beispielsweise eine benutzerdefinierte Aktionsschaltfläche für die Benutzeroberfläche Ihres Mobilgeräts hinzuzufügen:

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

1. Übergeben Sie ein zusätzliches Argument im Kontextconfig-Objekt actionbuttons, das ein Array von Objekten enthält, die die einzelnen Schaltflächen beschreiben, die Sie hinzufügen möchten.
1. Definieren Sie einen Schlüssel für den für die einzelnen Schaltflächen anzuzeigenden Text.
1. Fügen Sie einen Rückruf hinzu, der bei einem Klickereignis für jede Schaltfläche aufgerufen wird.

Der Rückruf wird mit einem Objekt mit zwei Schlüsseln aufgerufen: `authorId` und `contentId`.
