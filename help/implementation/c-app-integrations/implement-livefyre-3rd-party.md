---
description: Erstellen Sie Livefyre-Apps von Grund auf, um benutzerdefinierte Erlebnisse
  und Datenvisualisierungen zu erstellen.
seo-description: Erstellen Sie Livefyre-Apps von Grund auf, um benutzerdefinierte
  Erlebnisse und Datenvisualisierungen zu erstellen.
seo-title: Integrieren von Livefyre mit der Integration von Drittanbietern
solution: Experience Manager
title: Livefyre in ein CMS integrieren
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Implementieren von Livefyre mit der Integration von Drittanbietern

Erstellen Sie Livefyre-Apps von Grund auf, um benutzerdefinierte Erlebnisse und Datenvisualisierungen zu erstellen.

Sie können eine Livefyre-App von Grund auf neu erstellen, indem Sie Livefyre und soziale Daten mithilfe der Bootstrap- und Stream-API nutzen.

Informationen zu Livefyre-Apps, die Authentifizierung erfordern, finden Sie unter Identitätsintegration für Informationen zu unterstützten Authentifizierungsplattformen von Drittanbietern.

So implementieren Sie Unterhaltungsapps (Kommentare, Chat, Live Blog, Sidenotes):

1. App-Integration durchführen.
a. Erstellen Sie eine Sammlung mit dem sammlungmeta-Token.
b. Livefyre-Apps in Sites mithilfe der Embed-Codestruktur von Livefyre. js integrieren.

   * Weitere Informationen zur Verwendung der embed-Codestruktur von Livefyre. js finden Sie unter [App einbetten](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Informationen zum Integrieren der Kommentarapp finden Sie unter [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md).

   * Informationen zur Integration der Chat-App finden Sie [unter Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md).

   * Weitere Informationen zur Integration der Live Blog-App finden Sie unter [Live Blog](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md).

   * Weitere Informationen zur Integration der DOM-App finden Sie unter [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md).

1. Führen Sie die Authentifizierungsintegration durch.
a. Benutzerauthentifizierungstoken erstellen, um Benutzerdaten in Livefyre weiterzugeben und zu speichern.
b. Integration von Benutzern und Authentifizierungsplattformen von Drittanbietern Eine Liste der unterstützten Plattformen finden Sie unter [Identitätsintegration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

1. Führen Sie App-Anpassungen durch. App-Anpassungsoptionen, um Ihr Branding und Ihren Stil anzupassen und benutzerdefinierte Funktionen hinzuzufügen.

Erstellen einer Visualisierungsapp (Zuordnung, Medienwall, Trends, Karussell, Filmstreifen, Storify, Feature Card, Mosaic, Umfragen):

1. App-Integration durchführen.
a. Erstellen Sie eine Sammlung mit dem sammlungmeta-Token.
b. Livefyre-Apps in Sites mithilfe der Embed-Codestruktur von Livefyre. js integrieren. Weitere Informationen zur Verwendung der embed-Codestruktur von Livefyre. js finden Sie unter [App einbetten](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).

   * Informationen zum Integrieren der Map-App finden Sie unter [Zuordnung](/help/using/c-about-apps/c-map-app/c-map-app.md).

   * Informationen zum Integrieren der Medienwall-App finden Sie unter [Medienpinnwand](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md).

   * Weitere Informationen zur Integration der Trend-App finden Sie unter [Trends](/help/using/c-about-apps/c-trending-app/c-trending-app.md).

1. Führen Sie die Authentifizierungsintegration durch.
a. Benutzerauthentifizierungstoken erstellen, um Benutzerdaten an Livefyre weiterzugeben und zu speichern.
b. Integration von Benutzern und Authentifizierungsplattformen von Drittanbietern Eine Liste der unterstützten Plattformen finden Sie unter [Identitätsintegration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md).

>[!NOTE]
>
>Livefyre unterstützt Carousel, Filmstrip, Storify, Feature Card, Mosaic und Consulting Apps nicht mit Livefyre. js.
Integrieren Sie diese Apps mit dem [Vorgang "App](/help/using/c-about-apps/c-create-an-app.md) erstellen" .