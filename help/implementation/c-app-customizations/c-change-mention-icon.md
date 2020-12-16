---
description: Ändern Sie das für Livefyre-Benutzer angezeigte Symbol im Pull-down-Menü @mention.
seo-description: Ändern Sie das für Livefyre-Benutzer angezeigte Symbol im Pull-down-Menü @mention.
seo-title: Symbol @mention ändern
solution: Experience Manager
title: Symbol @mention ändern
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 31%

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
