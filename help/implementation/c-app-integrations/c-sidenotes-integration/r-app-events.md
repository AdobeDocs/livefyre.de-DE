---
description: Sie können Ereignisse auf einer Instanz von Siegels überwachen.
seo-description: Sie können Ereignisse auf einer Instanz von Siegels überwachen.
seo-title: Sizilien-App-Ereignisse
solution: Experience Manager
title: Sizilien-App-Ereignisse
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Sizilien-App-Ereignisse {#sidenotes-app-events}

Sie können Ereignisse auf einer Instanz von Siegels überwachen.

Rückrufe können beim `onmethod` und nicht bei der `removeListener` Methode registriert werden. Eine `once` Methode ist verfügbar, wenn der Rückruf nur einmal aufgerufen und dann nicht registriert werden soll.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Weitere Informationen zu Livefyre-Ereignissen finden Sie auf der Seite "JavaScript-Ereignisse"im Abschnitt "Referenz".

| Schlüssel | Beschreibung |
|--- |--- |
| sidenotes.initialized | Wird ausgelöst, wenn die App instanziiert wird, Daten enthält und sich auf der Seite befindet. |
| sidenotes.commentGekennzeichnet | Wird ausgelöst, wenn ein Kommentar markiert wurde. Daten enthalten: <br><ul><li>`targetId`: ID des gekennzeichneten Kommentars</li><li>`type`: Zeichentyp `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Wird ausgelöst, wenn ein Kommentar veröffentlicht wurde. Daten enthalten: <br><ul><li> `authorId`: ID des Verfassers des Kommentars </li><li>`bodyHtml`: Kommentartext </li><li> `parent`: id des übergeordneten Kommentars oder null</li></ul> |
| `sidenotes.commentShared` | Wird ausgelöst, wenn ein Kommentar freigegeben wurde. Daten enthalten: <br><ul><li>`targetId`: ID des freigegebenen Kommentars </li><li> `sharedToFacebook`: ob der Kommentar für Facebook freigegeben wurde </li><li>`sharedToTwitter`: ob der Kommentar für Twitter freigegeben wurde</li></ul> |
| `sidenotes.commentVoted` | Wird ausgelöst, wenn über einen Kommentar abgestimmt wurde. Daten enthalten: <br><ul><li>`targetId`: ID der Bemerkung, über die abgestimmt wurde </li><li> `targetAuthorId`: ID des Verfassers, über den abgestimmt wurde</li><li> `type`: numerische Stimmart:0: "clear", 1: "Hochrechnung"oder 2: "downAbstimmung"</li></ul> |
| `sidenotes.userLoggedIn` | Wird ausgelöst, wenn sich ein Benutzer anmeldet. Daten enthalten: <br><ul><li>`avatar`: avatar url for user </li><li>`displayName`: Anzeigename des Benutzers</li><li>`id`: ID des Benutzers</li><li> `isModerator`: ob der Benutzer Moderator der aktuellen Sammlung ist</li></ul> |
| `sidenotes.userLoggedOut` | Wird ausgelöst, wenn sich ein Benutzer abmeldet |
