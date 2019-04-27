---
description: Verwenden Sie Bootstrap und Stream-API mit Livefyre-Apps.
seo-description: Verwenden Sie Bootstrap und Stream-API mit Livefyre-Apps.
seo-title: App-Implementierung
solution: Experience Manager
title: App-Implementierung
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# App-Implementierung {#appimplementation}

Anwendungsfall: Als Kunde möchte ich mithilfe der Livefyre. js-Methode Livefyre in meine Drittanbieter-CMS integrieren.

Es gibt drei Möglichkeiten, Livefyre in einer benutzerdefinierten AEM-Komponente oder anderen CMS-Beispielen wie &quot;wordpress&quot; ,&quot; Sitecore&quot; oder &quot;demandware&quot; zu implementieren: Designer App-Implementierung, API, Implementierung und Drittanbieter-Authentifizierungsintegration.

## Designer App-Implementierung {#designerapp}

Was: Einfachste und schnellste Möglichkeit zur Integration einer Livefyre-App. Sie können einen benutzerdefinierten Javascript-Einbettungscode entwerfen, konfigurieren und generieren, um eine Liveyfre-App in Minuten zu integrieren.

Wie: [Erstellen, Anzeigen, Veröffentlichen und Einbetten einer Livefyre-App](/help/using/c-about-apps/c-create-an-app.md)

Beispiel: [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre. js-Implementierung {#livefyrejsimp}

Was: [Livefyre. js](/help/implementation/c-livefyre.js.md) ist die zentrale Bibliothek, die Apps und Auth auf einer Site anzeigt. Es definiert das globale `window.Livefyre` Objekt und eine einzelne öffentliche Methode, Livefyre. Anforderung, die zum Laden anderer Livefyre-javascript-Bibliotheken verwendet werden kann, die beim Einbetten von Livefyre-Apps und der Integration in die Plattformen der Benutzerauthentifizierung von Drittanbietern hilfreich sind.

Wie:

* [Erstellen einer Sammlung mit dem collectionmeta-Token](/help/implementation/t-create-a-collectionmeta-token.md)

* Apps mit App-Integrationen in Drittanbieter-CMS integrieren

Beispiele:

* Kommentare-App: [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* Review-App: [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Medienpinnwand: [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* Erweiterte Anpassungen mit dem SDK finden Sie unter streamhub sdks.

## API-Implementierung {#apiimplementation}

Zum Erstellen benutzerdefinierter Erlebnisse und Datenvisualisierungen können Livefyre-Apps von Grund auf neu erstellt werden, indem Livefyre und soziale Daten mithilfe der Bootstrap- und Stream-API genutzt werden.

## Integration von Drittanbieter-Authentifizierung {#thirdpartyauth}

Informationen zu Livefyre-Apps, die Authentifizierung erfordern, finden Sie unter [Identitätsintegration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) für Authentifizierungsplattformen von Drittanbietern.

## Kundenbeispiele {#customerexamples}

Die folgenden Kunden implementierten Livefyre mit CMS-Integrationen von Drittanbietern:

* [PGA-Tour Medienwall](https://www.pgatour.com/social-hub.html)

* [Timeout](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
