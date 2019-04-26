---
description: Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den
  DOM-Konstruktor eingefügt wurde.
seo-description: Benutzerdefinierte Stile werden über ein Objekt angewendet, das in
  den DOM-Konstruktor eingefügt wurde.
seo-title: Benutzerdefinierte Stile
title: Benutzerdefinierte Stile
uuid: 0 f 6 d 7 ad 6-1 f 6 a -4 ed 2-b 86 a -0 d 03782 e 591 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Benutzerdefinierte Stile{#sidenotes-custom-styles}

Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den DOM-Konstruktor eingefügt wurde.

Die "Schlüssel" sind Objektschlüssel, die DOM-Elemente darstellen, während" Eigenschaften" CSS-Eigenschaften für den jeweiligen Schlüssel werden. Um beispielsweise den Stil der blockbtn (die Schaltfläche, mit der der Popover "Sidenotes" gestartet wird) anzupassen, würde ein Objekt ein Objekt wie z. B. folgende Konstrukte konstruieren:

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
| `anonymousAvatar` | ' height ',' width ' | Anonymes Avatar-Bild links vom Textbereich-Editor. |
| `blockBtn` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Das "Starter-Symbol" platziert neben Elementen, die als autorisierbar festgelegt wurden. |
| `blockBtnActive` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Starter-Symbol in einem aktiven Status. |
| `commentAvatar` | ' height ',' width ' | Avatar-Bild links neben den Notizen auf der obersten Ebene. |
| `commentBody` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Textkörper der verketteten Notizen. |
| `commentDisplayName` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Anzeigename des Benutzers, der eine Notiz hinterlassen hat. |
| `commentDownvote` | ' Fontcolor ',' fontsize ' | Schaltfläche zum Herunterabstimmen auf einer Notiz. |
| `commentReplyExpand` | ' Backgroundcolor ',' bordercolor ',' borderwidth ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Schaltfläche für Expanding-Threads mit einer großen Anzahl von Antworten. |
| `commentTags` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Tags über einen Benutzer auf einer Notiz. |
| `commentUpvote` | ' Fontcolor ',' fontsize ' | Schaltfläche "Hochabstimmen" auf einer Notiz. |
| `editorTextarea` | ' height ',' width ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Texteingabefeld zum Verlassen von Notizen. |
| `mediaBlockBtn` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Medien-Starter-Symbol, wenn ein Medienelement (img, video) verwendet wird. |
| `mediaBlockBtnActive` | ' Fontcolor ',' fontsize ',' left ',' position ',' right ',' top ' | Medienstarter-Symbol in einem aktiven Zustand. |
| `numSidenotes` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ',' backgroundcolor ',' bordercolor ',' borderwidth ',' height ',' width ' | Anklickbare Schaltfläche, die die Anzahl der "Sidenotes" in der Sammlung anzeigt. |
| `numSidenotesPopover` | ' Fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ',' backgroundcolor ',' bordercolor ',' borderwidth ',' height ',' width ' | Popover mit einer kurzen Erklärung der Kritiker für den Benutzer. |
| `popover` | ' Backgroundcolor ' | Popover, der beim Aufrufen des Starter-Symbols aufgerufen wird. |
| `popoverArrowLeft` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | Linkspfeil auf dem Poster, der auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `popoverArrorRight` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | Pfeil nach rechts auf dem Poster, der auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `popoverArrowTop` | ' Backgroundimage ',' height ',' left ',' right ',' top ',' width ' | Top-Pfeilelement auf dem Poster, der auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `replyAvatar` | ' height ',' width ' | Avatar-Bild links neben den Anmerkungshinweisen. |
| `streamPoweredBy` | ' Backgroundcolor ',' bordercolor ',' lineheight ' | Fußzeile auf dem Popover. |
| `streamQueueButton` | ' Backgroundcolor ',' bordercolor ',' borderwidth ',' fontcolor ',' fontfamily ',' fontsize ',' fontweight ',' lineheight ' | Schaltfläche, um anzugeben, wann neue Notizen in einen offenen Popover fließen. |
| `userAvatar` | ' height ',' width ' | Avatar des authentifizierten Benutzers links vom Textbereich-Editor. |

