---
description: Implementieren von Anmerkungen mithilfe der .js-Implementierung.
seo-description: Implementieren von Anmerkungen mithilfe der .js-Implementierung.
seo-title: Implementierung von Sidenotes
solution: Experience Manager
title: Implementierung von Sidenotes
uuid: aa 13852 e-e 2 b 0-4 a 86-97 cd-d 08 ab 5 e 2 cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Implementierung von Sidenotes{#sidenotes-implementation}

## Implementieren von Anmerkungen mithilfe der .js-Implementierung

Übergeben Sie zur Implementierung dieser Funktion eine 1-1 Objektzuordnung der Zeichenfolgen, die Sie dem Javascript-Konfigurationsobjekt überschreiben möchten. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

### Beispiel 

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
