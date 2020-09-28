---
description: Versionshinweise für die Version vom 1. November 2018.
seo-description: Versionshinweise für die Version vom 1. November 2018.
seo-title: 1. November 2018
solution: Experience Manager
title: 1. November 2018
uuid: ed1a3bf1-b3f1-4746-8462-07283723ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 1. November 2018{#november}

Versionshinweise für die Version vom 1. November 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden neuen Funktionen wurden in der Produktionsversion dieser Version veröffentlicht:

* Smart-Tags für Videos

   Nutzen Sie modernste Computer-Vision-Technologie mit Adobe Sensei, um Videoinhalte automatisch zu taggen, wenn Sie sie in der Bibliothek speichern. Intelligente Tags helfen Ihnen, UGC effektiver zu verwalten, erstellen aber auch extrem präzise Kurationsregeln (Streams), die Inhalte auf der Grundlage des Inhalts des Videos erfassen, nicht nur des Textes, was Ihnen erhebliche Anstrengungen bei der Moderation unerwünschter Inhalte ermöglicht.

   Funktionsdetails:

   * Smart-Tags werden automatisch zu Videos hinzugefügt, die aus der Social-Suche, Streams und hochgeladenen Videodateien in der Bibliothek gewonnen wurden. Anzeigen von Tags in den Asset-Details für ein einzelnes Video
   * Tags von Videos im Format MP4, MOV und AVI
   * Tags von Videos bis zu 60 Sekunden oder 50 MB
   * Für Videos gelten zwei Kategorien von Smarttags: Funktionen (Tiere, Objekte, Orte usw.) und Aktionen (Laufen, Gehen, Singen usw.)
   For more information see [Smart Tags](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Begrenzung der Instagram-Rate

   Instagram hat die Anzahl der Anfragen geändert, die ein Unternehmen, das die Instagram-API verwendet, einschließlich Livefyre, von 5.000 Anfragen pro Stunde pro Token auf 200 Anfragen pro Token stellen kann. Dies wird als *Ratenbegrenzung* bezeichnet. Weitere Informationen finden Sie unter Einschränkungen der [Instagram-Rate](/help/using/c-streams/c-instagram-rate-limiting.md).

* Audiodateien in der Bibliothek

   Sie können jetzt die folgenden Funktionen für Audiodateien aus dem Bibliotheksbedienfeld ausführen:

   * Durchsuchen
   * Vorschau
   * Importieren
   * Filtern nach Audiodateien
   * Drag &amp; Drop von Dateien in den Designer

## Probleme {#section_ehw_ndt_wcb}

In der Produktionsversion dieser Version wurden keine neuen Probleme behoben. Siehe [Abschnitt oben](#c_rn/section_syx_mdt_wcb).

## UAT-Version {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

Die Probleme in den folgenden Tabellen wurden in der UAT-Version dieser Version behoben.

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Verbesserung | GDPR | Alle Daten, die früheren Kunden in Analytics zugewiesen wurden, werden gelöscht. |
| Fehler | Bibliothek | Es wurde ein Problem behoben, bei dem ein Video, das in die Bibliothek hochgeladen und dann im Detail angezeigt wurde, nicht korrekt angezeigt wurde. |
| Fehler | Mosaik | Es wurde ein Problem behoben, bei dem ein Mosaic das letzte Inhaltselement eines Instagram-Karussells als Miniaturansicht anstatt als Karte anzeigte. |
| Fehler | Social-Suche | Es wurde ein Problem behoben, bei dem die Suche in sozialen Instagram nicht wie erwartet funktionierte. |

