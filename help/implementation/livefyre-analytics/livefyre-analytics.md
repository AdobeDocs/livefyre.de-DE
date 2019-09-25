---
description: Analysieren Sie Benutzer-, Inhalts- und Moderatoraktivität für Ihre Site.
seo-description: Analysieren Sie Benutzer-, Inhalts- und Moderatoraktivität für Ihre Site.
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9d8a1b0478
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Analytics{#analytics}

Analysieren Sie Benutzer-, Inhalts- und Moderatoraktivität für Ihre Site.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analysieren Sie Benutzer-, Inhalts- und Moderatoraktivität für Ihre Site.

Livefyre Analytics bietet Zugriff auf Ihre Netzwerkdaten in leicht lesbaren Dashboards für Konversationen, Moderation und Benutzerdaten. Verwenden Sie diese Dashboards, um die Aktivität zu überwachen und schnelle Analysen auf Ihrer Site(n) durchzuführen.

Dashboards können nach Website, Datum und Aktivität gefiltert werden. Verwenden Sie den Netzwerk-Pulldown oben links im Fenster, um eine anzuzeigende Site auszuwählen. Klicken Sie nach der Generierung auf eine Spaltenüberschrift, um zu sortieren, oder halten Sie den Mauszeiger über das Diagramm, um genauere Informationen zu einem Datenpunkt anzuzeigen.

Diese Seite beschreibt:

* Auswählen eines [Datumsbereichs](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange) für Ihr Dashboard
* [Verfügbare Aktivitäten ein-/ausblenden](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [Exportieren von Dashboard-Daten](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [Das Sammlungs-Dashboard](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [Das Moderations-Dashboard](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [Das Benutzer-Dashboard](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Analytics unterstützt derzeit Aktivitäten, die von Livefyre-Core-Apps und -Moderationen stammen. Die meisten in diesen Dashboards enthaltenen Aktivitäten stehen auch über [Livefyre-JavaScript-Ereignisse](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/)zur Verfügung, mit denen Sie Ihr eigenes benutzerdefiniertes oder Drittanbieter-Analysetool aktivieren können.

## Datumsbereich {#concept_798C438120E643B6BE262C9997DC87C4}

Klicken Sie auf den Datumsabruf, um einen anzuzeigenden Bereich auszuwählen. Verwenden Sie die QuickDate oder wählen Sie ein Start- und Enddatum aus den bereitgestellten Kalendern.

![](assets/analytics-date-range.png)

Quick Dates:

* **** Heute: Zeigt Daten von Mitternacht am Morgen des aktuellen Tages bis zur letzten vollständigen Stunde vor diesem Moment an.
* **** Gestern: Zeigt die Daten der letzten 24 Stunden an.
* **** 7 Tage: Zeigt die Daten der letzten 7 Tage an, nicht einschließlich heute.
* **** 30 Tage: Zeigt die Daten der letzten 30 Tage an, nicht einschließlich heute.
* **** Diese Woche: Zeigt Daten von Mitternacht am Morgen des letzten Sonntags bis zur letzten vollständigen Stunde vor diesem Moment an.
* **** Diesen Monat: Zeigt Daten von Mitternacht am Morgen des ersten Tages des aktuellen Monats bis zur letzten vollständigen Stunde vor diesem Moment an.
* **** Letzte Woche: Zeigt die Daten der letzten Woche an.
* **** Letzter Monat: Zeigt die Daten des letzten Monats an.

## Anzeigen/Ausblenden von Aktivitäten {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Aktivitäten sind Aktionen, die Benutzer auf Ihrer Site ausführen, einschließlich Kommentierung, Kennzeichnung, Freigabe und Moderation. Verwenden Sie den Pulldown "Aktivitäten **einblenden/ausblenden"** , um Aktivitäten auszuwählen, die Sie in Ihr Dashboard aufnehmen möchten.

>[!NOTE]
>
>Wenn Sie neue Ereignisse für den Filter auswählen, wird die Seite erneut gerendert, ohne die URL zu ändern.

![](assets/analytics-show-hide-activities.png)

Die verfügbaren Aktivitäten variieren je nach Dashboard-Typ und Export und können Folgendes umfassen:

* **** Beiträge: Zeigt Daten von Mitternacht am Morgen des aktuellen Tages bis zur letzten vollständigen Stunde vor diesem Moment an.
* **** Antworten: Zeigt die Daten der letzten 24 Stunden an.
* **** "Gefällt mir"-Klicks: Zeigt die Daten der letzten 7 Tage an, nicht einschließlich heute.
* **** Unbeliebt: Zeigt die Daten der letzten 30 Tage an, nicht einschließlich heute.
* **** Enthält Medien: Zeigt Daten von Mitternacht am Morgen des letzten Sonntags bis zur letzten vollständigen Stunde vor diesem Moment an.
* **** Beitrag enthält Foto-Upload: Zeigt Daten von Mitternacht am Morgen des ersten Tages des aktuellen Monats bis zur letzten vollständigen Stunde vor diesem Moment an.
* **** Beitrag hat Link: Zeigt die Daten der letzten Woche an.
* **** Beitrag hat @Erwähnungen: Zeigt die Daten des letzten Monats an.
* **** Genehmigt: Zeigt die Daten des letzten Monats an.
* **** Bozo'd: Zeigt die Daten des letzten Monats an.
* **** Gestrichelt: Zeigt die Daten des letzten Monats an.
* **** Moderation gesamt: Zeigt die Daten des letzten Monats an.

## Exportieren von Dashboard-Daten {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Verwenden Sie das Pulldown-Menü " **Exportieren** ", um Ihre Dashboard-Daten als CSV-Datei zu exportieren.

* Tägliches Digest (nur Sammlungen): exportiert die täglichen Tabellen der letzten vollständigen Woche für jede Sammlung.
* Tabellendaten: exportiert alle aggregierten Sammlungsdaten (alle Spalten und alle Zeilen im aktuellen Bericht).
* Rohdaten: exportiert alle einzelnen Ereignisse, die zur Erstellung des aktuellen Rollup-Berichts verwendet wurden.

>[!NOTE]
>
>Der Export dieser Berichte kann einige Minuten dauern. Alle Zeitstempel sind Unix-Zeit.

## Sammlungen {#concept_228D8E5553784DB8BABF3819A5FF0345}

Das Sammlungs-Dashboard listet die Benutzeraktivität nach Sammlung auf, sodass Sie die am meisten (und am wenigsten interessanten) Inhalte ermitteln können. Jede aufgelistete Sammlung enthält einen Link zur Seite, auf der sie gefunden werden kann.

![](assets/analytics-collections.png)

## Moderation {#concept_98689B1E804B43CEA21E3F456107CCD9}

Das Dashboard "Moderation"listet Ereignisse nach Moderator auf, sodass Sie ihre Aktivität bewerten können. Verwenden Sie diesen Bericht, um Ihre aktivsten Moderatoren und die häufigsten Moderationsaktionen zu finden.

>[!NOTE]
>
>Automatisierte Livefyre-Moderationsaktivitäten werden für den Moderatornamen Livefyre System aufgelistet.

![](assets/analytics-moderation.png)

## Benutzer {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

Das Benutzer-Dashboard zeigt die Site-Aktivität nach Benutzer an, sodass Sie analysieren können, wie einzelne Benutzer mit Ihrer Site interagieren. Verwenden Sie dieses Dashboard, um Ihre aktivsten Benutzer auf Ihrer Site zu finden und die beliebtesten Site-Aktivitäten zu bewerten.

![](assets/analytics-users.png)

