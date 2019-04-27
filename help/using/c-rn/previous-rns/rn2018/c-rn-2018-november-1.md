---
description: Versionshinweise für die Version vom 1. November 2018.
seo-description: Versionshinweise für die Version vom 1. November 2018.
seo-title: 1. November 2018
solution: Experience Manager
title: 1. November 2018
uuid: ed 1 a 3 bf 1-b 3 f 1-4746-8462-07283723 ba 62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 1. November 2018{#november}

Versionshinweise für die Version vom 1. November 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden neuen Funktionen wurden in der Produktionsversion dieser Version veröffentlicht:

* Video-Smart-Tags

   Nutzen Sie die Vorteile der Technik für Computercomputervision, powered by Adobe Sensei, um Videoinhalte automatisch zu taggen, wenn Sie sie in der Bibliothek speichern. Mit intelligenten Tags können Sie UGC effektiver verwalten, aber auch sehr präzise Kuratierungsregeln (Streams) erstellen, die Inhalte basierend auf dem Inhalt des Videos erfassen, nicht nur den Text, sondern eine erhebliche Bemühung, unerwünschte Inhalte zu moderieren.

   Funktionsdetails:

   * Intelligente Tags werden automatisch zu Videos hinzugefügt, die aus Social-Suchen, Streams und hochgeladenen Videodateien in der Bibliothek gewonnen wurden. Anzeigen von Tags in den Asset-Details für ein einzelnes Video
   * Taggen von Videos in den Formaten. MP 4. MOV und AVI
   * Taggen von Videos bis zu 60 Sekunden oder 50 MB
   * Für Videos gelten zwei Kategorien von intelligenten Tags: Funktionen (Tiere, Objekte, Orte usw.) und Aktionen (laufen, laufen, sintieren usw.)
   Weitere Informationen finden [Sie unter Smart Tags.](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Instagram-Ratenbeschränkung

   Instagram hat die Anzahl der Anforderungen geändert, die ein beliebiges Unternehmen, das die Instagram-API verwendet, einschließlich Livefyre, von 5.000 Anfragen pro Stunde pro Token bis zu 200 Anforderungen pro Stunde vornehmen kann. Dies wird als *Ratenbeschränkung bezeichnet*. Weitere Informationen finden Sie unter [Instagram-Rateneinschränkung](/help/using/c-streams/c-instagram-rate-limiting.md).

* Audiodateien in der Bibliothek

   Sie können jetzt die folgenden Funktionen für Audiodateien aus dem Bibliothek-Bedienfeld ausführen:

   * Durchsuchen
   * Vorschau
   * Importieren
   * Filtern nach Audiodateien
   * Drag &amp; Drop von Dateien in Designer

## Probleme {#section_ehw_ndt_wcb}

In der Produktionsversion dieser Version wurden keine neuen Probleme behoben. Siehe [Abschnitt oben](#c_rn/section_syx_mdt_wcb).

## UAT-Version {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

Die Probleme in den folgenden Tabellen wurden in der UAT-Version dieser Version behoben.

| **Ausgabentyp** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Verbesserung | GDPR | Alle älteren Kunden innerhalb von Analytics zugewiesenen Daten werden gelöscht. |
| Bug | Bibliothek | Es wurde ein Problem behoben, durch das ein in die Bibliothek hochgeladenes Video, das dann in der Asset-Details angezeigt wurde, nicht richtig angezeigt wurde. |
| Bug | Mosaik | Es wurde ein Problem behoben, durch das Mosaic das letzte Inhaltselement aus einem Instagram-Karussell als Miniaturansicht anstelle einer Karte anzeigte. |
| Bug | Social Search | Es wurde ein Problem behoben, durch das die Instagram Social Search nicht wie erwartet funktionierte. |

