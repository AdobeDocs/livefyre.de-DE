---
description: Sie können die Livefyre-Identität mit Twitter verwenden, damit Benutzer
  ihre Twitter-Anmeldungen verwenden können, um Apps auf Ihrer Site zu interagieren.
seo-description: Sie können die Livefyre-Identität mit Twitter verwenden, damit Benutzer
  ihre Twitter-Anmeldungen verwenden können, um Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen einer Twitter-App für die Verwendung mit Livefyre Identity
solution: Experience Manager
title: Erstellen einer Twitter-App für die Verwendung mit Livefyre Identity
uuid: 841 cce 7 c -618 d -4154-85 a 3-1 de 96 d 04 bb 69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen einer Twitter-App für die Verwendung mit Livefyre Identity{#create-a-twitter-app-for-use-with-livefyre-identity}

Sie können die Livefyre-Identität mit Twitter verwenden, damit Benutzer ihre Twitter-Anmeldungen verwenden können, um Apps auf Ihrer Site zu interagieren.

Um die Twitter-Anmeldung zu aktivieren, erfordert Livefyre die folgenden Twitter-App-Informationen:

* Kundenschlüssel (API-Schlüssel)
* Geheimer Verbraucherschlüssel (API-geheimer Schlüssel)

So erstellen Sie eine Twitter-App für die Verwendung mit Livefyre-Identität:

1. Wechseln Sie zu [https://apps.twitter.com/](https://apps.twitter.com/)und melden Sie sich bei Ihrem Twitter-Konto an, um eine neue App zu erstellen oder eine vorhandene App für die Verwendung mit Livefyre-Identität auszuwählen.
1. Auf der Seite Einstellungen für die App:

   * Geben Sie **[!UICONTROL Callback URL:]**`https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (wobei **{networkname}** Ihr Livefyre-bereitgestellter Netzwerkname ist) ein. Beispiel: ** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deselect **[!UICONTROL Enable Callback Locking]**.
   * Wählen **[!UICONTROL Allow this application to be used to Sign in with Twitter]**Sie.

1. Wählen Sie aus der **[!UICONTROL Permissions]** Registerkarte **[!UICONTROL Access: Read only]**.

Wenn die Seite abgeschlossen ist, listet die Seite "Anwendungsverwaltung" >" Schlüssel und Zugriffstokens" der App den API-Schlüssel (API-Schlüssel) des App-Schlüssels (API-Schlüssel) und den geheimen Verbraucherschlüssel (API-geheimer Schlüssel) für die Verwendung auf der Seite "Integrationseinstellungen" von Studio auf.
