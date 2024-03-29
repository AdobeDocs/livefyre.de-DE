---
description: Versionshinweise für die Version vom 18. Januar 2018.
title: 18. Januar 2018
exl-id: aaf49dc9-64eb-4354-8bcb-04039fa25f10
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 7%

---

# 18. Januar 2018{#january}

Versionshinweise für die Version vom 18. Januar 2018.

## Produktionsversion

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Apps | Es wurde ein Fehler behoben, der dazu führte, dass Avatars nicht korrekt wiedergegeben wurden, wenn eine JPEG-Datei verwendet wurde. |
| Fehler | ModQ | Es wurde ein Fehler behoben, durch den S1-Kunden das Filtern nach Sammlungen in ModQ zulassen konnten. |
| Fehler | Streams | Es wurde ein Fehler behoben, der eine Stream-Regel beschädigte, wenn der Sprachfilter als &quot;none&quot;festgelegt wurde. |
| Fehler | Streams | Es wurde ein Fehler behoben, durch den YouTube-Stream-Regeln nicht gespeichert werden konnten. |
| Fehler | Streams | Behebung eines Fehlers, durch den Benutzer falsch formatierte Geoeinträge in Stream-Regeln erstellen und speichern konnten, wodurch der Stream fehlschlug. Jetzt können Benutzer nicht mehr falsch formatierte Geo-Tags speichern. |
| Fehler | Studio | Es wurde ein Problem behoben, das verhinderte, dass sich einige Benutzer bei Livefyre anmelden konnten. |

## UAT-Version

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Bibliothek | Sicherheitsfehlerbehebung. Alle Authentifizierungsaufrufe werden jetzt über das HTTPS-Protokoll statt über HTTP ausgeführt. |
| Verbesserung | Smart-Tags | Streaming-Inhalte werden jetzt automatisch von Adobe Sensei mit intelligenten Tags versehen, wenn sie in einem Ordner gespeichert oder in einer App veröffentlicht werden. |
| Fehler | Streams | Es wurde ein Problem behoben, bei dem Instagram-Stream-Regeln japanische Zeichen nicht erkannten. |
| Verbesserung | Streams | Kunden können jetzt die logischen Operatoren ( ANY, ALL, NOT) verwenden, um detaillierte Smart-Tag-Filter in Streams zu erstellen, die viel genauere Inhalte kuratieren. Wenn ich zum Beispiel das Hashtag #himalyas verwende, kann ich nur Bilder anzeigen, die &quot;schneebedeckte&quot; &quot;Berge&quot; enthalten. |
| Fehler | Studio | Korrektur eines Fehlers, der Sonderzeichen in Namen als HTML anzeigte. |
