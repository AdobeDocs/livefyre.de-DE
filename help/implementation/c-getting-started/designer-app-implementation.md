---
description: Verwenden Sie die Bootstrap- und Stream-API mit Livefyre-Apps.
title: App-Implementierung
uuid: null
exl-id: f1edef86-491d-4f8e-8ce5-f6e019d057ec
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# App-Implementierung {#appimplementation}

Verwendungsfall: Als Kunde möchte ich Livefyre mithilfe der Livefyre.js-Methode in mein Drittanbieter-CMS integrieren.

Es gibt drei Möglichkeiten, Livefyre in eine benutzerdefinierte AEM oder andere CMS-Komponenten wie WordPress, Sitecore oder DemandWare zu implementieren: Integration von Designer-App-Implementierung, -API, -Implementierung und Drittanbieter-Authentifizierung

## Designer-App-Implementierung {#designerapp}

Was: Einfachste und schnellste Integration einer Livefyre-App. Sie können einen benutzerdefinierten JavaScript-Einbettungscode entwerfen, konfigurieren und erstellen, um eine Liveyfre-App in wenigen Minuten auf einer Seite zu integrieren.

Wie: [Erstellen, Vorschau, Veröffentlichen und Einbetten einer Livefyre-App](/help/using/c-about-apps/c-create-an-app.md)

Beispiel: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre.js-Implementierung {#livefyrejsimp}

Was: [Livefyre.js](/help/implementation/c-livefyre.js.md) ist die Hauptbibliothek, die Apps und Auth auf einer Site aktiviert. Es definiert das globale `window.Livefyre`-Objekt und eine einzige öffentliche Methode, Livefyre.require, die zum Laden anderer Livefyre JavaScript-Bibliotheken verwendet werden kann, die beim Einbetten von Livefyre-Apps und bei der Integration mit externen User Auth-Plattformen helfen.

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

Informationen zu LiveCycle-Apps, die eine Authentifizierung erfordern, finden Sie unter [Identitätsintegration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) für Authentifizierungsplattformen von Drittanbietern.

## Kundenbeispiele {#customerexamples}

Die folgenden Kunden implementierten Livefyre mit CMS-Integrationen von Drittanbietern:

* [PGA-Medienwall](https://www.pgatour.com/social-hub.html)

* [TimeOut](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
