---
description: Sie können Livefyre Identity mit Facebook verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen zu verwenden, um mit Apps auf Ihrer Site zu interagieren.
seo-description: Sie können Livefyre Identity mit Facebook verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen zu verwenden, um mit Apps auf Ihrer Site zu interagieren.
seo-title: Facebook-App zur Verwendung mit Livefyre-Identität erstellen
solution: Experience Manager
title: Facebook-App zur Verwendung mit Livefyre-Identität erstellen
uuid: a7f7be4e-8986-4e79-831a-0bb0ae555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Erstellen einer Facebook-App zur Verwendung mit Livefyre-Identität{#create-a-facebook-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit Facebook verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen zu verwenden, um mit Apps auf Ihrer Site zu interagieren.

Damit sich Ihre Benutzer mit ihren Facebook-Anmeldedaten anmelden können, benötigt Livefyre die folgenden Facebook-App-Informationen:

* App-ID
* App-Geheim

So erstellen Sie eine Facebook-App zur Verwendung mit Livefyre-Identität:

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

Nach Abschluss des Vorgangs wird auf der Seite &quot;Dashboard&quot;des Facebook-Entwicklers Ihre App-ID und Ihr geheimer App-Schlüssel zur Verwendung in den Integrationseinstellungen von Studio Liste.
