---
description: Sie können Stream-Regeln erstellen, die Inhalte von Tumblr abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte von Tumblr abrufen.
seo-title: Tumblr-Regeln
solution: Experience Manager
title: Tumblr-Regeln
uuid: fe 9601 ab-aa 5 e -48 c 6-a 5 bf -5543 c 179 cb 90
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Tumblr-Regeln{#tumblr-rules}

Sie können Stream-Regeln erstellen, die Inhalte von Tumblr abrufen.

Tumblr-Regeln basierend auf einem Tumblr-Blog erstellen und nach Tag gefiltert werden. Tumblr-Streams werden alle 5 Minuten aktualisiert und suchen nach Inhalten, die in Livefyre aus den ersten 20 Elementen des Feeds nicht bereits vorhanden sind. Livefyre ignoriert alles über die ersten 20 Elemente im Feed.

Um Tumblr-Regeln zum Abrufen von Inhalten von Tumblr in Ihre App oder zum Ordner zu erstellen, können Sie nach Folgendem Filtern nach:

* **[!UICONTROL Blog]**

   * Geben Sie den **[!UICONTROL Blog Name]** Tumblr-Blog ein. Geben Sie die URL (*staff.tumblr.com*) oder den Namen des Blogs (*Personal*) ein.

   * Schließen Sie bis zu einem **[!UICONTROL Tag]** Wert ein, um Ergebnisse nach Beiträgen einschließlich eines angegebenen Tags zu filtern.

* **[!UICONTROL Include recent items.]** Wenn dies festgelegt ist:

   * **[!UICONTROL Enabled]**, fügt Livefyre die ersten 20 Inhaltselemente im Feed unabhängig vom Veröffentlichungsdatum in den Stream ein.
   * **[!UICONTROL Disabled]**, fügt Livefyre die ersten 20 Inhaltselemente in Ihrem Feed mit einem Veröffentlichungsdatum hinzu, der mit dem Erstellungsdatum des Stream-Regels oder höher übereinstimmt.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
