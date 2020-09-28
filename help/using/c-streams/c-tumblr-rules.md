---
description: Sie können Stream-Regeln erstellen, die Inhalte von Tumblr abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte von Tumblr abrufen.
seo-title: Tumblr-Regeln
solution: Experience Manager
title: Tumblr-Regeln
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Tumblr-Regeln{#tumblr-rules}

Sie können Stream-Regeln erstellen, die Inhalte von Tumblr abrufen.

Erstellen Sie Tumblr-Regeln basierend auf einem Tumblr-Blog und gefiltert nach Tag. Tumblr-Streams werden alle 5 Minuten aktualisiert und suchen nach Inhalten, die nicht bereits in Livefyre vorhanden sind, aus den ersten 20 Elementen im Feed. Livefyre ignoriert alles, was über die ersten 20 Elemente im Feed hinausgeht.

Um Tumblr-Regeln zu erstellen, um Inhalte aus Tumblr in Ihre App oder Ihren Ordner zu ziehen, können Sie nach folgenden Kriterien filtern:

* **[!UICONTROL Blog]**

   * Geben Sie die **[!UICONTROL Blog Name]** für den Tumblr-Blog ein. Geben Sie die URL (*employee.tumblr.com*) oder den Namen des Blogs (*Mitarbeiter*) ein.

   * Schließen Sie bis zu einem ein, **[!UICONTROL Tag]** um die Ergebnisse nach Beiträgen einschließlich eines angegebenen Tags zu filtern.

* **[!UICONTROL Include recent items.]** Wenn dies auf Folgendes festgelegt ist:

   * **[!UICONTROL Enabled]** hinzugefügt, fügt Livefyre die ersten 20 Inhaltselemente in Ihrem Feed unabhängig vom Veröffentlichungsdatum zum Stream hinzu.
   * **[!UICONTROL Disabled]** hinzugefügt, fügt Livefyre die ersten 20 Inhaltselemente in Ihrem Feed mit einem Veröffentlichungsdatum hinzu, das dem Erstellungsdatum der Stream-Regel oder höher entspricht.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
