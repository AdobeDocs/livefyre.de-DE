---
description: Sie können Stream-Regeln erstellen, die Inhalte aus RSS-Feeds abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte aus RSS-Feeds abrufen.
seo-title: RSS-Regeln
solution: Experience Manager
title: RSS-Regeln
uuid: 3 c 9 e 2069-bb 5-41 dc -8 b 35-6237642 a 538 a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# RSS-Regeln{#rss-rules}

Sie können Stream-Regeln erstellen, die Inhalte aus RSS-Feeds abrufen.

RSS-Streams werden alle 5 Minuten aktualisiert und suchen nach Inhalten, die in Livefyre aus den ersten 50 Elementen des Feeds nicht bereits vorhanden sind. Livefyre ignoriert alles über die ersten 50 Elemente im Feed.

Um RSS-Regeln zum Abrufen von Inhalten aus RSS-Feeds in Ihre App oder Ihren Ordner zu erstellen, können Sie nach Folgendem Filtern nach:

* **[!UICONTROL URL]** des RSS-Feeds.
* **[!UICONTROL Include recent items.]** Wenn dies festgelegt ist:

   * **[!UICONTROL Enabled]**, fügt Livefyre die ersten 50 Inhaltselemente im Feed unabhängig vom Veröffentlichungsdatum in den Stream ein.
   * **[!UICONTROL Disabled]**, fügt Livefyre die ersten 50 Inhaltselemente in Ihrem Feed mit einem Veröffentlichungsdatum hinzu, der mit dem Erstellungsdatum des Stream-Regels oder höher übereinstimmt.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Abrufen von Informationen aus dem Elementlink oder aus der XML.

**RSS-Regeln**

Livefyre parses RSS Feeds basierend auf den folgenden RSS-Spezifikationen:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [Medien-RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Atom-Feed](https://validator.w3.org/feed/docs/atom.html)

Livefyre liest keine Feeds, die diese Spezifikationen nicht berücksichtigen, und deren Inhalt wird nicht in Ihren Stream gezogen. Verwenden Sie den WC 3-Feed-Validierungsdienst, um die Syntax Ihres RSS-Feeds zu prüfen und sicherzustellen, dass er gültig ist.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
