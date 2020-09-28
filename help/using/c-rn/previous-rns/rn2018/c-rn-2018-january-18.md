---
description: Versionshinweise für die Version vom 18. Januar 2018.
seo-description: Versionshinweise für die Version vom 18. Januar 2018.
seo-title: 18. Januar 2018
solution: Experience Manager
title: 18. Januar 2018
uuid: 8141f431-c154-4c8f-bcd-b7c712fe5f7d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# January 18, 2018{#january}

Versionshinweise für die Version vom 18. Januar 2018.

## Produktionsversion

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Apps | Es wurde ein Fehler behoben, der dazu führte, dass Avatars nicht korrekt wiedergegeben wurden, wenn eine JPEG-Datei verwendet wurde. |
| Fehler | ModQ | Es wurde ein Fehler behoben, durch den S1-Kunden das Filtern nach Sammlungen in ModQ zulassen konnten. |
| Fehler | Streams | Es wurde ein Fehler behoben, der eine Stream-Regel beschädigte, wenn der Sprachfilter als "none"festgelegt wurde. |
| Fehler | Streams | Es wurde ein Fehler behoben, durch den YouTube-Stream-Regeln nicht gespeichert werden konnten. |
| Fehler | Streams | Behebung eines Fehlers, durch den Benutzer falsch formatierte Geoeinträge in Stream-Regeln erstellen und speichern konnten, wodurch der Stream fehlschlug. Jetzt können Benutzer nicht mehr falsch formatierte Geo-Tags speichern. |
| Fehler | Studio | Es wurde ein Problem behoben, das verhinderte, dass sich einige Benutzer bei Livefyre anmelden konnten. |

## UAT-Version

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Bibliothek | Sicherheitsfehlerbehebung Alle Authentifizierungsaufrufe werden jetzt über das HTTPS-Protokoll statt über HTTP ausgeführt. |
| Verbesserung | Smart-Tags | Streaming-Inhalte werden jetzt automatisch von Adobe Sensei mit Tags versehen, da sie in einem Ordner gespeichert oder in einer App veröffentlicht werden. |
| Fehler | Streams | Korrektur des Problems, bei dem Instagram-Stream-Regeln japanische Zeichen nicht erkannten. |
| Verbesserung | Streams | Kunden können jetzt die logischen Operatoren ( ANY, ALL, NOT) verwenden, um detaillierte Smart-Tag-Filter in Streams zu erstellen, die sehr viel genauere Inhalte kuratieren. Wenn ich zum Beispiel das Hashtag #himalyas verwende, kann ich nur Bilder anzeigen, die "schneebedeckte" "Berge" enthalten. |
| Fehler | Studio | Korrektur eines Fehlers, der Sonderzeichen in Namen als HTML anzeigte. |

