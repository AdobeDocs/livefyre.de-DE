---
description: Versionshinweise für die Version vom 8. März 2018.
title: 8. März 2018
exl-id: 46d4a425-17e0-48a2-a596-5cc7163f9edd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 5%

---

# Samstag, 8. März 2018{#march}

Versionshinweise für die Version vom 8. März 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden Funktionen sind in der Produktionsversion dieser Version neu:

* **Löschen von Apps. **Es wurde die Möglichkeit hinzugefügt, Apps in Studio zu löschen, damit die Benutzer die App-Liste besser verwalten können. Wenn Sie eine App löschen, wird sie aus der Tabelle entfernt, jedoch nicht aus der Site. Die App empfängt weiterhin Inhalte aus einem Stream, wenn sie dafür konfiguriert ist.

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

## Produktionsversion

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Umfragen | Umfragen wurden geändert, um ausschließlich HTTPS zu verwenden. Bisher waren Umfragen weiterhin für HTTP zulässig. |
| Fehler | Studio | Es wurde ein Fehler behoben, der dazu führte, dass das modale Fenster, das Ankündigungen anzeigte, wenn Sie sich bei Studio anmelden, auf Bildschirmen mit niedriger Auflösung zu groß angezeigt wurde. |

## UAT-Version

| Art des Problems | Komponente | Versionshinweise |
|--- |--- |--- |
| Verbesserung | Filmstreifen | Die folgenden Barrierefreiheitsfunktionen für den Filmstreifen wurden aktualisiert: <br><ul><li>Links-/Rechts-Pfeile korrigiert von &lt;div> bis &lt;button> </li><li>Das Bild-Element der Vorschau wurde von einer weniger beschreibenden ARIA-Beschriftung &quot;Offenes angehängtes Foto&quot;zu einer Beschriftung geändert, die den Plattformnamen und den Beitragstext liest.</li></ul> |
| Fehler | Medienwall | Es wurde ein Problem in Media Pinnwand behoben, bei dem Tags nicht angeklickt werden konnten, wenn ein Instagram-Beitrag aus einer Stream-Regel hinzugefügt wurde. |
| Verbesserung | Medienwall | Die Barrierefreiheit von Media Wall wurde wie folgt verbessert: <br><ul><li>Das Öffnen und Schließen von Modellen über Tastaturbefehle verschiebt den Fokus nicht mehr zurück zum Anfang der Seite. Der Fokus bleibt stattdessen auf das Element, das zuletzt vor dem modalen Popup fokussiert wurde.</li><li>Schaltfläche &quot;Mehr laden&quot;kann mit der Tabulatortaste geöffnet und über die Eingabetaste ausgelöst werden.</li></ul> |
| Fehler | Rights Management | Es wurde ein Fehler behoben, durch den das Berechtigungsanforderungsmodell nach der Erteilung der Rechte für ein Instagram-Asset nicht angezeigt wurde. |
