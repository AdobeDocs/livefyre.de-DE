---
description: Versionshinweise für die Version vom 8. März 2018.
seo-description: Versionshinweise für die Version vom 8. März 2018.
seo-title: 8. März 2018
solution: Experience Manager
title: 8. März 2018
uuid: 4 ed 67147-0837-4 d 5 e -8 e 99-532 a 4278 bcce
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 8. März 2018{#march}

Versionshinweise für die Version vom 8. März 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden Funktionen sind in der Produktionsversion dieser Version neu:

* ** Löschen von Apps. ** Es wurde die Fähigkeit hinzugefügt, Apps in Studio zu löschen, damit Benutzer die App-Liste besser verwalten können. Durch Löschen einer App wird sie aus der Tabelle entfernt, die App wird jedoch nicht von Ihrer Site entfernt. Die App erhält weiterhin Inhalte aus einem Stream, wenn diese konfiguriert ist.

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

## Produktionsversion

| **Ausgabentyp** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Bug | Umfragen | Die Umfrage wurde geändert, um HTTPS exklusiv zu verwenden. Zuvor waren Umfragen weiterhin mit HTTP zulässig. |
| Bug | Studio | Es wurde ein Problem behoben, durch das das modale Fenster, das Ankündigungen anzeigt, wenn Sie sich bei Studio anmelden, zu groß auf Bildschirmen mit niedriger Auflösung angezeigt wurde. |

## UAT-Version

| Ausgabentyp | Komponente | Versionshinweise |
|--- |--- |--- |
| Verbesserung | Filmstreifen | Die folgenden Barrierefreiheitsfunktionen für Filmstreifen wurden aktualisiert: <br><ul><li>Links/Rechtspfeile korrigiert von &lt; div &gt; auf &lt; Schaltfläche &gt; </li><li>Vorschaubild wurde von einer weniger beschreibenden ARIA-Beschriftung von &quot;Angehängtes Foto öffnen&quot; in eine Beschriftung geändert, die den Namen der Plattform und des Beitragstexts liest.</li></ul> |
| Bug | Medienpinnwand | Es wurde ein Problem in der Medienpinnwand behoben, bei dem Tags nicht anklickbar waren, wenn ein Instagram-Beitrag aus einer Stream-Regel hinzugefügt wurde. |
| Verbesserung | Medienpinnwand | Verbesserte Barrierefreiheit von Medien-Pinnwänden: <br><ul><li>Beim Öffnen und Schließen von Modalen über Tastaturbefehle wird der Fokus nicht mehr an den Anfang der Seite verschoben. Fokus bleibt stattdessen auf dem Element, das zuletzt fokussiert ist, vor dem modalen Popup.</li><li>Die Schaltfläche &quot;Mehr laden&quot; kann mit der Tastatur eingeblendet und mit der Tastatur ausgelöst werden.</li></ul> |
| Bug | Rights Management | Es wurde ein Fehler behoben, der dazu führte, dass die Rechte für Rechte nach dem Erteilen der Rechte für ein Instagram-Asset nicht mehr angezeigt wurden. |

