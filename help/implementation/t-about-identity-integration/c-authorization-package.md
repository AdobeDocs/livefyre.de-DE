---
description: Installieren Sie das Authentifizierungspaket, um die Benutzerauthentifizierung zu aktivieren, damit Benutzer mit Ihren Apps interagieren können.
seo-description: Installieren Sie das Authentifizierungspaket, um die Benutzerauthentifizierung zu aktivieren, damit Benutzer mit Ihren Apps interagieren können.
seo-title: Authentifizierungspaket
solution: Experience Manager
title: Authentifizierungspaket
uuid: 4eec30cf-66b6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---


# Authentifizierungspaket{#authentication-package}

Installieren Sie das Authentifizierungspaket, um die Benutzerauthentifizierung zu aktivieren, damit Benutzer mit Ihren Apps interagieren können.

Livefyre-Apps verwenden das globale Authentifizierungspaket, um Benutzer mit App-Aktionen zu verknüpfen. Das Authentifizierungspaket ist über `Livefyre.require` verfügbar.

Um die Authentifizierung auf Ihrer Seite zu aktivieren, fügen Sie zunächst `Livefyre.js` zum `<head>`-Element Ihrer Webseite oder Website-Vorlage hinzu.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

Die Verwendung von Livefyre.require zum Aktivieren von auth ist ähnlich wie die Verwendung von require zum Aufrufen anderer Pakete. Der Integrationscode, für den auth erforderlich ist, sieht wie folgt aus:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Methoden {#section_ojx_1lz_fz}

Wenn das Auth-Modul, wie oben beschrieben, mit `Livefyre.require` eingeschlossen wurde, stellt es die folgenden Methoden bereit, die Sie aufrufen können, um andere Apps auf der Seite über authentifizierungsbezogene Ereignis zu benachrichtigen.

| Methode | Beschreibung |
|--- |--- |
| `.login(callback)` | Auslösen des Anmeldeflusses, wie vom registrierten AuthDelegate implementiert. Normalerweise werden nur auth-fähige Apps diesen Aufruf ausführen, nicht die Hostseite selbst. |
| `.logout(callback)` | Informieren Sie darüber, dass der Endbenutzer sich auf externe Weise abgemeldet hat und dass alle vertrauenden Apps ihren Authentifizierungsstatus bis zur nächsten Anmeldung löschen sollten. Dadurch wird die von Auth geführte interne Sitzung gelöscht. |
| `.authenticate(credentials)` | Informieren Sie Auth darüber, dass ein Benutzer auf externe Weise authentifiziert wurde und ein Livefyre-Authentifizierungstoken für den Endbenutzer bereitgestellt wurde. Verwenden Sie dies, wenn Sie ein Cookie mit dem Livefyre-Token setzen oder ein Token für den Benutzer haben und den Benutzer explizit anmelden möchten. Beispiel: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delegieren Sie die Implementierungsdetails der Authentifizierung (z. B. Ihren benutzerdefinierten Authentifizierungsfluss) an ein von Ihnen definiertes Objekt. Dies muss von der Hostseite aufgerufen werden, um interaktive Funktionen von Livefyre-Apps zu aktivieren. |

