---
description: Sie können auf einer Instanz von Siegels auf Ereignis hören.
title: Sizilien-App-Ereignis
exl-id: e341ca76-002d-425c-8d1a-35c3253fb254
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Sibezeichnet App-Ereignis {#sidenotes-app-events}

Sie können auf einer Instanz von Siegels auf Ereignis hören.

Rückrufe können bei der `onmethod`-Methode registriert und bei der `removeListener`-Methode nicht registriert werden. Eine `once`-Methode ist verfügbar, wenn der Rückruf nur einmal aufgerufen und dann nicht registriert werden soll.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Weitere Informationen zu Livefyre-Ereignissen finden Sie auf der Seite &quot;JavaScript-Ereignis&quot;im Abschnitt &quot;Referenz&quot;.

| Schlüssel | Beschreibung |
|--- |--- |
| sidenotes.initialized | Wird ausgelöst, wenn die App instanziiert wird, Daten enthält und sich auf der Seite befindet. |
| sidenotes.commentFlagged | Wird ausgelöst, wenn ein Kommentar markiert wurde. Daten enthalten: <br><ul><li>`targetId`: ID des gekennzeichneten Kommentars</li><li>`type`: Zeichentypzeichenfolge  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Wird ausgelöst, wenn ein Kommentar veröffentlicht wurde. Daten enthalten: <br><ul><li> `authorId`: ID des Verfassers des Kommentars </li><li>`bodyHtml`: Kommentartext </li><li> `parent`: id des übergeordneten Kommentars oder null</li></ul> |
| `sidenotes.commentShared` | Wird ausgelöst, wenn ein Kommentar freigegeben wurde. Daten enthalten: <br><ul><li>`targetId`: ID des freigegebenen Kommentars </li><li> `sharedToFacebook`: ob der Kommentar für Facebook freigegeben wurde </li><li>`sharedToTwitter`: ob der Kommentar für Twitter freigegeben wurde</li></ul> |
| `sidenotes.commentVoted` | Wird ausgelöst, wenn über einen Kommentar abgestimmt wurde. Daten enthalten: <br><ul><li>`targetId`: ID der Bemerkung, über die abgestimmt wurde </li><li> `targetAuthorId`: ID des Verfassers, über den abgestimmt wurde</li><li> `type`: numerische Stimmart: 0: &quot;clear&quot;, 1: &quot;Hochrechnung&quot;oder 2: &quot;downAbstimmung&quot;</li></ul> |
| `sidenotes.userLoggedIn` | Wird ausgelöst, wenn sich ein Benutzer anmeldet. Daten enthalten: <br><ul><li>`avatar`: avatar url for user </li><li>`displayName`: Anzeigename des Benutzers</li><li>`id`: ID des Benutzers</li><li> `isModerator`: ob der Benutzer Moderator der aktuellen Sammlung ist</li></ul> |
| `sidenotes.userLoggedOut` | Wird ausgelöst, wenn sich ein Benutzer abmeldet |
