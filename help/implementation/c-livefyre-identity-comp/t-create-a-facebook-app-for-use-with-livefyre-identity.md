---
description: Sie können Livefyre Identity mit Facebook verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen für die Interaktion mit Apps auf Ihrer Site zu verwenden.
title: Facebook-App zur Verwendung mit Livefyre-Identität erstellen
exl-id: ec320865-6ea3-4f6f-a5f6-31f3d5cbdc93
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---

# Erstellen einer Facebook-App zur Verwendung mit Livefyre-Identität{#create-a-facebook-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit Facebook verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen für die Interaktion mit Apps auf Ihrer Site zu verwenden.

Damit Ihre Benutzer sich mit ihren Facebook-Anmeldedaten anmelden können, benötigen Sie für Livefyre die folgenden Facebook-App-Informationen:

* App-ID
* App-Geheim

So erstellen Sie eine Facebook-App zur Verwendung mit Livefyre Identity:

1. Gehen Sie zu [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Melden Sie sich bei Ihrem Facebook-Entwicklerkonto an.
1. Klicken Sie auf **[!UICONTROL Add New App]** oder wählen Sie eine vorhandene App zur Verwendung mit Livefyre Identity.
1. Klicken Sie auf **[!UICONTROL Settings]** und dann auf **[!UICONTROL Basic]**. Geben Sie eine **[!UICONTROL Contact Email]**-Adresse, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** und **[!UICONTROL Terms of Service URL]** ein.
1. Klicken Sie auf das Pluszeichen ( **[!UICONTROL +]**) neben **[!UICONTROL Products]**.
1. Klicken Sie auf **[!UICONTROL Set Up]** unter **[!UICONTROL Facebook Login]**.
1. Klicken Sie auf **[!UICONTROL Settings]** und richten Sie Folgendes ein:

   * Setzen Sie **[!UICONTROL Client OAuth Login]** auf **[!UICONTROL Yes]**.
   * Setzen Sie **[!UICONTROL Web OAuth Login]** auf **[!UICONTROL Yes]**.
   * Setzen Sie **[!UICONTROL Use Strict Mode for Redirect URIs]** auf **[!UICONTROL Yes]**.
   * Setzen Sie **[!UICONTROL Enforce HTTPS for Web OAuth Login]** auf **[!UICONTROL Yes]**.
   * Fügen Sie unter **[!UICONTROL Valid OAuth redirect URLs]** die URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` hinzu (wobei `{networkName}` Ihr Livefyre-bereitgestellter Netzwerkname ist).

1. Unter **[!UICONTROL App Review]**:

   * Machen Sie die App öffentlich.
   * Stellen Sie sicher, dass **[!UICONTROL Approved Items]** für **[!UICONTROL Login Permissions]** `email`, `public_profile` und `user_friends` eingeschlossen sind.

Nach Abschluss des Vorgangs werden auf der Facebook Developer&#39;s Dashboard-Seite Ihre App-ID und Ihr App-Geheimnis in den Integrationseinstellungen von Studio Liste.
