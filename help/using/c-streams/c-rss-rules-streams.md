---
description: Sie können Stream-Regeln erstellen, die Inhalte aus RSS-Feeds abrufen.
title: RSS-Regeln
exl-id: bfb3bbad-ab26-451e-b540-d6c41f54dc31
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# RSS-Regeln{#rss-rules}

Sie können Stream-Regeln erstellen, die Inhalte aus RSS-Feeds abrufen.

RSS-Streams werden alle 5 Minuten aktualisiert und suchen nach Inhalten, die in Livefyre nicht bereits von den ersten 50 Elementen im Feed vorhanden sind. Livefyre ignoriert alles, was über die ersten 50 Elemente im Feed hinausgeht.

Um RSS-Regeln zu erstellen, mit denen Inhalte aus RSS-Feeds in Ihre App oder Ihren Ordner gezogen werden, können Sie nach Folgendem filtern:

* **[!UICONTROL URL]** des RSS-Dienstes.
* **[!UICONTROL Include recent items.]** Wenn dies auf Folgendes festgelegt ist:

   * **[!UICONTROL Enabled]** hinzugefügt, fügt Livefyre die ersten 50 Inhaltselemente in Ihrem Feed unabhängig vom Veröffentlichungsdatum zum Stream hinzu.
   * **[!UICONTROL Disabled]** hinzugefügt, fügt Livefyre die ersten 50 Inhaltselemente in Ihrem Feed mit einem Veröffentlichungsdatum hinzu, das dem Erstellungsdatum der Stream-Regel oder höher entspricht.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Ziehen Sie Informationen aus dem Element-Link oder aus der XML.

**RSS-Regeln**

Livefyre analysiert RSS-Dienste auf der Grundlage der folgenden RSS-Spezifikationen:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [Media RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Atom-Feed](https://validator.w3.org/feed/docs/atom.html)

Livefyre liest keine Feeds, die nicht diesen Spezifikationen entsprechen, und ihr Inhalt wird nicht in Ihren Stream geladen. Verwenden Sie den WC3-Feed-Validierungsdienst, um die Syntax Ihres RSS-Dienstes zu überprüfen und sicherzustellen, dass er gültig ist.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
