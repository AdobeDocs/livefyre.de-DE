---
description: Implementieren von Anmerkungen mithilfe der .js-Implementierung.
seo-description: Implementieren von Anmerkungen mithilfe der .js-Implementierung.
seo-title: Implementierung von Sizilien
solution: Experience Manager
title: Implementierung von Sizilien
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Implementierung von Sizilien{#sidenotes-implementation}

## Implementieren von Anmerkungen mithilfe der .js-Implementierung

Übergeben Sie zur Implementierung dieser Funktion eine 1-1-Objektzuordnung der Zeichenfolgen, die Sie überschreiben möchten, an das JavaScript-Konfigurationsobjekt. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

### Beispiel 

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
