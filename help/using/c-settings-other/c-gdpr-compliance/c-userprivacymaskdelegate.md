---
description: Sie können den Warntext ändern, der bei Videomasken angezeigt wird.
seo-description: Sie können den Warntext ändern, der bei Videomasken angezeigt wird.
seo-title: Userprivacymaskdelegate
solution: Experience Manager
title: Userprivacymaskdelegate
uuid: 8 e 5 a 2750-bf 45-4 e 70-a 5 f 9-37 f 5 e 7 c 61 f 8 e
translation-type: tm+mt
source-git-commit: 097321964ff078bac83c4674100f8c62a8f3a1af

---


# Userprivacymaskdelegate{#userprivacymaskdelegate}

Sie können den Warntext ändern, der bei Videomasken angezeigt wird.

Dieser Text ist vorhanden, um die GDPR-Regel einzuhalten. Wenn eine Quelle einen Proxy nicht unterstützt, zeigt Livefyre diesen Text und eine Maske auf dem Inhalt an, es sei denn, ein Benutzer klickt auf das Video und genehmigt die potenzielle Verfolgung aus dieser Quelle.

Wenn Sie nicht verwenden `userPrivacyMaskDelegate`, wird der folgende Standardtext angezeigt:

Hinzufügen `userPrivacyMaskDelegate` nach `userPrivacyOptOut`. Sie können alle Livefyre-Datenschutzmarkierungen gleichzeitig als Teil eines Livefyre-Objekts hinzufügen.

Hier sehen Sie ein Beispiel für die Verwendung `userPrivacyMaskDelegate`:

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
