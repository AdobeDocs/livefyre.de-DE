---
description: Fügen Sie der Seite das Flag userPrivacyOptOut hinzu, damit ein Besucher der Site diese Verfolgung abwählen kann.
seo-description: Fügen Sie der Seite das Flag userPrivacyOptOut hinzu, damit ein Besucher der Site diese Verfolgung abwählen kann.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyOptOut{#userprivacyoptout}

Fügen Sie der Seite das `userPrivacyOptOut` Flag hinzu, damit ein Site-Besucher diese Verfolgung abwählen kann.

Livefyre bietet JavaScript-Ereignisse zur Verfolgung von Benutzeraktivitäten in Ihren Livefyre-Apps.

Wenn Sie Livefyre-Apps einbetten und ein Besucher der Verfolgung nicht zustimmt, können Sie Livefyre dynamisch so konfigurieren, dass Funktionen deaktiviert werden, um die Privatsphäre des Besuchers zu gewährleisten.

Wenn Livefyre konfiguriert ist,

* Deaktivieren Sie die Authentifizierungsunterstützung in Apps.
* LiveCycle und Ereigniserstellung deaktivieren
* Löschen Sie vorhandene Cookies, die von Apps erstellt wurden, die sich auf der Seite befinden
* Proxy-Medien mit Bildern von Drittanbieterdomänen, um zu verhindern, dass Drittanbieter Cookies erstellen
* Durchklicken von Videomasken für Videos von Drittanbietern, für die ein zusätzlicher Klick erforderlich ist

## Seite für Ausschluss konfigurieren

Integrationen, die Livefyre-Apps einbetten, können Livefyre konfigurieren, wenn ein Sitebesucher keine Einwilligung mit einer einzelnen JavaScript-Variablen erteilt hat.

Anleitung:

1. Fügen Sie der Seite vor dem `userPrivacyOptOut` JavaScript das `Livefyre.js` Flag hinzu:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Fügen Sie `Livefyre.js` der Seite an einer beliebigen Stelle nach `userPrivacyOptOut`.

   Livefyre-Apps instanziieren mit den erhöhten Datenschutzeinstellungen.

   >[!NOTE]
   >
   >Ändern Sie den Wert nicht mehr, wenn `userPrivacyOptOut` Livefyre-Apps geladen wurden.

Stellen Sie sicher, dass Ihr Arbeitsablauf für die Zustimmung den Wert "true" `userPrivacyOptOut` angibt, wenn sich ein Besucher der Site für die Abmeldung entscheidet.
