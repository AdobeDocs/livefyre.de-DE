---
description: Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.
title: Livefyre.js
uuid: null
exl-id: 5f60ce54-5669-4768-912d-c1b13946d8b8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

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
