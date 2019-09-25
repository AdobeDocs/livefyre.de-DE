---
description: Sie können Livefyre Identity mit Facebook verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen für die Interaktion mit Apps auf Ihrer Site zu verwenden.
seo-description: Sie können Livefyre Identity mit Facebook verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen für die Interaktion mit Apps auf Ihrer Site zu verwenden.
seo-title: Facebook-App zur Verwendung mit Livefyre-Identität erstellen
solution: Experience Manager
title: Facebook-App zur Verwendung mit Livefyre-Identität erstellen
uuid: a7f7be4e-8986-4e79-831a-0bb0ae555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Facebook-App zur Verwendung mit Livefyre-Identität erstellen{#create-a-facebook-app-for-use-with-livefyre-identity}

Sie können Livefyre Identity mit Facebook verwenden, um Benutzern zu ermöglichen, ihre Facebook-Anmeldungen für die Interaktion mit Apps auf Ihrer Site zu verwenden.

Damit sich Ihre Benutzer mit ihren Facebook-Anmeldedaten anmelden können, benötigt Livefyre die folgenden Facebook-App-Informationen:

* App-ID
* App-Geheim

So erstellen Sie eine Facebook-App zur Verwendung mit Livefyre-Identität:

1. Wechseln Sie zu [https://developers.facebook.com/apps](https://developers.facebook.com/apps).
1. Melden Sie sich bei Ihrem Facebook-Entwicklerkonto an.
1. Klicken Sie auf **[!UICONTROL Add New App]** oder wählen Sie eine vorhandene App zur Verwendung mit Livefyre Identity aus.
1. Klicken Sie auf **[!UICONTROL Settings]** und dann **[!UICONTROL Basic]**. Geben Sie eine **[!UICONTROL Contact Email]** Adresse, **[!UICONTROL Display Name]**, **[!UICONTROL Privacy Policy URL]** und ein **[!UICONTROL Terms of Service URL]**.
1. Klicken Sie auf das Pluszeichen ( **[!UICONTROL +]**) neben **[!UICONTROL Products]**.
1. Klicken Sie **[!UICONTROL Set Up]** unter **[!UICONTROL Facebook Login]**.
1. Klicken Sie auf **[!UICONTROL Settings]** und richten Sie Folgendes ein:

   * Set **[!UICONTROL Client OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Web OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Use Strict Mode for Redirect URIs]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Enforce HTTPS for Web OAuth Login]** to **[!UICONTROL Yes]**.
   * Fügen Sie unter **[!UICONTROL Valid OAuth redirect URLs]** die URL hinzu `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (wobei `{networkName}` der von Livefyre bereitgestellte Netzwerkname ist).

1. Under **[!UICONTROL App Review]**:

   * Machen Sie die App öffentlich.
   * Stellen Sie sicher, dass die **[!UICONTROL Approved Items]** für **[!UICONTROL Login Permissions]** einschließlich `email`, `public_profile`und `user_friends`.

Nach Abschluss des Vorgangs werden auf der Dashboard-Seite des Facebook-Entwicklers Ihre App-ID und Ihr geheimer App-Schlüssel in den Integrationseinstellungen von Studio aufgeführt.
