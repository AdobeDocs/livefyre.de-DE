---
description: Sie können die Livefyre-Identität mit Facebook verwenden, damit Benutzer ihre Facebook-Anmeldungen verwenden können, um mit Apps auf Ihrer Site zu interagieren.
seo-description: Sie können die Livefyre-Identität mit Facebook verwenden, damit Benutzer ihre Facebook-Anmeldungen verwenden können, um mit Apps auf Ihrer Site zu interagieren.
seo-title: Erstellen einer Facebook-App für die Verwendung mit Livefyre-Identität
solution: Experience Manager
title: Erstellen einer Facebook-App für die Verwendung mit Livefyre-Identität
uuid: a 7 f 7 be 4 e -9886-4 e 79-831 a -0 bb 0 ae 555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Erstellen einer Facebook-App für die Verwendung mit Livefyre-Identität{#create-a-facebook-app-for-use-with-livefyre-identity}

Sie können die Livefyre-Identität mit Facebook verwenden, damit Benutzer ihre Facebook-Anmeldungen verwenden können, um mit Apps auf Ihrer Site zu interagieren.

Damit Ihre Benutzer sich mit ihren Facebook-Anmeldeinformationen anmelden können, erfordert Livefyre die folgenden Facebook-App-Informationen:

* App-ID
* App-Geheimnis

So erstellen Sie eine Facebook-App für die Verwendung mit Livefyre-Identität:

1. Rufen Sie [https://developers.facebook.com/apps](https://developers.facebook.com/apps)auf.
1. Melden Sie sich bei Ihrem Facebook-Entwicklerkonto an.
1. Klicken **[!UICONTROL Add New App]** oder wählen Sie eine vorhandene App für die Verwendung mit Livefyre Identity aus.
1. Klicken **[!UICONTROL Settings]****[!UICONTROL Basic]** Sie auf und dann auf. Geben Sie eine **[!UICONTROL Contact Email]** Adresse, **[!UICONTROL Display Name]** einen, **[!UICONTROL Privacy Policy URL]****[!UICONTROL Terms of Service URL]** ein und ein.
1. Klicken Sie auf das Pluszeichen ( **[!UICONTROL +]**) neben **[!UICONTROL Products]**.
1. **[!UICONTROL Set Up]****[!UICONTROL Facebook Login]** Klicken Sie auf.
1. Klicken **[!UICONTROL Settings]** Sie auf und richten Sie Folgendes ein:

   * Auf **[!UICONTROL Client OAuth Login]****[!UICONTROL Yes]**.
   * Auf **[!UICONTROL Web OAuth Login]****[!UICONTROL Yes]**.
   * Auf **[!UICONTROL Use Strict Mode for Redirect URIs]****[!UICONTROL Yes]**.
   * Auf **[!UICONTROL Enforce HTTPS for Web OAuth Login]****[!UICONTROL Yes]**.
   * Fügen Sie unter **[!UICONTROL Valid OAuth redirect URLs]** fügen Sie die URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` hinzu (wobei `{networkName}` es sich um Ihren Netzwerknamen für Livefyre handelt).

1. **[!UICONTROL App Review]** Unter:

   * Machen Sie die App öffentlich.
   * Stellen Sie sicher, dass der **[!UICONTROL Approved Items]** Parameter **[!UICONTROL Login Permissions]** einschließlich `email`, `public_profile`und `user_friends`.

Nach Abschluss des Vorgangs listet die Facebook-Seite des Entwicklers Ihre App-ID und App-geheimer Schlüssel für die Verwendung in den Studio-Integrationseinstellungen auf.
