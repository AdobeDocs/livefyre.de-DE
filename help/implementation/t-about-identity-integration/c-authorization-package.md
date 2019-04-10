---
description: Installieren Sie das Authentifizierungspaket, um die Benutzerauthentifizierung
  zu aktivieren, damit Benutzer mit Ihren Apps interagieren können.
seo-description: Installieren Sie das Authentifizierungspaket, um die Benutzerauthentifizierung
  zu aktivieren, damit Benutzer mit Ihren Apps interagieren können.
seo-title: Authentifizierungspaket
solution: Experience Manager
title: Authentifizierungspaket
uuid: 4 eec 30 cf -66 b 6-408 d -985 d -3 e 23 b 8 b 70 d 01
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Authentifizierungspaket{#authentication-package}

Installieren Sie das Authentifizierungspaket, um die Benutzerauthentifizierung zu aktivieren, damit Benutzer mit Ihren Apps interagieren können.

Livefyre-Apps verwenden das globale Authentifizierungs-Paket, um Benutzer mit App-Aktionen zu verknüpfen. Das Auth-Paket `Livefyre.require`ist verfügbar.

Um die Authentifizierung auf Ihrer Seite zu aktivieren, fügen `Livefyre.js` Sie zuerst dem `<head>` Element Ihrer Webseite oder Website-Vorlage hinzu.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

Die Verwendung von Livefyre. erfordert die Aktivierung der Authentifizierung ähnlich wie die Verwendung anderer Pakete. Der Integrationscode, der authentifiziert werden muss, sieht wie folgt aus:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Methoden {#section_ojx_1lz_fz}

Nachdem das Authentifizierungsmodul mit der `Livefyre.require`obigen Funktion eingefügt wurde, stellt es die folgenden Methoden bereit, die Sie aufrufen können, um andere Apps auf der Seite zu authentifizierungsbezogenen Ereignissen zu benachrichtigen.

| Methode | Beschreibung |
|--- |--- |
| `.login(callback)` | Lösen Sie den Anmeldefluss wie vom registrierten authdelegate implementiert aus. In der Regel werden nur Authentifizierungsaktivierte Apps aufgerufen, nicht die Hostseite selbst. |
| `.logout(callback)` | Benachrichtigen Sie die Authentifizierung, dass sich der Endbenutzer bei einigen externen Mitteln abmeldet und dass alle abhängigen Apps ihren Authentifizierungsstatus bis zur nächsten Anmeldung löschen sollten. Dadurch wird die interne Sitzung gelöscht, die von Auth verwaltet wird. |
| `.authenticate(credentials)` | Benachrichtigen Sie Authentifizierungen, die ein Benutzer durch einige externe Mittel authentifiziert hat und ein Livefyre-Authentifizierungstoken für den Endbenutzer erworben wurde. Verwenden Sie dies, wenn Sie ein Cookie mit dem Livefyre-Token festlegen oder ein Token für den Benutzer haben und den Benutzer explizit anmelden möchten. Beispiel: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delegieren Sie die Implementierungsdetails der Authentifizierung (z. B. Ihren benutzerdefinierten Authentifizierungsfluss) auf ein Objekt, das Sie definieren. Dies muss auf der Hostseite aufgerufen werden, um interaktive Funktionen von Livefyre-Apps zu aktivieren. |

