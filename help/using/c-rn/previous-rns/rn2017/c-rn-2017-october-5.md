---
description: Versionshinweise für die Version vom 5. Oktober 2017.
seo-description: Versionshinweise für die Version vom 5. Oktober 2017.
seo-title: 5. Oktober 2017
title: 5. Oktober 2017
uuid: 62e9e4ee-1644-4d22-9589-2e208a68aeb
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# October 5, 2017{#october}

Versionshinweise für die Version vom 5. Oktober 2017.

## Produktionsversion

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Livefyre-Identität | Kunden, die sich mit der Livefyre-Identität anmelden, hatten Probleme beim Anzeigen oder Aktualisieren ihrer Avatare beim Posten in Kommentierungs-Apps. Dies wurde jetzt behoben, da Avatare jetzt sichtbar und für die Aktualisierung verfügbar sind. |
| Fehler | Rights Management | Es wurde ein Fehler behoben, durch den lange Benutzernamen auf der Registerkarte "Rights Modal"angezeigt wurden. |
| Verbesserung | Streams | Es wurde die Möglichkeit hinzugefügt, die Tabulatortaste in einem Streams-Textfeld zu drücken, um einen Suchbegriff abzuschließen. |

## UAT-Version

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Verbesserung | Filmstreifen | Wenn ein Kunde eine Folio-App bereitstellt, wird neben der neu gestreuten UGC eine "neue"Beschriftung angezeigt, um sie schnell zu identifizieren. |
| Verbesserung | Filmstreifen | Filmstreifen ist eine brandneue Visualisierungs-App, die hauptsächlich dazu bestimmt ist, UGC in E-Commerce-Szenarien wie Produktseiten oder transaktionale Websites zu präsentieren. Der Filmstreifen richtet UGC horizontal aus, um jeweils als eine Filmrolle angezeigt zu werden. Endbenutzer können durch Klicken auf die Seitenpfeile durch den Filmstreifen navigieren, um durch den verfügbaren Inhalt zu blättern. |
| Verbesserung | Bibliothek | Dateien, die von einem Kunden in die Bibliothek hochgeladen werden, werden automatisch Rechte gewährt. Dies ist eine hilfreiche Funktion, wenn die Benutzer den Filter "Erforderliche Rechte gewährt"in ihren Apps aktiviert haben. |
| Verbesserung | Livefyre-Identität | Kunden können sich jetzt mit ihren Github-Anmeldeinformationen bei LIvefyre Identity anmelden und an unseren Kommentarapps teilnehmen. |
| Fehler | Rights Management | Es wurde ein Fehler behoben, durch den das Einfügen von Unicode-Zeichen in Rights Request-Nachrichten die Überprüfung umgangen werden konnte. |
| Verbesserung | SAFE | Kleinere Verbesserungen wurden zur SAFE-Spam-Erkennung hinzugefügt. |
| Fehler | Diensleistung | Für Benutzer ohne gültige E-Mails werden E-Mails erstellt. Es wurde ein Problem mit Produktionsprotokollen behoben, durch das das System keine E-Mails an diese Benutzer gesendet hat. |
| Verbesserung | Studio | Link zur Livefyre-Hilfe in der oberen Navigationsleiste aktualisiert. |
| Verbesserung | UGC Commerce | Als Kunde kann ich jetzt eine einzelne Livefyre-App erstellen (Mosaic, FilmStrip oder Media Wall) und sie auf mehreren Produktseiten einbetten, die die entsprechende UGC für jede Produktseite dynamisch filtert (Beispiel: UGC mit Schuhen für eine Schuhproduktseite). |
| Verbesserung | UGC Commerce | Kunden können nun einen Google-Produktkatalog manuell in das Livefyre-Studio hochladen, indem sie einen JSON-Dateiexport verwenden. Dadurch kann der Kunde UGC mit Produkten aus diesem Katalog verbinden und sie in unseren Commerce-fähigen Apps visualisieren. |
| Verbesserung | UGC Commerce | Kunden können auswählen, welche Produktordner beim Filtern ihrer E-Commerce-App nach Produkt-ID verwendet werden sollen. Zum Beispiel möchte ich, dass mein neuer Filmstreifen auf den Produktseiten für Damen- und Damenschuhe erscheint. Daher werde ich nur die Produktordner "Damenschuhe-Sammlung"und "Damenbeutel"auswählen. |
| Verbesserung | UGC Commerce | Livefyre-Kunden können nun die in ihren Apps veröffentlichten UGC nur dann filtern, wenn ihnen Rechte gewährt wurden. Beispielsweise kann ein Kunde eine Auswahl von Elementen kuratieren und veröffentlichen, aber diese Elemente werden nur dann in der App wiedergegeben, wenn der Autor ihnen Rechte erteilt hat. Dies ist besonders wichtig für E-Commerce-Nutzungsszenarien, in denen der UGC für kommerzielle Zwecke verwendet wird. |

