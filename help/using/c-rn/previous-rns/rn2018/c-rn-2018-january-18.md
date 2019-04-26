---
description: Versionshinweise für die Version vom 18. Januar 2018.
seo-description: Versionshinweise für die Version vom 18. Januar 2018.
seo-title: 18. Januar 2018
solution: Experience Manager
title: 18. Januar 2018
uuid: 8141 f 431-c 154-4 c 8 f-bbcd-b 7 c 712 fe 5 f 7 d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# 18. Januar 2018{#january}

Versionshinweise für die Version vom 18. Januar 2018.

## Produktionsversion

| **Ausgabentyp** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Bug | Apps | Fehler behoben, der verhinderte, dass Avatare richtig dargestellt wurden, wenn eine JPEG-Datei verwendet wurde. |
| Bug | Modq | Es wurde ein Fehler für S 1-Kunden behoben, um die Filterung nach Sammlungen in modq zuzulassen. |
| Bug | Streams | Es wurde ein Fehler behoben, durch den eine Stream-Regel beschädigt wurde, wenn der Sprachfilter als "Keine" festgelegt wurde. |
| Bug | Streams | Es wurde ein Fehler behoben, durch den Youtube-Stream-Regeln nicht gespeichert werden konnten. |
| Bug | Streams | Behebt einen Fehler, durch den Benutzer in Stream-Regeln falsch formatierte Geo-Einträge erstellen und speichern können, wodurch der Stream fehlschlägt. Nun können Benutzer keine falsch formatierten Geo-Tags mehr speichern. |
| Bug | Studio | Es wurde ein Problem behoben, durch das einige Benutzer sich nicht bei Livefyre anmelden konnten. |

## UAT-Version

| **Ausgabentyp** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Bug | Bibliothek | Fehlerbehebung für Sicherheitsfehler. Alle Authentifizierungsaufrufe werden jetzt über das HTTPS-Protokoll statt über HTTP ausgeführt. |
| Verbesserung | Smart Tags | Gestreamter Inhalt wird jetzt automatisch von Adobe Sensei getaggt, da er in einem Ordner gespeichert oder in einer App veröffentlicht wird. |
| Bug | Streams | Korrektur des Problems, bei dem Instagram-Stream-Regeln japanische Zeichen nicht erkannten. |
| Verbesserung | Streams | Kunden können jetzt die logischen Operatoren (ANY, ALL, NOT) verwenden, um detaillierte Smart-Tag-Filter in Streams zu erstellen, die wesentlich genauere Inhalte kuratieren. Wenn ich beispielsweise Hashtag # himalyas verwende, kann ich nur Bilder anzeigen, die "Snowy" -Berge enthalten. |
| Bug | Studio | Fehler behoben, durch den Sonderzeichen in Namen als HTML angezeigt wurden. |

