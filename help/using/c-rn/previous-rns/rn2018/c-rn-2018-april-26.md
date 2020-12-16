---
description: Versionshinweise für die Version vom 26. April 2018.
seo-description: Versionshinweise für die Version vom 26. April 2018.
seo-title: 26. April 2018
solution: Experience Manager
title: 26. April 2018
uuid: a84ebe5c-40d5-43b5-a300-3e041ab22046
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 4%

---


# 26. April 2018{#april}

Versionshinweise für die Version vom 26. April 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden Funktionen sind in der Produktionsversion dieser Version neu:

* Es wurde eine neue Funktion hinzugefügt, mit der Kunden eine bestimmte Anzahl von Spalten für eine Medienwall konfigurieren können. Die Anzahl der Spalten, die Sie auswählen, erzwingt die Medienmauer unabhängig von der Größe in diese Spaltenanzahl. Andernfalls wird für die Anzahl der Spalten der Medienwall standardmäßig &quot;auto&quot;verwendet, wobei die Spalten an eine Zahl angepasst werden, die die Medienwall für die Bildschirmgröße optimiert.
* Im Media Pinnwand-Designer gibt es jetzt einen Umschalter, mit dem Sie die automatische Media Pinnwand-Animation deaktivieren können, die beim Laden einer Seite mit einer Media Pinnwand auftritt.
* Sie können jetzt den Vertrauensschwellenwert für Smart-Tags in Streams wählen. Wenn Sie den Präzisionswert (0-100) für Tags festlegen, können Sie die Genauigkeit der von uns abgerufenen Assets steuern.
* Es wurden Moderationsempfehlungen hinzugefügt. Livefyre scannt jetzt jeden Beitrag in kommentierenden Apps und sagt voraus, ob Sie ihn auf der Grundlage historischer Daten und maschineller Lernprozesse abschaffen werden. Diese Empfehlungen werden in ModQ angezeigt.
   * Benutzer können Moderationsempfehlungen deaktivieren, die es Benutzern ermöglichen, ModQ nach dem Inhalt zu filtern, den Livefyre für den Papierkorb hält.
   * Es wurde die Möglichkeit hinzugefügt, ModQ nach dem Moderations-Empfehlungs-Tag &quot;Papierkorb&quot;zu filtern.

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

## Produktionsversion

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Rights Management | Es wurde ein Problem behoben, bei dem Berechtigungsanforderungen für Assets nach dem Auffinden in einer Social-Suche nicht funktionierten. |
| Verbesserung | Streams | Der Streaming-Mechanismus wurde aktualisiert, mit dem Inhalte von Facebook gestreamt werden können, um einer von Facebook erstellten Back-End-Änderung zu entsprechen. |
| Fehler | UGC Commerce | Es wurde ein Problem behoben, bei dem die CTA-Schaltfläche &quot;Shop&quot;nicht in einer Mosaic- oder Filmstreifen-App oder einem Produktmodal angezeigt wurde, wenn der Mauszeiger über eine Karte mit einem Produkt bewegt wurde, wenn die CTA-Schaltfläche aktiviert ist. |
| Verbesserung | UGC Commerce | Es wurde ein Problem behoben, bei dem das UGC Commerce-Flag standardmäßig auf &quot;Aus&quot;anstatt auf &quot;Ein&quot;gesetzt wurde. |

## UAT-Version

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Bibliothek/Suche | Es wurde ein Problem behoben, durch das Videos nicht ordnungsgemäß hochgeladen wurden. |
| Verbesserung | Studio | Es wurde die Möglichkeit hinzugefügt, vorgeschlagene Wörter bei der Eingabe von Tag-Namen anzuzeigen. |

