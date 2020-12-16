---
description: Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.
seo-description: Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.
seo-title: updateAnchors-Methode
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---


# updateAnchors-Methode {#updateAnchorsMethod}

Verwenden Sie die updateAnchors-Methode, um der Seite dynamisch zugewiesenen Inhalt hinzuzufügen.

Diese Methode eignet sich für die Paginierung oder in anderen Fällen, in denen der Seite dynamisch Inhalte hinzugefügt werden, die mit einer eigenen Schreibweise versehen sind. Diese Methode definiert neue Anker für die zugeordneten Elemente und verwendet ein einziges Argument: newSelectors.

**newSelectors**. Die Selektoren, die zu Simit hinzugefügt werden sollen. Dies kann eine Selektorzeichenfolge, ein jQuery-Objekt oder ein Array von Elementen sein (ein beliebiger Typ, der vom Selektorargument akzeptiert wird, das während der App-Erstellung weitergegeben wird).
Format:

```
app.updateAnchors(newSelectors);
```

Beispiel:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
