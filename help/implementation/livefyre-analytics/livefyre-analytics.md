---
description: Analysieren Sie Benutzer-, Inhalts- und Moderatoraktivität für Ihre Site.
title: Analytics
exl-id: dc0545ec-2294-44ab-87c4-67eb30c3f787
source-git-commit: 9cd6617c4204b2c09787ea294227f640018928ce
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 1%

---

# Analytics{#analytics}

Analysieren Sie Benutzer-, Inhalts- und Moderatoraktivität für Ihre Site.

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

Analysieren Sie Benutzer-, Inhalts- und Moderatoraktivität für Ihre Site.

Livefyre Analytics bietet den Zugriff auf Ihre Netzwerkdaten in leicht lesbaren Dashboards für Konversationen, Moderation und Benutzerdaten. Verwenden Sie diese Dashboards, um Aktivitäten zu überwachen und schnelle Analysen auf Ihren Sites durchzuführen.

Dashboards können nach Site, Datum und Aktivität gefiltert werden. Verwenden Sie das Netzwerk-Pulldown oben links im Fenster, um eine anzuzeigende Site auszuwählen. Klicken Sie nach der Erstellung auf eine Spaltenüberschrift, um sie zu sortieren, oder bewegen Sie den Mauszeiger über das Diagramm, um genauere Informationen zu einem Datenpunkt zu erhalten.

Auf dieser Seite wird Folgendes beschrieben:

* Datumsbereich für Ihr Dashboard auswählen
* Anzeigen/Ausblenden der verfügbaren Aktivitäten
* Exportieren von Dashboard-Daten
* Das Dashboard &quot;Sammlungen&quot;
* Das Moderations-Dashboard
* Das Benutzer-Dashboard

>[!NOTE]
>
>Analytics unterstützt derzeit Aktivitäten, die von Livefyre Core Apps und Moderation stammen. Die meisten in diesen Dashboards enthaltenen Aktivitäten stehen auch über Livefyre-JavaScript-Ereignisse zur Verfügung, mit denen Sie Ihr eigenes benutzerdefiniertes Analysetool oder Analysetool von Drittanbietern nutzen können.

## Datumsbereich {#concept_798C438120E643B6BE262C9997DC87C4}

Klicken Sie auf die Datums-Pulldown-Liste, um einen anzuzeigenden Bereich auszuwählen. Verwenden Sie die Schnelldaten oder wählen Sie in den verfügbaren Kalendern ein Start- und ein Enddatum aus.

![](assets/analytics-date-range.png)

Quick Dates:

* **Heute:** Zeigt Daten von Mitternacht am Morgen des aktuellen Tages bis zur letzten vollständigen Stunde vor diesem Zeitpunkt an.
* **Gestern:** Zeigt die Daten der letzten 24 Stunden an.
* **7 Tage:** Zeigt die Daten der letzten sieben Tage an, mit Ausnahme des aktuellen Tages.
* **30 Tage:** Zeigt die Daten der letzten 30 Tage an, mit Ausnahme des aktuellen Tages.
* **Diese Woche:** Zeigt Daten von Mitternacht am Morgen des letzten Sonntags bis zur letzten vollständigen Stunde vor diesem Zeitpunkt an.
* **Diesen Monat:** Zeigt Daten von Mitternacht am Morgen des ersten Tages des aktuellen Monats bis zur letzten vollständigen Stunde vor diesem Zeitpunkt an.
* **Letzte Woche:** Zeigt die Daten der letzten Woche an.
* **Letzter Monat:** Zeigt die Daten des letzten Monats an.

## Ein-/Ausblenden von Aktivitäten {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

Aktivitäten sind Aktionen, die Benutzer auf Ihrer Site ausführen, einschließlich Kommentieren, Kennzeichnen, Freigeben und Moderieren. Verwenden Sie die **Aktivitäten ein-/ausblenden** -Pulldown zur Auswahl der Aktivitäten, die in Ihr Dashboard aufgenommen werden sollen.

>[!NOTE]
>
>Wenn Sie neue Ereignisse für den Filter auswählen, wird die Seite erneut gerendert, ohne die URL zu ändern.

![](assets/analytics-show-hide-activities.png)

Die verfügbaren Aktivitäten variieren je nach Dashboard-Typ und -Export und können Folgendes umfassen:

* **Beiträge:** Zeigt Daten von Mitternacht am Morgen des aktuellen Tages bis zur letzten vollständigen Stunde vor diesem Zeitpunkt an.
* **Antworten:** Zeigt die Daten der letzten 24 Stunden an.
* **&quot;Gefällt mir&quot;-Klicks:** Zeigt die Daten der letzten sieben Tage an, mit Ausnahme des aktuellen Tages.
* **Ungern:** Zeigt die Daten der letzten 30 Tage an, mit Ausnahme des aktuellen Tages.
* **Enthält Medien:** Zeigt Daten von Mitternacht am Morgen des letzten Sonntags bis zur letzten vollständigen Stunde vor diesem Zeitpunkt an.
* **Beitrag enthält Foto-Upload:** Zeigt Daten von Mitternacht am Morgen des ersten Tages des aktuellen Monats bis zur letzten vollständigen Stunde vor diesem Zeitpunkt an.
* **Beitrag enthält Link:** Zeigt die Daten der letzten Woche an.
* **Beitrag hat @mentions:** Zeigt die Daten des letzten Monats an.
* **Genehmigt:** Zeigt die Daten des letzten Monats an.
* **Bozo&#39;d:** Zeigt die Daten des letzten Monats an.
* **Gelöscht:** Zeigt die Daten des letzten Monats an.
* **Moderationssumme:** Zeigt die Daten des letzten Monats an.

## Exportieren von Dashboard-Daten {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

Verwenden Sie die **Export** Pulldown-Menü, um Ihre Dashboard-Daten als CSV-Datei zu exportieren.

* Tägliche Zusammenfassung (nur Sammlungen): exportiert die täglichen Tabellen der letzten vollständigen Woche für jede Sammlung.
* Tabellendaten: exportiert alle aggregierten Sammlungsdaten (alle Spalten und Zeilen im aktuellen Bericht).
* Rohdaten: exportiert alle einzelnen Ereignisse, die zur Erstellung des aktuellen aggregierten Berichts verwendet wurden.

>[!NOTE]
>
>Der Export dieser Berichte kann einige Minuten dauern. Alle Zeitstempel sind Unix-Zeit.

## Sammlungen {#concept_228D8E5553784DB8BABF3819A5FF0345}

Im Dashboard &quot;Sammlungen&quot;werden die Benutzeraktivitäten nach Sammlungen aufgelistet, sodass Sie Ihre am meisten (und am wenigsten ansprechenden) Inhalte ermitteln können. Jede aufgelistete Sammlung enthält einen Link zu der Seite, auf der sie zu finden ist.

![](assets/analytics-collections.png)

## Moderation {#concept_98689B1E804B43CEA21E3F456107CCD9}

Im Dashboard Moderation werden die Ereignisse nach Moderator aufgelistet, sodass Sie ihre Aktivität bewerten können. Verwenden Sie diesen Bericht, um Ihre aktivsten Moderatoren und deren gängigste Moderationsaktionen zu finden.

>[!NOTE]
>
>Die automatisierten Livefyre-Moderationsaktivitäten werden für den Moderatorennamen Livefyre System aufgeführt.

![](assets/analytics-moderation.png)

## Benutzer {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

Das Benutzer-Dashboard zeigt die Site-Aktivität nach Benutzer an, sodass Sie analysieren können, wie einzelne Benutzer mit Ihrer Site interagieren. Verwenden Sie dieses Dashboard, um Ihre aktivsten Benutzer auf Ihrer Site zu finden und die beliebtesten Site-Aktivitäten zu evaluieren.

![](assets/analytics-users.png)
