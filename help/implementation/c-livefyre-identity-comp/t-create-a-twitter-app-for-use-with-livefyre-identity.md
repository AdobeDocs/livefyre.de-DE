---
description: Sie können Livefyre Identity mit Twitter verwenden, um Benutzern die Nutzung ihrer Twitter-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.
seo-description: Sie können Livefyre Identity mit Twitter verwenden, um Benutzern die Nutzung ihrer Twitter-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen einer Twitter-App zur Verwendung mit einer Livefyre-Identität
solution: Experience Manager
title: Erstellen einer Twitter-App zur Verwendung mit einer Livefyre-Identität
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen einer Twitter-App zur Verwendung mit einer Livefyre-Identität{#create-a-twitter-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit Twitter verwenden, um Benutzern die Nutzung ihrer Twitter-Anmeldungen zu ermöglichen, Apps auf Ihrer Site zu interagieren.

Zur Aktivierung der Twitter-Anmeldung benötigt Livefyre die folgenden Twitter-App-Informationen:

* Benutzerschlüssel (API-Schlüssel)
* Verbrauchergeheimnis (API-Geheimnis)

So erstellen Sie eine Twitter-App zur Verwendung mit Livefyre-Identität:

1. Wechseln Sie zu [https://apps.twitter.com/](https://apps.twitter.com/)und melden Sie sich bei Ihrem Twitter-Konto an, um eine neue App zu erstellen oder eine vorhandene App zur Verwendung mit Livefyre Identity auszuwählen.
1. Auf der Seite "Einstellungen"für die App:

   * Geben Sie **[!UICONTROL Callback URL:]** (wobei `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre`{networkName}**** Ihr Livefyre-bereitgestellter Netzwerkname ist) ein. For example:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deaktivieren Sie **[!UICONTROL Enable Callback Locking]**.
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Wählen Sie auf der **[!UICONTROL Permissions]** Registerkarte **[!UICONTROL Access: Read only]**.

Nach Abschluss des Vorgangs werden auf der Seite "Anwendungsverwaltung"&gt; "Schlüssel und Zugriffstoken"der Benutzerschlüssel (API-Schlüssel) der App und der geheime Verbraucherschlüssel (API-Schlüssel) für die Verwendung auf der Seite "Integrationseinstellungen"von Studio aufgelistet.
