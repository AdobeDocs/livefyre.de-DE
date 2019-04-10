---
description: Sie können Ereignisse auf einer Instanz von Sidenotes überwachen.
seo-description: Sie können Ereignisse auf einer Instanz von Sidenotes überwachen.
seo-title: App-Ereignisse für Wettbewerbe
solution: Experience Manager
title: App-Ereignisse für Wettbewerbe
uuid: afca 4 b 03-c 370-41 ca-aa 12-45 bc 357517 ca
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# App-Ereignisse für Wettbewerbe {#sidenotes-app-events}

Sie können Ereignisse auf einer Instanz von Sidenotes überwachen.

Rückrufe können bei der `onmethod``removeListener` Methode registriert und nicht registriert werden. `once` Eine Methode steht zur Verfügung, wenn der Rückruf nur einmal aufgerufen und dann nicht registriert werden soll.

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

Weitere Informationen zu Livefyre-Ereignissen finden Sie auf der Seite "Javascript-Ereignisse" im Abschnitt" Referenz" .

| Schlüssel | Beschreibung |
|--- |--- |
| sidenotes. initialized | Wird ausgelöst, wenn die App instanziiert wird, Daten enthält und sich auf der Seite befindet. |
| sidenotes. commentflag | Wird ausgelöst, wenn ein Kommentar gekennzeichnet wurde. Daten enthalten: <br><ul><li>`targetId`: ID des Kommentars, das markiert wurde</li><li>`type`: Flag-Typ-Zeichenfolge `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | Wird ausgelöst, wenn ein Kommentar veröffentlicht wurde. Daten enthalten: <br><ul><li> `authorId`: ID des Autors des Kommentars </li><li>`bodyHtml`: Text des Kommentars </li><li> `parent`: ID des übergeordneten Kommentars oder null</li></ul> |
| `sidenotes.commentShared` | Wird ausgelöst, wenn ein Kommentar freigegeben wurde. Daten enthalten: <br><ul><li>`targetId`: ID des freigegebenen Kommentars </li><li> `sharedToFacebook`: ob der Kommentar für Facebook freigegeben wurde </li><li>`sharedToTwitter`: ob der Kommentar für Twitter freigegeben wurde</li></ul> |
| `sidenotes.commentVoted` | Wird ausgelöst, wenn ein Kommentar abgegeben wurde. Daten enthalten: <br><ul><li>`targetId`: ID des Kommentars, auf das abgestimmt wurde </li><li> `targetAuthorId`: ID des Autors, dessen Kommentar abgegeben wurde</li><li> `type`: numerischer Abstimmungstyp: 0: ' clear ', 1: ' upabstimmen'oder 2: ' downabstimmen '</li></ul> |
| `sidenotes.userLoggedIn` | Wird ausgelöst, wenn sich ein Benutzer anmeldet. Daten enthalten: <br><ul><li>`avatar`: Avatar-URL für den Benutzer </li><li>`displayName`: Anzeigename des Benutzers</li><li>`id`: ID des Benutzers</li><li> `isModerator`: ob der Benutzer ein Moderator der aktuellen Sammlung ist</li></ul> |
| `sidenotes.userLoggedOut` | Wird ausgelöst, wenn sich ein Benutzer anmeldet. |
