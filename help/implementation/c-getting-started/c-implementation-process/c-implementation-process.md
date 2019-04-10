---
description: Was soll bei der Implementierung von Livefyre Studio erwartet werden
seo-description: Was soll bei der Implementierung von Livefyre Studio erwartet werden
seo-title: Implementierungsprozess
solution: Experience Manager
title: Implementierungsprozess
uuid: 9 a 0 f 394 e -3467-47 d 1-9816-45 e 2130 db 440
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Implementierungsprozess{#implementation-process}

Der Zeitraum zur Implementierung von Livefyre hängt von Ihrer Implementierung und Ihrem Umfang ab.

## Übersicht über Livefyre-Netzwerkarchitektur {#section_dgj_l32_rbb}

Livefyre verwendet die folgenden Begriffe in der Diskussion über die Netzwerkarchitektur:

* Netzwerk. Die Domäne auf höchster Ebene, auf der Livefyre verwendet werden soll.
* Sites. Eine Subdomäne oder ein Site-Abschnitt, der Teil des Netzwerks ist.
* Apps. Wiedergabe von Inhalten auf Ihrer Site. Inhalte werden in Apps visuell angezeigt. Verwenden Sie dazu Visualisierungsapps (Mosaic, Karussell, Feature Card usw.). oder im Textformat verwenden, indem Sie Unterhaltungsapps (Kommentare, Reviews, Chat usw.) verwenden. Sie können eine oder mehrere Apps auf Ihren Sites platzieren.
* Streams. Streams sind Filter, die soziale Medien und andere Sites suchen, um Inhalte für die Moderation oder direkte Veröffentlichung in einer App automatisch zu erfassen.
* Inhalt (z. B. UGC, Kommentare) Was in den Apps angezeigt wird. Inhalte können visuell (z. B. ein Foto oder Video), nur Audio oder Text sein.

Das folgende Diagramm zeigt die Beziehung zwischen Netzwerk, Sites, Apps und Inhalten.

![](assets/network_site_architecture.png)

Sie haben Ihre eigene Livefyre-Instanz, die Ihr zentrales Dashboard für die Moderation von Inhalten, die Verwaltung von Benutzern und vieles mehr ist. Wenden Sie sich an Ihren CSM, um auf Ihre Livefyre-Instanz zuzugreifen.

## Integrationsschritte {#section_s2j_d2x_tz}

Es gibt drei Hauptschritte zur Integration von Livefyre:

* App-Integration

   Wenn Sie Livefyre implementieren, hängt der Stil der Implementierung von Ihrem Verwendungsfall ab. Für [jeden Implementierungstyp](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Authentifizierungsintegration

   Sie müssen Ihr vorhandenes Benutzerverwaltungssystem in Livefyre für Unterhaltungen und andere Apps integrieren, die eine Endbenutzerauthentifizierung auf Ihrer Site erfordern. Wenn Sie derzeit kein Tool zur Benutzerverwaltung verwenden, können Sie die Livefyre-Identität verwenden. Weitere [Informationen zu Livefyre-Identität finden Sie unter und wie sie eingerichtet](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity)werden.

* Anpassung

   Die Anpassung ist optional, die meisten Kunden passen Apps jedoch an ihre Marke an.

