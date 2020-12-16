---
description: Sie können den Warnungstext ändern, der auf Videomasken angezeigt wird.
seo-description: Sie können den Warnungstext ändern, der auf Videomasken angezeigt wird.
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bf45-4e70-a5f9-37f5e7c61f8e
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '119'
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
