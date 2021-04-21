---
description: Was bei der Implementierung von Livefyre Studio zu erwarten ist.
title: Implementierungsverfahren
exl-id: 82bf8c09-946a-4be8-97bf-5b9868a4e031
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 3%

---

# Implementierungsverfahren{#implementation-process}

Die Dauer der Implementierung von Livefyre hängt von Ihrer Implementierung und Ihrem Arbeitsbereich ab.

## Übersicht über die Livefyre-Netzwerkarchitektur {#section_dgj_l32_rbb}

Livefyre verwendet die folgenden Begriffe bei der Diskussion der Netzwerkarchitektur:

* Netzwerk. Die Domäne auf der obersten Ebene, auf der Sie Livefyre verwenden möchten.
* Sites. Eine Subdomäne oder ein Site-Abschnitt, die Teil des Netzwerks ist.
* Apps. Eine Wiedergabe von Inhalten auf Ihrer Site. Inhalte werden in Apps visuell mit Visualisierungs-Apps (Mosaik, Karussell, Feature Card usw.) angezeigt. oder in Textformaten, mit Konvertierungs-Apps (Kommentare, Reviews, Chat usw.). Sie können eine oder mehrere Apps auf Ihre Sites setzen.
* Streams. Streams sind Filter, die nach sozialen Medien und anderen Sites suchen, um Inhalte automatisch zur Moderation oder zur direkten Veröffentlichung in einer App zu sammeln.
* Inhalt (z. B. UGC, Kommentare). Was wird in den Apps angezeigt. Inhalte können visuell (z. B. ein Foto oder Video), nur Audio oder Text sein.

Das folgende Diagramm zeigt die Beziehung zwischen Netzwerk, Sites, Apps und Inhalt.

![](assets/network_site_architecture.png)

Sie haben Ihre eigene Livefyre-Instanz, die Ihr zentrales Dashboard für die Moderation von Inhalten, die Benutzerverwaltung und mehr ist. Wenden Sie sich für den Zugriff auf Ihre Livefyre-Instanz an Ihren CSM.

## Integrationsschritte {#section_s2j_d2x_tz}

Zur Integration von Livefyre gibt es drei Hauptschritte:

* App-Integration

   Wenn Sie Livefyre implementieren, hängt der Implementierungsstil von Ihrem Anwendungsfall ab. Für [mehr zu jedem Implementierungstyp](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types).

* Authentifizierungs-Integration

   Sie müssen Ihr bestehendes Benutzerverwaltungssystem in Livefyre für Konversations-Apps und andere Apps integrieren, für die eine Endbenutzerauthentifizierung auf Ihrer Site erforderlich ist. Wenn Sie derzeit kein Benutzerverwaltungstool verwenden, können Sie Livefyre Identity verwenden. Für [weitere Informationen über Livefyre Identity, was es ist und wie es eingerichtet wird](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity).

* Anpassung

   Die Anpassung ist optional, aber die meisten Kunden passen Apps an ihre Marke an.
