---
description: Was bei der Implementierung von Livefyre Studio zu erwarten ist.
seo-description: Was bei der Implementierung von Livefyre Studio zu erwarten ist.
seo-title: Implementierungsverfahren
solution: Experience Manager
title: Implementierungsverfahren
uuid: 9a0f394e-3467-47d1-9816-45e2130db440
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Implementierungsverfahren{#implementation-process}

Die Dauer der Implementierung von Livefyre hängt von Ihrer Implementierung und Ihrem Arbeitsbereich ab.

## Übersicht über die Livefyre-Netzwerkarchitektur {#section_dgj_l32_rbb}

Livefyre verwendet die folgenden Begriffe bei der Diskussion der Netzwerkarchitektur:

* Netzwerk. Die Domäne auf der höchsten Ebene, auf der Sie Livefyre verwenden möchten.
* Sites. Eine Subdomäne oder ein Site-Abschnitt, die Teil des Netzwerks ist.
* Apps. Eine Wiedergabe von Inhalten auf Ihrer Site. Inhalte werden in Apps visuell mit Visualisierungs-Apps (Mosaik, Karussell, Feature Card usw.) angezeigt. oder in Textformaten, mit Konvertierungs-Apps (Kommentare, Reviews, Chat usw.). Sie können eine oder mehrere Apps auf Ihre Sites setzen.
* Streams. Streams sind Filter, mit denen soziale Medien und andere Sites durchsucht werden, um Inhalte automatisch zur Moderation oder zur direkten Veröffentlichung in einer App zu erfassen.
* Inhalt (z. B. UGC, Kommentare). Was wird in den Apps angezeigt. Inhalte können visuell (z. B. ein Foto oder Video), nur Audio oder Text sein.

Das folgende Diagramm zeigt die Beziehung zwischen Netzwerk, Sites, Apps und Inhalt.

![](assets/network_site_architecture.png)

Sie haben Ihre eigene Livefyre-Instanz, die Ihr zentrales Dashboard zur Moderation von Inhalten, Verwaltung von Benutzern und mehr ist. Wenden Sie sich für den Zugriff auf Ihre Livefyre-Instanz an Ihren CSM.

## Integrationsschritte {#section_s2j_d2x_tz}

Zur Integration von Livefyre gibt es drei Hauptschritte:

* App-Integration

   Bei der Implementierung von Livefyre hängt der Implementierungsstil von Ihrem Anwendungsfall ab. Für [weitere Informationen zu jedem Implementierungstyp](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Authentifizierungsintegration

   Sie müssen Ihr bestehendes Benutzerverwaltungssystem in Livefyre für Konversations-Apps und andere Apps integrieren, für die eine Endbenutzerauthentifizierung auf Ihrer Site erforderlich ist. Wenn Sie derzeit kein Benutzerverwaltungstool verwenden, können Sie Livefyre Identity verwenden. Für [weitere Informationen über Livefyre Identity, was es ist und wie es einzurichten](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Anpassung

   Die Anpassung ist optional, aber die meisten Kunden passen Apps an ihre Marke an.

