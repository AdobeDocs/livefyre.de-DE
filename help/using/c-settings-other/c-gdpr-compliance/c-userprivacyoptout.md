---
description: hinzufügen das Flag userPrivacyOptOut auf die Seite, damit ein Site-Besucher diese Verfolgung Opt-out kann.
title: userPrivacyOptOut
exl-id: 1e935e69-60af-4151-905c-93a1cccbeb49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# userPrivacyOptOut{#userprivacyoptout}

hinzufügen Sie das `userPrivacyOptOut`-Flag zur Seite, damit ein Site-Besucher diese Verfolgung Opt-out kann.

Livefyre bietet JavaScript-Ereignisse zur Verfolgung der Aktivität von Benutzern in Ihren Livefyre-Apps.

Wenn Sie Livefyre-Apps einbetten und ein Besucher der Verfolgung nicht zustimmt, können Sie Livefyre dynamisch so konfigurieren, dass Funktionen deaktiviert werden, um die Privatsphäre des Besuchers zu gewährleisten.

Bei der Konfiguration von Livefyre:

* Deaktivieren Sie die Authentifizierungsunterstützung in Apps.
* LiveCycle und Ereignis-Generierung deaktivieren
* Löschen Sie vorhandene Cookies, die von Apps erstellt wurden, die sich auf der Seite befinden
* Proxy-Medien mit Bildern von Drittanbieterdomänen, um zu verhindern, dass Drittanbieter Cookies erstellen
* Durchklicken der Videomaske für Videos von Drittanbietern, für die ein zusätzlicher Klick zur Ansicht erforderlich ist

## Seite für Ausschluss konfigurieren

Integrationen, die Livefyre-Apps einbetten, können Livefyre konfigurieren, wenn ein Site-Besucher keine Einwilligung mit einer einzelnen JavaScript-Variablen erteilt hat.

Anleitung:

1. hinzufügen Sie das `userPrivacyOptOut`-Flag auf der Seite vor dem JavaScript `Livefyre.js`:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. hinzufügen `Livefyre.js` an einer beliebigen Stelle nach `userPrivacyOptOut` auf die Seite.

   Livefyre-Apps instanziieren mit den erhöhten Datenschutzeinstellungen.

   >[!NOTE]
   >
   >Ändern Sie nicht den Wert von `userPrivacyOptOut`, nachdem Livefyre-Apps geladen wurden.

Stellen Sie sicher, dass Ihr Genehmigungsarbeitsablauf `userPrivacyOptOut` auf true setzt, wenn ein Site-Besucher Opt-out wählt.
