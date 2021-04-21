---
description: Sie können Livefyre Identity mit Twitter verwenden, um Benutzern zu ermöglichen, ihre Twitter-Anmeldungen zu verwenden, um mit Apps auf Ihrer Site zu interagieren.
title: Twitter-App zur Verwendung mit Livefyre-Identität erstellen
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Erstellen einer Twitter-App zur Verwendung mit Livefyre-Identität{#create-a-twitter-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit Twitter verwenden, um Benutzern zu ermöglichen, ihre Twitter-Anmeldungen zu verwenden, um mit Apps auf Ihrer Site zu interagieren.

Zum Aktivieren der Twitter-Anmeldung benötigt Livefyre die folgenden Twitter-App-Informationen:

* Consumer key (API-Schlüssel)
* Consumer secret (API-geheimer Schlüssel)

So erstellen Sie eine Twitter-App zur Verwendung mit Livefyre Identity:

1. Wechseln Sie zu [https://apps.twitter.com/](https://apps.twitter.com/) und melden Sie sich bei Ihrem Twitter-Konto an, um eine neue App zu erstellen oder eine vorhandene App zur Verwendung mit Livefyre Identity auszuwählen.
1. Auf der Seite &quot;Einstellungen&quot;für die App:

   * Geben Sie **[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` ein (wobei **{networkName}** Ihr Livefyre-bereitgestellter Netzwerkname ist). Beispiel:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deaktivieren Sie **[!UICONTROL Enable Callback Locking]**.
   * Auswählen **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. Wählen Sie auf der Registerkarte **[!UICONTROL Permissions]** **[!UICONTROL Access: Read only]**.

Nach Abschluss des Vorgangs werden auf der Seite &quot;Anwendungsverwaltung&quot;> &quot;Schlüssel und Zugriffstoken&quot;die Consumer key (API-Schlüssel) und die Consumer secret (API-geheimer Schlüssel) der App zur Verwendung auf der Seite &quot;Integrationseinstellungen&quot;von Studio Liste.
