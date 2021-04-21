---
description: Implementieren von Anmerkungen mithilfe der .js-Implementierung.
title: Implementierung von Sizilien
exl-id: 07a68677-c67e-4128-8cb7-c5fb9e0ecc60
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 22%

---

# Si7-Implementierung{#sidenotes-implementation}

## Implementieren von Anmerkungen mithilfe der .js-Implementierung

Übergeben Sie zur Implementierung dieser Funktion eine 1-1-Objektzuordnung der Zeichenfolgen, die Sie überschreiben möchten, an das JavaScript-Konfigurationsobjekt. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

### Beispiel 

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
