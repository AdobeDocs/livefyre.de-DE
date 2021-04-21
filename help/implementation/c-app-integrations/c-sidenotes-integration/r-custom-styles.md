---
description: Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den Siegels-Konstruktor eingefügt wird.
title: Benutzerdefinierte Stile
exl-id: 846605b7-a21e-4600-bf17-18841d2ed96d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Benutzerdefinierte Stile für Sidemarkierungen{#sidenotes-custom-styles}

Benutzerdefinierte Stile werden über ein Objekt angewendet, das in den Siegels-Konstruktor eingefügt wird.

Die &quot;Schlüssel&quot;sind Objektschlüssel, die DOM-Elemente darstellen, während &quot;Eigenschaften&quot;für den jeweiligen Schlüssel unterstützt werden. Um beispielsweise den Stil von blockBtn anzupassen (d. h. die Schaltfläche, mit der das Siegels-Popup gestartet wird), würde ein Objekt wie das folgende erstellt:

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
| `anonymousAvatar` | &quot;height&quot;, &quot;width&quot; | Anonymes Avatarbild, links neben dem Texteditor. |
| `blockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Das &quot;Startsymbol&quot;, das neben den Elementen platziert wird, die als &quot;sidenote-fähig&quot;angegeben wurden. |
| `blockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Startsymbol, wenn es sich in einem aktiven Status befindet. |
| `commentAvatar` | &quot;height&quot;, &quot;width&quot; | Avatar-Bild links von Notizen der obersten Ebene. |
| `commentBody` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Textkörper von Notizen mit Gewinde. |
| `commentDisplayName` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Anzeigename des Benutzers, der eine Notiz hinterlassen hat. |
| `commentDownvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Schaltfläche zum Herunterfahren auf einer Notiz. |
| `commentReplyExpand` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Schaltfläche zum Erweitern von Threads mit einer großen Anzahl von Antworten. |
| `commentTags` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Tags über einen Benutzer in einer Notiz. |
| `commentUpvote` | &quot;fontColor&quot;, &quot;fontSize&quot; | Schaltfläche zum Hochladen auf einer Notiz. |
| `editorTextarea` | &quot;height&quot;, &quot;width&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Textarea Eingabefeld zum Verlassen von Notizen. |
| `mediaBlockBtn` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Symbol &quot;Media Launcher&quot;über einem Medienelement (img, video). |
| `mediaBlockBtnActive` | &quot;fontColor&quot;, &quot;fontSize&quot;, &quot;left&quot;, &quot;position&quot;, &quot;right&quot;, &quot;top&quot; | Symbol &quot;Media Launcher&quot;in einem aktiven Status. |
| `numSidenotes` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Klicken Sie auf eine Schaltfläche, die die Anzahl der Siegels in der Sammlung anzeigt. |
| `numSidenotesPopover` | &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot;, &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;height&quot;, &quot;width&quot; | Geben Sie eine kurze Erläuterung zu Siegels für den Benutzer ein. |
| `popover` | &quot;backgroundColor&quot; | Popover, der beim Aufrufen des Startersymbols angezeigt wird. |
| `popoverArrowLeft` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Linkes Pfeilelement im Popup, das auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `popoverArrorRight` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Rechtes Pfeilelement im Popup, das auf das DOM-Element mit einem Startersymbol verweist. |
| `popoverArrowTop` | &quot;backgroundImage&quot;, &quot;height&quot;, &quot;left&quot;, &quot;right&quot;, &quot;top&quot;, &quot;width&quot; | Oberer Pfeil im Popup-Fenster, der auf das DOM-Element verweist, das ein Startersymbol enthält. |
| `replyAvatar` | &quot;height&quot;, &quot;width&quot; | Avatar-Bild links neben den Notizen auf Antwortebene. |
| `streamPoweredBy` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;lineHeight&quot; | Fußzeile &quot;Powered by&quot;im Popup-Fenster. |
| `streamQueueButton` | &quot;backgroundColor&quot;, &quot;borderColor&quot;, &quot;borderWidth&quot;, &quot;fontColor&quot;, &quot;fontFamily&quot;, &quot;fontSize&quot;, &quot;fontWeight&quot;, &quot;lineHeight&quot; | Schaltfläche, die angibt, wann neue Notizen in ein geöffnetes Popup fließen. |
| `userAvatar` | &quot;height&quot;, &quot;width&quot; | Avatarbild des authentifizierten Benutzers links neben dem Texteditor. |
