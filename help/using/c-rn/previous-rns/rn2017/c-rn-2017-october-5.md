---
description: Versionshinweise für die Version vom 5. Oktober 2017.
title: 5. Oktober 2017
exl-id: 6e39a86e-82dd-47ff-ad68-2b483f8b1921
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 4%

---

# 5. Oktober 2017{#october}

Versionshinweise für die Version vom 5. Oktober 2017.

## Produktionsversion

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Livefyre-Identität | Kunden, die sich mit der Livefyre-Identität anmelden, hatten Probleme beim Anzeigen oder Aktualisieren ihrer Avatare beim Posten in Kommentierungs-Apps. Dies wurde jetzt behoben, da Avatare jetzt sichtbar und für die Aktualisierung verfügbar sind. |
| Fehler | Rights Management | Es wurde ein Fehler behoben, durch den lange Benutzernamen auf der Registerkarte &quot;Rights Modal&quot;angezeigt wurden. |
| Verbesserung | Streams | Es wurde die Möglichkeit hinzugefügt, die Tabulatortaste in einem Streams-Textfeld zu drücken, um einen Suchbegriff abzuschließen. |

## UAT-Version

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Verbesserung | Filmstreifen | Wenn ein Kunde eine Folio-App bereitstellt, wird neben der neu gestreuten UGC eine &quot;neue&quot;Beschriftung angezeigt, um sie schnell zu identifizieren. |
| Verbesserung | Filmstreifen | Filmstreifen ist eine brandneue Visualisierungs-App, die hauptsächlich dazu bestimmt ist, UGC in E-Commerce-Szenarien wie Produktseiten oder transaktionale Websites zu präsentieren. Der Filmstreifen richtet UGC horizontal aus, um jeweils als eine Filmrolle angezeigt zu werden. Endbenutzer können durch Klicken auf die Seitenpfeile durch den Filmstreifen navigieren, um durch den verfügbaren Inhalt zu blättern. |
| Verbesserung | Bibliothek | Dateien, die von einem Kunden in die Bibliothek hochgeladen werden, werden automatisch Rechte gewährt. Dies ist eine hilfreiche Funktion, wenn die Benutzer den Filter &quot;Benötigte Rechte gewährt&quot;in ihren Apps aktiviert haben. |
| Verbesserung | Livefyre-Identität | Kunden können sich jetzt mit ihren Github-Anmeldeinformationen bei LIvefyre Identity anmelden und an unseren Kommentarapps teilnehmen. |
| Fehler | Rights Management | Es wurde ein Fehler behoben, durch den das Einfügen von Unicode-Zeichen in Rights Request-Nachrichten die Überprüfung umgangen werden konnte. |
| Verbesserung | SAFE | Kleinere Verbesserungen wurden zur SAFE-Spam-Erkennung hinzugefügt. |
| Fehler | Diensleistung | Für Benutzer ohne gültige E-Mails werden E-Mails erstellt. Es wurde ein Problem mit Produktionsprotokollen behoben, durch das das System keine E-Mails an diese Benutzer gesendet hat. |
| Verbesserung | Studio | Der Link zur Livefyre-Hilfe in der oberen Navigationsleiste wurde aktualisiert. |
| Verbesserung | UGC Commerce | Als Kunde kann ich jetzt eine einzelne Livefyre-App erstellen (Mosaic, FilmStrip oder Media Wall) und sie auf mehreren Produktseiten einbetten, die dynamisch die entsprechende UGC für jede Produktseite (z. B. UGC mit Schuhen für eine Schuhproduktseite) Filter. |
| Verbesserung | UGC Commerce | Kunden können nun einen Google-Produktkatalog manuell in das Livefyre-Studio hochladen, indem sie einen JSON-Dateiexport verwenden. Dadurch kann der Kunde UGC mit Produkten aus diesem Katalog verbinden und sie in unseren Commerce-fähigen Apps visualisieren. |
| Verbesserung | UGC Commerce | Kunden können auswählen, welche Produktordner beim Filtern ihrer E-Commerce-App nach Produkt-ID verwendet werden sollen. Zum Beispiel möchte ich, dass mein neuer Filmstreifen auf den Produktseiten für Damen- und Damenschuhe erscheint. Daher werde ich nur die Produktordner &quot;Damenschuhe-Sammlung&quot;und &quot;Damenbeutel&quot;auswählen. |
| Verbesserung | UGC Commerce | Livefyre-Kunden können nun die in ihren Apps veröffentlichten UGC nur dann filtern, wenn ihnen Rechte gewährt wurden. Beispielsweise kann ein Kunde eine Auswahl von Elementen kuratieren und veröffentlichen, aber diese Elemente werden nur dann in der App wiedergegeben, wenn der Autor ihnen Rechte erteilt hat. Dies ist besonders wichtig für E-Commerce-Nutzungsszenarien, in denen der UGC für kommerzielle Zwecke verwendet wird. |
