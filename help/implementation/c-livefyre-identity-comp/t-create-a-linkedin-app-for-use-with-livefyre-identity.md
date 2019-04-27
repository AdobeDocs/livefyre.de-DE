---
description: Sie können die Livefyre-Identität mit linkedin verwenden, damit Benutzer ihre linkedin-Anmeldungen verwenden können, um Apps auf Ihrer Site zu interagieren.
seo-description: Sie können die Livefyre-Identität mit linkedin verwenden, damit Benutzer ihre linkedin-Anmeldungen verwenden können, um Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen einer linkedin-App für die Verwendung mit Livefyre Identity
solution: Experience Manager
title: Erstellen einer linkedin-App für die Verwendung mit Livefyre Identity
uuid: c 5112 f 24-a 4 e 0-4526-afe 8-b 8 f 27 a 3 b 2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen einer linkedin-App für die Verwendung mit Livefyre Identity{#create-a-linkedin-app-for-use-with-livefyre-identity}

Sie können die Livefyre-Identität mit linkedin verwenden, damit Benutzer ihre linkedin-Anmeldungen verwenden können, um Apps auf Ihrer Site zu interagieren.

Um die linkedin-Anmeldung zu aktivieren, erfordert Livefyre die folgenden linkedin-App-Informationen:

* Kundenschlüssel (API-Schlüssel)
* Geheimer Verbraucherschlüssel (API-geheimer Schlüssel)

Erstellen einer linkedin-App für die Verwendung mit Livefyre-Identität:

1. Wechseln Sie zu https://www.linkedin.com/secure/developer und melden Sie sich bei Ihrem linkedin-Konto an, um eine neue App zu erstellen oder eine vorhandene App für die Verwendung mit Livefyre Identity auszuwählen.
1. Klicken **[!UICONTROL Create Application]** Sie auf.
1. Füllen Sie das Formular aus, um die Anwendung zu erstellen.
1. Aktivieren **[!UICONTROL Default Application Permissions]** Sie die Berechtigungen **[!UICONTROL r_basicprofile]** und **[!UICONTROL r_emailaddress]** App-Berechtigungen.
1. Geben Sie als **[!UICONTROL OAuth 2.0 Authorized Redirect URL]**`https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. Speichern Sie die App.
1. Schalten Sie in **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]****[!UICONTROL Enable LinkedIn Login]****[!UICONTROL On]** ein.
1. Geben Sie die Linkedin Client ID und den geheimen linkedin-Client-Schlüssel ein.
1. Klicken **[!UICONTROL Save Settings]** Sie auf.

Wenn die App-Details vollständig abgeschlossen sind, listet der APP-Schlüssel (Consumer-Schlüssel) des App-Schlüssels (Consumer-Schlüssel) und der API-geheime Schlüssel (Consumer Secret) zur Verwendung auf der Seite &quot;Integrationseinstellungen von Studio&quot; auf.
