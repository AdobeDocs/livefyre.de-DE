---
description: Sie können Livefyre Identity mit GitHub Identity verwenden, um Benutzern die Verwendung ihrer GitHub-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.
seo-description: Sie können Livefyre Identity mit GitHub Identity verwenden, um Benutzern die Verwendung ihrer GitHub-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen einer GitHub-Identitätsanwendung zur Verwendung mit Livefyre-Identität
title: Erstellen einer GitHub-Identitätsanwendung zur Verwendung mit Livefyre-Identität
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# Erstellen einer GitHub-Identitätsanwendung zur Verwendung mit Livefyre-Identität{#create-a-github-identity-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit GitHub Identity verwenden, um Benutzern die Verwendung ihrer GitHub-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.

Damit sich Benutzer mit ihren GitHub-Identitätsberechtigungen anmelden können, benötigt Livefyre die folgenden GitHub-Identitätsinformationen:

* Client-ID (privater Schlüssel)
* geheimer Clientschlüssel (Kennwort)

So erstellen Sie eine GitHub-Identitäts-App zur Verwendung mit Livefyre-Identität:

1. Erstellen oder melden Sie sich bei einem GitHub-Konto unter [](https://github.com/settings/developers) an.
1. Registrieren Sie eine neue oder wählen Sie eine vorhandene App zur Verwendung mit Livefyre Identity.
1. Geben Sie alle Informationen in das Formular ein. Geben Sie **[!UICONTROL Authorization callback URL]** unter Verwendung Ihres Netzwerknamens anstelle von `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre` ein.

1. Wechseln Sie in **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]** den Umschalter **[!UICONTROL Enable GitHub Login]** zu **[!UICONTROL On]**.

1. Geben Sie die GitHub-Client-ID und den geheimen GitHub-Client ein.
1. Klicken **[!UICONTROL Save Settings]**.

Nach Abschluss des Vorgangs wird auf der Seite mit den App-Details von GitHub Identity die Client-ID (Consumer key) und der geheime Clientschlüssel (Consumer secret) der App für die Verwendung auf der Seite &quot;Integrationseinstellungen&quot;von Studio Liste.
