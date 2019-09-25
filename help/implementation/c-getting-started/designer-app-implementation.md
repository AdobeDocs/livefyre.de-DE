---
description: Verwenden Sie Bootstrap- und Stream-API mit Livefyre-Apps.
seo-description: Verwenden Sie Bootstrap- und Stream-API mit Livefyre-Apps.
seo-title: App-Implementierung
solution: Experience Manager
title: App-Implementierung
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# App-Implementierung {#appimplementation}

Verwendungsfall: Als Kunde möchte ich Livefyre mithilfe der Livefyre.js-Methode in mein Drittanbieter-CMS integrieren.

Es gibt drei Möglichkeiten, Livefyre in eine benutzerdefinierte AEM-Komponente oder andere CMS-Komponenten wie WordPress, SiteCore oder DemandWare zu implementieren: Integration von Designer-App-Implementierung, -API, -Implementierung und Drittanbieter-Authentifizierung

## Designer-App-Implementierung {#designerapp}

Was: Einfachste und schnellste Integration einer Livefyre-App. Sie können einen benutzerdefinierten JavaScript-Einbettungscode entwerfen, konfigurieren und erstellen, um eine Liveyfre-App in wenigen Minuten auf einer Seite zu integrieren.

Wie: Erstellen, Anzeigen einer Vorschau, Veröffentlichen und Einbetten einer Livefyre-App [](/help/using/c-about-apps/c-create-an-app.md)

Beispiel: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre.js-Implementierung {#livefyrejsimp}

Was: [Livefyre.js](/help/implementation/c-livefyre.js.md) ist die Kernbibliothek, mit der Apps und Auth auf einer Site ausgeführt werden. Es definiert das globale `window.Livefyre` Objekt und eine einzige öffentliche Methode, Livefyre.require, die zum Laden anderer Livefyre JavaScript-Bibliotheken verwendet werden kann, die beim Einbetten von Livefyre-Apps und bei der Integration mit Auth-Plattformen von Drittanbietern helfen.

Wie:

* [Erstellen einer Sammlung mit dem CollectionMeta-Token](/help/implementation/t-create-a-collectionmeta-token.md)

* Integrieren von Apps in CMS von Drittanbietern mithilfe von App-Integrationen

Beispiele:

* Kommentar-App: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Reviews App: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Medienwall: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Informationen zu erweiterten Anpassungen mit dem SDK finden Sie unter StreamHub-SDKs.

## API-Implementierung {#apiimplementation}

Zur Erstellung benutzerdefinierter Erlebnisse und Datenvisualisierungen können Livefyre-Apps von Grund auf erstellt werden, indem Livefyre- und Social-Daten mit der Bootstrap- und Stream-API genutzt werden.

## Integration der Drittanbieter-Authentifizierung {#thirdpartyauth}

Informationen zu Livefyre-Apps, die eine Authentifizierung erfordern, finden Sie unter [Identitätsintegration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) für Authentifizierungsplattformen von Drittanbietern.

## Kundenbeispiele {#customerexamples}

Die folgenden Kunden implementierten Livefyre mit CMS-Integrationen von Drittanbietern:

* [PGA-Medienwall](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
