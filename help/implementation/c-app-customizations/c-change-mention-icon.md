---
description: Ändern Sie das für Livefyre-Benutzer angezeigte Symbol im Pull-down-Menü
  @mention.
seo-description: Ändern Sie das für Livefyre-Benutzer angezeigte Symbol im Pull-down-Menü
  @mention.
seo-title: Symbol @mention ändern
solution: Experience Manager
title: Symbol @mention ändern
uuid: a 395 f 4 ff-a 774-454 a -8 d 94-4 a 3371 d 8 cc 2 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# `@mention` Symbol ändern {#change-mention-icon}

Ändern Sie das für Livefyre-Benutzer angezeigte Symbol im `@mention` Pulldown-Menü.

Ändern Sie das im `@mention` Pulldown-Menü verwendete Livefyre-Symbol auf ein Symbol Ihrer Wahl, damit Sie Ihre Community-Mitglieder mit Ihrem eigenen Symbol angeben können.

## Beispiel 

Um dieses Symbol zu ändern, fügen Sie dem Stylesheet die folgende CSS hinzu. Ersetzen Sie <*Ihre Ressource*> url durch die URL des ausgewählten Bilds, um das standardmäßige Livefyre-Zeichen zu ersetzen.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
