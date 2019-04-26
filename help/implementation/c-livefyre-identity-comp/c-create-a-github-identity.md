---
description: Sie können die Livefyre-Identität mit der github-Identität verwenden,
  damit Benutzer ihre github-Anmeldungen verwenden können, um Apps auf Ihrer Site
  zu interagieren.
seo-description: Sie können die Livefyre-Identität mit der github-Identität verwenden,
  damit Benutzer ihre github-Anmeldungen verwenden können, um Apps auf Ihrer Site
  zu interagieren.
seo-title: Erstellen einer github-Identitätsapp für die Verwendung mit Livefyre-Identität
title: Erstellen einer github-Identitätsapp für die Verwendung mit Livefyre-Identität
uuid: cf 56164 c -1521-4 a 42-89 cb -39483764807 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen einer github-Identitätsapp für die Verwendung mit Livefyre-Identität{#create-a-github-identity-app-for-use-with-livefyre-identity}

Sie können die Livefyre-Identität mit der github-Identität verwenden, damit Benutzer ihre github-Anmeldungen verwenden können, um Apps auf Ihrer Site zu interagieren.

Damit Benutzer sich mit ihren github Identity Credentials anmelden können, erfordert Livefyre die folgenden github-Identitätsinformationen:

* Client-ID (privater Schlüssel)
* Geheimer Clientschlüssel (Kennwort)

So erstellen Sie eine github-Identitätsapp für die Verwendung mit Livefyre-Identität:

1. Create or sign in to a GitHub account at [](https://github.com/settings/developers).
1. Registrieren Sie eine neue oder wählen Sie eine vorhandene App für die Verwendung mit Livefyre-Identität.
1. Geben Sie alle Informationen im Formular ein. Geben Sie unter **[!UICONTROL Authorization callback URL]**Verwendung Ihres Netzwerknamens statt `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`des Netzwerknamens ein.

1. Schalten Sie in **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]****[!UICONTROL Enable GitHub Login]****[!UICONTROL On]**ein.

1. Geben Sie die geheime github-Client-ID und den geheimen github-Client ein.
1. Klicken **[!UICONTROL Save Settings]**Sie auf.

Wenn die App-Details der Github-Identität abgeschlossen sind, listet die Detailseite der App die Client-ID (Consumer-Schlüssel) und geheimer Clientschlüssel (Consumer-Secret) für die Verwendung auf der Seite Integration von Studio auf.
