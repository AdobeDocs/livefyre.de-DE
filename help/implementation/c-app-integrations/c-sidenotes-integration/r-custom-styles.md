---
description: Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den DOM-Konstruktor eingefügt wurde.
seo-description: Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den DOM-Konstruktor eingefügt wurde.
seo-title: Benutzerdefinierte Stile
title: Benutzerdefinierte Stile
uuid: 0 f 6 d 7 ad 6-1 f 6 a -4 ed 2-b 86 a -0 d 03782 e 591 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Benutzerdefinierte Stile{#sidenotes-custom-styles}

Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den DOM-Konstruktor eingefügt wurde.

Die &quot;Schlüssel&quot; sind Objektschlüssel, die DOM-Elemente darstellen, während&quot; Eigenschaften&quot; CSS-Eigenschaften für den jeweiligen Schlüssel werden. Um beispielsweise den Stil der blockbtn (die Schaltfläche, mit der der Popover &quot;Sidenotes&quot; gestartet wird) anzupassen, würde ein Objekt ein Objekt wie z. B. folgende Konstrukte konstruieren:

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
| `anonymousAvatar` | &#39; height &#39;,&#39; width &#39; | Anonymes Avatar-Bild links vom Textbereich-Editor. |
| `blockBtn` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Das &quot;Starter-Symbol&quot; platziert neben Elementen, die als autorisierbar festgelegt wurden. |
| `blockBtnActive` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Starter-Symbol in einem aktiven Status. |
| `commentAvatar` | &#39; height &#39;,&#39; width &#39; | Avatar-Bild links neben den Notizen auf der obersten Ebene. |
| `commentBody` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Textkörper der verketteten Notizen. |
| `commentDisplayName` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Anzeigename des Benutzers, der eine Notiz hinterlassen hat. |
| `commentDownvote` | &#39; Fontcolor &#39;,&#39; fontsize &#39; | Schaltfläche zum Herunterabstimmen auf einer Notiz. |
| `commentReplyExpand` | &#39; Backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Schaltfläche für Expanding-Threads mit einer großen Anzahl von Antworten. |
| `commentTags` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Tags über einen Benutzer auf einer Notiz. |
| `commentUpvote` | &#39; Fontcolor &#39;,&#39; fontsize &#39; | Schaltfläche &quot;Hochabstimmen&quot; auf einer Notiz. |
| `editorTextarea` | &#39; height &#39;,&#39; width &#39;,&#39; fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Texteingabefeld zum Verlassen von Notizen. |
| `mediaBlockBtn` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Medien-Starter-Symbol, wenn ein Medienelement (img, video) verwendet wird. |
| `mediaBlockBtnActive` | &#39; Fontcolor &#39;,&#39; fontsize &#39;,&#39; left &#39;,&#39; position &#39;,&#39; right &#39;,&#39; top &#39; | Medienstarter-Symbol in einem aktiven Zustand. |
| `numSidenotes` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39;,&#39; backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; height &#39;,&#39; width &#39; | Anklickbare Schaltfläche, die die Anzahl der &quot;Sidenotes&quot; in der Sammlung anzeigt. |
| `numSidenotesPopover` | &#39; Fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39;,&#39; backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; height &#39;,&#39; width &#39; | Popover mit einer kurzen Erklärung der Kritiker für den Benutzer. |
| `popover` | &#39; Backgroundcolor &#39; | Popover, der beim Aufrufen des Starter-Symbols aufgerufen wird. |
| `popoverArrowLeft` | &#39; Backgroundimage &#39;,&#39; height &#39;,&#39; left &#39;,&#39; right &#39;,&#39; top &#39;,&#39; width &#39; | Linkspfeil auf dem Poster, der auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `popoverArrorRight` | &#39; Backgroundimage &#39;,&#39; height &#39;,&#39; left &#39;,&#39; right &#39;,&#39; top &#39;,&#39; width &#39; | Pfeil nach rechts auf dem Poster, der auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `popoverArrowTop` | &#39; Backgroundimage &#39;,&#39; height &#39;,&#39; left &#39;,&#39; right &#39;,&#39; top &#39;,&#39; width &#39; | Top-Pfeilelement auf dem Poster, der auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `replyAvatar` | &#39; height &#39;,&#39; width &#39; | Avatar-Bild links neben den Anmerkungshinweisen. |
| `streamPoweredBy` | &#39; Backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; lineheight &#39; | Fußzeile auf dem Popover. |
| `streamQueueButton` | &#39; Backgroundcolor &#39;,&#39; bordercolor &#39;,&#39; borderwidth &#39;,&#39; fontcolor &#39;,&#39; fontfamily &#39;,&#39; fontsize &#39;,&#39; fontweight &#39;,&#39; lineheight &#39; | Schaltfläche, um anzugeben, wann neue Notizen in einen offenen Popover fließen. |
| `userAvatar` | &#39; height &#39;,&#39; width &#39; | Avatar des authentifizierten Benutzers links vom Textbereich-Editor. |

