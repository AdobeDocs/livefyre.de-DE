---
description: Ändern Sie das für Livefyre-Benutzer angezeigte Symbol im Pull-down-Menü @mention.
title: Symbol @mention ändern
exl-id: e078ef7f-7f16-4f5d-9152-95ae7fe7e4bd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---

# Ändern Sie das Symbol `@mention` {#change-mention-icon}

Ändern Sie das Symbol, das für Livefyre-Benutzer im Pulldown-Menü `@mention` angezeigt wird.

Ändern Sie das Livefyre-Symbol, das im Pulldown-Menü `@mention` verwendet wird, in ein Symbol Ihrer Wahl, sodass Sie Ihre Community-Mitglieder mit Ihrem eigenen Symbol kennzeichnen können.

## Beispiel 

Um dieses Symbol zu ändern, fügen Sie dem Stylesheet die folgende CSS hinzu. Ersetzen Sie die URL &lt;*Ihrer Ressource* durch die URL des ausgewählten Bilds, um das standardmäßige Livefyre-Zeichen zu ersetzen.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
