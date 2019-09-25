---
description: Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den Siegels-Konstruktor eingefügt wird.
seo-description: Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den Siegels-Konstruktor eingefügt wird.
seo-title: Benutzerdefinierte Stile
title: Benutzerdefinierte Stile
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Benutzerdefinierte Stile{#sidenotes-custom-styles}

Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den Siegels-Konstruktor eingefügt wird.

Die "Schlüssel"sind Objektschlüssel, die DOM-Elemente darstellen, während "Eigenschaften"für den jeweiligen Schlüssel unterstützt werden. Um beispielsweise den Stil von blockBtn anzupassen (d. h. die Schaltfläche, mit der das Siegels-Popup gestartet wird), würde ein Objekt wie das folgende erstellt:

```
var styles = { 
   'blockBtn': { 
      'fontColor': '#555', 
      'fontSize': '18px' 
   } 
}; 
new Livefyre.Sidenotes({ 
   customStyles: styles, 
      ...  
})
```

| **Schlüssel** | **Eigenschaften** | Beschreibung |
|---|---|---|
| `anonymousAvatar` | "height", "width" | Anonymes Avatarbild, links neben dem Texteditor. |
| `blockBtn` | "fontColor", "fontSize", "left", "position", "right", "top" | Das "Startsymbol", das neben den Elementen platziert wird, die als "sidenote-fähig"angegeben wurden. |
| `blockBtnActive` | "fontColor", "fontSize", "left", "position", "right", "top" | Startsymbol, wenn es sich in einem aktiven Status befindet. |
| `commentAvatar` | "height", "width" | Avatar-Bild links von Notizen der obersten Ebene. |
| `commentBody` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Textkörper von Notizen mit Gewinde. |
| `commentDisplayName` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Anzeigename des Benutzers, der eine Notiz hinterlassen hat. |
| `commentDownvote` | "fontColor", "fontSize" | Schaltfläche zum Herunterfahren auf einer Notiz. |
| `commentReplyExpand` | "backgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Schaltfläche zum Erweitern von Threads mit einer großen Anzahl von Antworten. |
| `commentTags` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Tags über einen Benutzer in einer Notiz. |
| `commentUpvote` | "fontColor", "fontSize" | Schaltfläche zum Hochladen auf einer Notiz. |
| `editorTextarea` | "height", "width", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Textarea Eingabefeld zum Verlassen von Notizen. |
| `mediaBlockBtn` | "fontColor", "fontSize", "left", "position", "right", "top" | Symbol "Media Launcher"über einem Medienelement (img, video). |
| `mediaBlockBtnActive` | "fontColor", "fontSize", "left", "position", "right", "top" | Symbol "Media Launcher"in einem aktiven Status. |
| `numSidenotes` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight", "backgroundColor", "borderColor", "borderWidth", "height", "width" | Klicken Sie auf eine Schaltfläche, die die Anzahl der Siegels in der Sammlung anzeigt. |
| `numSidenotesPopover` | "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight", "backgroundColor", "borderColor", "borderWidth", "height", "width" | Geben Sie eine kurze Erläuterung zu Siegels für den Benutzer ein. |
| `popover` | "backgroundColor" | Popover, der beim Aufruf des Startersymbols angezeigt wird. |
| `popoverArrowLeft` | "backgroundImage", "height", "left", "right", "top", "width" | Linkes Pfeilelement im Popup, das auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `popoverArrorRight` | "backgroundImage", "height", "left", "right", "top", "width" | Rechtes Pfeilelement im Popup, das auf das DOM-Element mit einem Startersymbol verweist. |
| `popoverArrowTop` | "backgroundImage", "height", "left", "right", "top", "width" | Oberer Pfeil im Popup-Fenster, der auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `replyAvatar` | "height", "width" | Avatar-Bild links neben den Notizen auf Antwortebene. |
| `streamPoweredBy` | "backgroundColor", "borderColor", "lineHeight" | Fußzeile "Powered by"im Popup-Fenster. |
| `streamQueueButton` | "backgroundColor", "borderColor", "borderWidth", "fontColor", "fontFamily", "fontSize", "fontWeight", "lineHeight" | Schaltfläche, die angibt, wann neue Notizen in ein geöffnetes Popup fließen. |
| `userAvatar` | "height", "width" | Avatarbild des authentifizierten Benutzers links neben dem Texteditor. |

