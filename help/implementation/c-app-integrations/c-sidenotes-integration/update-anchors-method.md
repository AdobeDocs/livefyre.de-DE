---
description: Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.
seo-description: Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.
seo-title: updateAnchors-Methode
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# updateAnchors-Methode {#updateAnchorsMethod}

Use the updateAnchors method to add sidenoted content to the page dynamically.

This method is useful for pagination, or in other cases where sidenote-able content is added to the page dynamically. This method defines new anchors for the matched elements, and takes a single argument: newSelectors.

**newSelectors.** The selectors to add to Sidenotes. This may be a selector string, a jQuery object, or an array of elements (any of the types accepted by the selectors argument passed during app construction).
Format:

```
app.updateAnchors(newSelectors);
```

Beispiel:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
