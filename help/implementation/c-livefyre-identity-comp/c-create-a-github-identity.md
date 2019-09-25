---
description: Sie können Livefyre Identity mit GitHub Identity verwenden, um Benutzern die Verwendung ihrer GitHub-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.
seo-description: Sie können Livefyre Identity mit GitHub Identity verwenden, um Benutzern die Verwendung ihrer GitHub-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen einer GitHub-Identitätsanwendung zur Verwendung mit Livefyre-Identität
title: Erstellen einer GitHub-Identitätsanwendung zur Verwendung mit Livefyre-Identität
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen einer GitHub-Identitätsanwendung zur Verwendung mit Livefyre-Identität{#create-a-github-identity-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit GitHub Identity verwenden, um Benutzern die Verwendung ihrer GitHub-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.

Damit sich Benutzer mit ihren GitHub-Identitätsberechtigungen anmelden können, benötigt Livefyre die folgenden GitHub-Identitätsinformationen:

* Client-ID (privater Schlüssel)
* geheimer Clientschlüssel (Kennwort)

So erstellen Sie eine GitHub-Identitäts-App zur Verwendung mit Livefyre-Identität:

1. Erstellen oder melden Sie sich bei einem GitHub-Konto an [](https://github.com/settings/developers).
1. Registrieren Sie eine neue oder wählen Sie eine vorhandene App zur Verwendung mit Livefyre Identity.
1. Geben Sie alle Informationen in das Formular ein. Geben Sie den **[!UICONTROL Authorization callback URL]** Namen anstelle des Netzwerknamens ein `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`.

1. Schalten Sie **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]** den **[!UICONTROL Enable GitHub Login]** Umschalter in **[!UICONTROL On]**.

1. Geben Sie die GitHub-Client-ID und den geheimen GitHub-Client ein.
1. Klicken Sie auf **[!UICONTROL Save Settings]**.

Nach Abschluss des Vorgangs werden auf der Seite mit den App-Details von GitHub Identity die Client-ID (Consumer Key) und der geheime Clientschlüssel (Consumer Secret) der App für die Verwendung auf der Seite "Integrationseinstellungen"von Studio aufgelistet.
