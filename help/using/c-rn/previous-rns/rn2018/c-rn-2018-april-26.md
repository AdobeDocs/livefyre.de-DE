---
description: Versionshinweise für die Version vom 26. April 2018.
seo-description: Versionshinweise für die Version vom 26. April 2018.
seo-title: 26. April 2018
solution: Experience Manager
title: 26. April 2018
uuid: a 84 ebe 5 c -40 d 5-43 b 5-a 300-3 e 041 ab 22046
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 26. April 2018{#april}

Versionshinweise für die Version vom 26. April 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden Funktionen sind in der Produktionsversion dieser Version neu:

* Es wurde eine neue Funktion hinzugefügt, mit der Kunden eine bestimmte Anzahl von Spalten für eine Medienpinnwand konfigurieren können. Die Anzahl der ausgewählten Spalten erzwingt die Medienpinnwand in dieser Anzahl von Spalten unabhängig von der Größe. Andernfalls ist die Anzahl der Medienwall-Spalten standardmäßig &quot;auto&quot; , wobei die Spalten an eine Zahl angepasst werden, die Media Wall für die Bildschirmgröße optimiert.
* Im Medienwall Designer gibt es jetzt einen Umschalter, mit dem Sie die automatische Medienpinnwand deaktivieren können, die auftritt, wenn eine Seite mit einer Medienpinnwand geladen wird.
* Sie können nun den Vertrauensschwellenwert für Smart-Tags in Streams auswählen. Wenn Sie die Genauigkeit (0-100) für Tags festlegen, können Sie die Genauigkeit der Assets steuern, die wir abrufen.
* Es wurden Moderationsempfehlungen hinzugefügt. Livefyre scannt jetzt jeden Beitrag in Kommentarapps und sagt vorhersagen, ob Sie ihn verschlüsseln oder nicht auf der Grundlage von historischen Daten und maschinellem Lernen. Diese Empfehlungen werden in modq angezeigt.
   * Benutzer können die Empfehlungen zur Moderation deaktivieren, wodurch Benutzer das modq nach dem von Livefyre erwarteten Inhalt filtern können.
   * Es wurde die Fähigkeit hinzugefügt, modq durch das Tag für die Moderation-Empfehlung, Papierkorb zu filtern.

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

## Produktionsversion

| **Ausgabentyp** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Bug | Rights Management | Es wurde ein Problem behoben, bei dem Rechte für Rechte nicht für Assets funktionierten, nachdem sie in einer Social-Suche gefunden wurden. |
| Verbesserung | Streams | Der Streaming-Mechanismus wurde aktualisiert, der Inhalte aus Facebook streamen und so einer von Facebook erstellten Back-End-Änderung entspricht. |
| Bug | UGC Commerce | Es wurde ein Problem behoben, durch das die CTA-Schaltfläche &quot;Shop&quot; nicht in einer Mosaic- oder Filmstrip-App angezeigt wurde, wenn die Maus über eine Karte mit einem Produkt bewegt wurde, wenn die CTA-Schaltfläche aktiviert wurde. |
| Verbesserung | UGC Commerce | Es wurde ein Problem behoben, durch das das UGC Commerce-Flag standardmäßig standardmäßig auf &quot;off&quot; gesetzt wurde. |

## UAT-Version

| **Ausgabentyp** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Bug | Bibliothek/Suche | Es wurde ein Problem behoben, durch das Videos nicht ordnungsgemäß hochgeladen wurden. |
| Verbesserung | Studio | Es wurde die Fähigkeit hinzugefügt, vorgeschlagene Wörter beim Eingeben in Tag-Namen anzuzeigen. |

