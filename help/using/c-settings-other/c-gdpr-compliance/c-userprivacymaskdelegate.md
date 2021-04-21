---
description: Sie können den Warnungstext ändern, der auf Videomasken angezeigt wird.
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

Sie können den Warnungstext ändern, der auf Videomasken angezeigt wird.

Dieser Text entspricht der GDPR-Verordnung. Wenn eine Quelle keinen Proxy unterstützt, zeigt Livefyre diesen Text und eine Maske für den Inhalt an, es sei denn, ein Benutzer klickt auf das Video und genehmigt die potenzielle Verfolgung aus dieser Quelle.

Wenn Sie `userPrivacyMaskDelegate` nicht verwenden, wird der folgende Standardtext angezeigt:

hinzufügen `userPrivacyMaskDelegate` nach `userPrivacyOptOut`. Sie können alle Livefyre-Datenschutzkennzeichnungen gleichzeitig als Teil eines Livefyre-Objekts hinzufügen.

Hier ist ein Beispiel für die Verwendung von `userPrivacyMaskDelegate`:

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
