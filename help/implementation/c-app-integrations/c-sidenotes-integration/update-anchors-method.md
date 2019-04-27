---
description: Die Core-Livefyre-Bibliothek, die für den Betrieb von Livefyre auf Ihrer Site verwendet wird.
seo-description: Die Core-Livefyre-Bibliothek, die für den Betrieb von Livefyre auf Ihrer Site verwendet wird.
seo-title: Updateanchors-Methode
solution: Experience Manager
title: Livefyre. js
uuid: null
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Updateanchors-Methode {#updateAnchorsMethod}

Verwenden Sie die Methode updateanchors, um der Seite dynamisch gezählte Inhalte hinzuzufügen.

Diese Methode eignet sich für Paginierung oder in anderen Fällen, in denen der Inhalt der Seite dynamisch hinzugefügt wird. Diese Methode definiert neue Anker für die übereinstimmenden Elemente und akzeptiert ein einzelnes Argument: Newselectors.

**Newselectors**. Die Selektoren, die den Autoren hinzugefügt werden sollen. Dies kann eine Selektorzeichenfolge, ein jquery-Objekt oder ein Array von Elementen sein (beliebige Typen, die vom Selektoren-Argument akzeptiert werden, das während der App-Konstruktion übergeben wird).
Format:

```
app.updateAnchors(newSelectors);
```

Beispiel:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
