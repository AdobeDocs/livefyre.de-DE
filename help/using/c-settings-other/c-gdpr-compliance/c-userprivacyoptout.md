---
description: Fügen Sie der Seite das Flag userprivacyoptout hinzu, damit ein Site-Besucher
  diese Verfolgung abwählen kann.
seo-description: Fügen Sie der Seite das Flag userprivacyoptout hinzu, damit ein Site-Besucher
  diese Verfolgung abwählen kann.
seo-title: Userprivacyoptout
title: Userprivacyoptout
uuid: a 043 c 50 e -0 a 02-4 c 83-bbce -54 b 9 b 51316 a 5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyoptout{#userprivacyoptout}

Fügen Sie der Seite das `userPrivacyOptOut` Flag hinzu, damit ein Site-Besucher diese Verfolgung ablehnen kann.

Livefyre stellt javascript-Ereignisse zur Verfolgung von Benutzeraktivitäten in Ihren Livefyre-Apps bereit.

Wenn Sie Livefyre-Apps einbetten und ein Besucher nicht der Verfolgung zugestimmt hat, können Sie Livefyre dynamisch konfigurieren, um die Funktionalität zu deaktivieren, um die Privatsphäre des Besuchers sicherzustellen.

Bei Konfiguration wird Livefyre:

* Deaktivieren Sie die Authentifizierungsunterstützung in Apps.
* Livecount und Ereignisgenerierung deaktivieren
* Löschen von vorhandenen Cookies, die von Apps erstellt wurden, die sich auf der Seite befinden
* Proxy-Medien mit Bildern aus Drittanbieterdomänen, um Drittanbieter daran zu hindern, Cookies zu erstellen
* Aktivieren Sie die Clickthrough-Clickthrough-Clickthrough für Drittanbieter-Videos, für die ein zusätzlicher Klick zur Ansicht erforderlich ist.

## Seite für Ausschluss konfigurieren

Integrationen, die Livefyre-Apps einbetten, können Livefyre konfigurieren, wenn ein Site-Besucher die Zustimmung über eine einzige javascript-Variable nicht erteilt hat.

Anweisungen:

1. Fügen Sie der `userPrivacyOptOut` Seite vor dem `Livefyre.js` javascript das Flag hinzu:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Fügen `Livefyre.js` Sie jeder beliebigen Seite nach `userPrivacyOptOut`.

   Livefyre-Apps werden mit den erhöhten Datenschutzeinstellungen instanziiert.

   >[!NOTE]
   >
   >Ändern Sie nicht den Wert von `userPrivacyOptOut` Livefyre-Apps, die geladen wurden.

Stellen Sie sicher, dass Ihr Arbeitsablauf für die Genehmigung den `userPrivacyOptOut` Wert "true" festlegt, wenn sich ein Site-Besucher auswählt.
