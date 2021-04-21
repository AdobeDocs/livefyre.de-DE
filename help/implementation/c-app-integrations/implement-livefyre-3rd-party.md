---
description: Erstellen Sie Livefyre-Apps von Grund auf, um benutzerdefinierte Erlebnisse und Datenvisualisierungen zu erstellen.
title: Livefyre in ein CMS integrieren
exl-id: 05d85792-de97-47b1-90cc-ad7e841754b5
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Implementieren von Livefyre mit Integration von Drittanbietern

Erstellen Sie Livefyre-Apps von Grund auf, um benutzerdefinierte Erlebnisse und Datenvisualisierungen zu erstellen.

Sie können eine Livefyre-App von Grund auf neu erstellen, indem Sie mithilfe der Bootstrap- und Stream-API Livefyre- und Social-Daten nutzen.

Informationen zu unterstützten Authentifizierungsplattformen für Livefyre-Apps, für die eine Authentifizierung erforderlich ist, finden Sie unter Identitätsintegration.

So implementieren Sie Konvertierungs-Apps (Kommentare, Chat, Live-Blog, Siegels):

1. Führen Sie eine App-Integration durch.
a. Erstellen Sie eine Sammlung mit dem CollectionMeta-Token.
b. Integrieren von Livefyre-Apps in Sites mithilfe der Livefyre.js-Einbettungscode-Struktur.

   * Weitere Informationen zur Verwendung der Livefyre.js-Einbettungscode-Struktur finden Sie unter [Eine App](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) einbetten.

   * Informationen zur Integration der Kommentaranwendung finden Sie unter [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md).

   * Informationen zur Integration der Chat-App finden Sie unter [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Informationen zur Integration der Live-Blog-App finden Sie unter [Live-Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Weitere Informationen zur Integration der Siegels-App finden Sie unter [Sibezeichnet](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Authentifizierungsintegration durchführen.
a. Erstellen Sie Auth-Token für Benutzer, um Benutzerdaten in Livefyre zu übermitteln und zu speichern.
b. Integration von Drittanbieterbenutzern und Authentifizierungsplattformen. Eine Liste der unterstützten Plattformen finden Sie unter [Identitätsintegration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Nehmen Sie App-Anpassungen vor. App-Anpassungsoptionen, um Ihr Branding und Ihren Stil anzupassen und benutzerdefinierte Funktionen hinzuzufügen.

So erstellen Sie eine Visualisierungs-App (Map, Media Wall, Trending, Karussell, Filmstreifen, Storify, Feature Card, Mosaic, Polls):

1. Führen Sie eine App-Integration durch.
a. Erstellen Sie eine Sammlung mit dem CollectionMeta-Token.
b. Integrieren von Livefyre-Apps in Sites mithilfe der Livefyre.js-Einbettungscode-Struktur. Weitere Informationen zur Verwendung der Livefyre.js-Einbettungscode-Struktur finden Sie unter [Eine App](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) einbetten.

   * Informationen zur Integration der Map-App finden Sie unter [Map](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Weitere Informationen zur Integration der Media Wall-App finden Sie unter [Medienwall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Weitere Informationen zur Integration der Trendanwendung finden Sie unter [Trending](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Authentifizierungsintegration durchführen.
a. Erstellen Sie Auth-Token für Benutzer, um Benutzerdaten an Livefyre zu übermitteln und zu speichern.
b. Integration von Drittanbieterbenutzern und Authentifizierungsplattformen. Eine Liste der unterstützten Plattformen finden Sie unter [Identitätsintegration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre unterstützt keine Karussell-, Filmstreifen-, Storify-, Feature Card-, Mosaic- und Polls-Apps, die Livefyre.js verwenden.

Integrieren Sie diese Apps mit dem Vorgang [App](/help/using/c-about-apps/c-create-an-app.md) erstellen.
