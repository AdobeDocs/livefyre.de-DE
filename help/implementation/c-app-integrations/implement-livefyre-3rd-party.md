---
description: Erstellen Sie Livefyre-Apps von Grund auf, um benutzerdefinierte Erlebnisse und Datenvisualisierungen zu erstellen.
seo-description: Erstellen Sie Livefyre-Apps von Grund auf, um benutzerdefinierte Erlebnisse und Datenvisualisierungen zu erstellen.
seo-title: Integration von Livefyre in die Integration von Drittanbietern
solution: Experience Manager
title: Livefyre in ein CMS integrieren
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 40cd8c2c89c17134bfcda510527dd6fff41400b5

---


# Implementieren von Livefyre mit Integration von Drittanbietern

Erstellen Sie Livefyre-Apps von Grund auf, um benutzerdefinierte Erlebnisse und Datenvisualisierungen zu erstellen.

Sie können eine Livefyre-App von Grund auf neu erstellen, indem Sie mithilfe der Bootstrap- und Stream-API Livefyre- und Social-Daten nutzen.

Informationen zu unterstützten Authentifizierungsplattformen für Livefyre-Apps, für die eine Authentifizierung erforderlich ist, finden Sie unter Identitätsintegration.

So implementieren Sie Konvertierungs-Apps (Kommentare, Chat, Live-Blog, Siegels):

1. Führen Sie eine App-Integration durch.
a. Erstellen Sie eine Sammlung mit dem CollectionMeta-Token.
b. Integrieren von Livefyre-Apps in Sites mithilfe der Livefyre.js-Einbettungscode-Struktur.

   * Weitere Informationen zur Verwendung der Livefyre.js-Einbettungscodestruktur finden Sie unter [Einbetten einer App](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Informationen zur Integration der Kommentaranwendung finden Sie unter [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md).

   * Informationen zur Integration der Chat-App finden Sie unter [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Informationen zur Integration der Live-Blog-App finden Sie im [Live-Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Weitere Informationen zur Integration der Sibezeichnet-App finden Sie unter [Sibezeichnet](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Authentifizierungsintegration durchführen.
a. Erstellen Sie Auth-Token für Benutzer, um Benutzerdaten in Livefyre zu übermitteln und zu speichern.
b. Integration von Drittanbieterbenutzern und Authentifizierungsplattformen. Eine Liste der unterstützten Plattformen finden Sie unter [Identitätsintegration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Nehmen Sie App-Anpassungen vor. App-Anpassungsoptionen, um Ihr Branding und Ihren Stil anzupassen und benutzerdefinierte Funktionen hinzuzufügen.

So erstellen Sie eine Visualisierungs-App (Map, Media Wall, Trending, Karussell, Filmstreifen, Storify, Feature Card, Mosaic, Polls):

1. Führen Sie eine App-Integration durch.
a. Erstellen Sie eine Sammlung mit dem CollectionMeta-Token.
b. Integrieren von Livefyre-Apps in Sites mithilfe der Livefyre.js-Einbettungscode-Struktur. Weitere Informationen zur Verwendung der Livefyre.js-Einbettungscodestruktur finden Sie unter [Einbetten einer App](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Informationen zur Integration der Map-App finden Sie unter [Map](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Informationen zur Integration der Media Wall-App finden Sie unter [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Informationen zur Integration der Trends-App finden Sie unter [Trends](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Authentifizierungsintegration durchführen.
a. Erstellen Sie Auth-Token für Benutzer, um Benutzerdaten an Livefyre zu übermitteln und zu speichern.
b. Integration von Drittanbieterbenutzern und Authentifizierungsplattformen. Eine Liste der unterstützten Plattformen finden Sie unter [Identitätsintegration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre unterstützt keine Apps für Karussell, Filmstreifen, Storify, Feature Card, Mosaic und Polls, die Livefyre.js verwenden.
Integrieren Sie diese Apps mithilfe des Prozesses [Erstellen einer App](/help/using/c-about-apps/c-create-an-app.md) .