---
description: Sie können Livefyre Identity mit Microsoft Live Identity verwenden, um Benutzern die Nutzung ihrer Facebook-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.
seo-description: Sie können Livefyre Identity mit Microsoft Live Identity verwenden, um Benutzern die Nutzung ihrer Facebook-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen einer Microsoft Live-Identitäts-App zur Verwendung mit Livefyre-Identität
solution: Experience Manager
title: Erstellen einer Microsoft Live-Identitäts-App zur Verwendung mit Livefyre-Identität
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen einer Microsoft Live-Identitäts-App zur Verwendung mit Livefyre-Identität{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit Microsoft Live Identity verwenden, um Benutzern die Nutzung ihrer Facebook-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.

Damit Benutzer sich mit ihren Microsoft Live-Identitätsberechtigungen anmelden können, benötigt Livefyre die folgenden Microsoft Live-Identitätsinformationen:

* Client-ID (privater Schlüssel)
* geheimer Clientschlüssel (Kennwort)

So erstellen Sie eine Microsoft Live Identity-App zur Verwendung mit Livefyre Identity:

1. Erstellen oder melden Sie sich bei einem Microsoft Live-Konto unter [https://apps.dev.microsoft.com an](https://apps.dev.microsoft.com/)
1. Erstellen Sie eine neue oder wählen Sie eine vorhandene App zur Verwendung mit Livefyre Identity aus.
1. Klicken Sie auf **[!UICONTROL Add Platform]** und wählen Sie dann Web als Plattformtyp aus.
1. Stellen Sie sicher, dass die **[!UICONTROL Allow Implicit Flow]** Option aktiviert ist, und geben Sie die Umleitungs-URL unter Verwendung Ihres Netzwerknamens anstelle von {Netzwerkname} ein: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. Erstellen Sie ein neues Kennwort-/Schlüsselpaar, um den privaten Schlüssel abzurufen.
1. Schalten Sie **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]** den **[!UICONTROL Enable Microsoft Live Login]** Umschalter in **[!UICONTROL On]**.
1. Geben Sie die Microsoft Live Client-ID und den geheimen Microsoft Live Client ein.
1. Klicken Sie auf **[!UICONTROL Save Settings]**.

Nach Abschluss des Vorgangs werden auf der Seite mit den App-Details von Microsoft Live Identity die Client-ID (Consumer Key) und der geheime Clientschlüssel (Consumer Secret) der App für die Verwendung in den Integrationseinstellungen von Studio aufgeführt.
