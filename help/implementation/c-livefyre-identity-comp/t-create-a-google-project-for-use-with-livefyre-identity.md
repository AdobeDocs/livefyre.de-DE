---
description: Sie können die Livefyre-Identität mit Google verwenden, damit Benutzer
  ihre Google-Anmeldungen verwenden können, um mit Apps auf Ihrer Site zu interagieren.
seo-description: Sie können die Livefyre-Identität mit Google verwenden, damit Benutzer
  ihre Google-Anmeldungen verwenden können, um mit Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen eines Google Project für die Verwendung mit Livefyre Identity
solution: Experience Manager
title: Erstellen eines Google Project für die Verwendung mit Livefyre Identity
uuid: b 0 a 6 bb 8 a-abea -4 f 5 c -92 ed -26 e 60183 e 1 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen eines Google Project für die Verwendung mit Livefyre Identity{#create-a-google-project-for-use-with-livefyre-identity}

Sie können die Livefyre-Identität mit Google verwenden, damit Benutzer ihre Google-Anmeldungen verwenden können, um mit Apps auf Ihrer Site zu interagieren.

Damit Ihre Benutzer sich mit ihren Google-Anmeldeinformationen anmelden können, erfordert Livefyre die folgenden Google Project-Informationen:

* Client-ID
* Geheimer Clientschlüssel

Erstellen eines Google Project für die Verwendung mit Livefyre-Identität:

1. Wechseln Sie zu [https://console.cloud.google.com/project](https://console.cloud.google.com/project) und melden Sie sich bei Ihrem Google-Konto an, um eine neue App zu erstellen oder eine vorhandene App für die Verwendung mit Livefyre Identity auszuwählen.
1. Klicken **[!UICONTROL Enable and Manage APIs]**Sie im Projekt-Dashboard für die App auf.
1. Klicken Sie auf der API-Übersichtsseite unter Social apis auf, um die Google +-API zu aktivieren.
1. Wählen Sie auf der Seite API-Anmeldeinformationen **[!UICONTROL Credentials > New credentials > OAuth]** die Client-ID aus. Auf der **[!UICONTROL Create client ID]** Seite, die geöffnet wird:

   * Anwendungstyp auswählen: Webanwendung.
   * Geben Sie ein **[!UICONTROL Name]** für **[!UICONTROL Client ID]**.
   * Feld **[!UICONTROL Authorized JavaScript origins]** leer lassen.
   * Eingeben **[!UICONTROL Authorized redirect URIs]**: `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/google_fyre` (wo **[!UICONTROL {networkName}]** ist Ihr Livefyre-Netzwerkname angegeben) Beispiel: ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Klicken **[!UICONTROL Create]** Sie auf, um Ihre Anmeldedaten zu speichern.

Nach Abschluss des Vorgangs listet die Google API Manager > Anmeldeinformationen die Client-ID und den geheimen Clientnamen des Projekts für die Verwendung auf der Seite Integrationseinstellungen von Studio auf.
