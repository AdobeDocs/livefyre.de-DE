---
description: Sie können die Livefyre-Identität mit Microsoft Live Identity verwenden,
  damit Benutzer ihre Facebook-Anmeldungen verwenden können, um Apps auf Ihrer Site
  zu interagieren.
seo-description: Sie können die Livefyre-Identität mit Microsoft Live Identity verwenden,
  damit Benutzer ihre Facebook-Anmeldungen verwenden können, um Apps auf Ihrer Site
  zu interagieren.
seo-title: Erstellen einer Microsoft Live Identity App zur Verwendung mit Livefyre-Identität
solution: Experience Manager
title: Erstellen einer Microsoft Live Identity App zur Verwendung mit Livefyre-Identität
uuid: 0 c 13 e 1 bc -817 f -43 ed -85 d 5-09 c 9 e 95 b 6234
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Erstellen einer Microsoft Live Identity App zur Verwendung mit Livefyre-Identität{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Sie können die Livefyre-Identität mit Microsoft Live Identity verwenden, damit Benutzer ihre Facebook-Anmeldungen verwenden können, um Apps auf Ihrer Site zu interagieren.

Damit Benutzer sich mit ihren Microsoft Live Identity-Anmeldeinformationen anmelden können, erfordert Livefyre die folgenden Microsoft Live Identity Information:

* Client-ID (privater Schlüssel)
* Geheimer Clientschlüssel (Kennwort)

Erstellen einer Microsoft Live Identity-App für die Verwendung mit Livefyre-Identität:

1. Erstellen oder melden Sie sich bei einem Microsoft Live-Konto unter [https://apps.dev.microsoft.com an.](https://apps.dev.microsoft.com/)
1. Erstellen Sie eine neue oder wählen Sie eine vorhandene App für die Verwendung mit Livefyre-Identität aus.
1. Klicken **[!UICONTROL Add Platform]**Sie auf und wählen Sie dann Web als Plattformtyp.
1. Vergewissern Sie sich, dass die **[!UICONTROL Allow Implicit Flow]** Option aktiviert ist, und geben Sie die Umleitungs-URL unter Verwendung Ihres Netzwerknamens anstelle von {network-name} ein: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Erstellen Sie ein neues Kennwort/Schlüsselpaar, um den privaten Schlüssel abzurufen.
1. Schalten Sie in **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]****[!UICONTROL Enable Microsoft Live Login]****[!UICONTROL On]**ein.
1. Geben Sie die Microsoft Live Client ID und Microsoft Live Client Secret ein.
1. Klicken **[!UICONTROL Save Settings]**Sie auf.

Wenn die App-Details der Microsoft Live-Identität abgeschlossen sind, listet die Detailseite der App die Client-ID (Consumer-Schlüssel) und geheimer Clientschlüssel (Consumer-Secret) für die Verwendung auf der Seite "Integrationseinstellungen von Studio" auf.
