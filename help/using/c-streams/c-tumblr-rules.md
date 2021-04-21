---
description: Sie können Stream-Regeln erstellen, die Inhalte von Tumblr abrufen.
title: Tumblr-Regeln
exl-id: 5d49b266-6d1f-4ec2-8891-5e98fcab14a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Tumblr Rules{#tumblr-rules}

Sie können Stream-Regeln erstellen, die Inhalte von Tumblr abrufen.

Erstellen Sie Tumblr-Regeln basierend auf einem Tumblr-Blog und gefiltert nach Tag. Tumblr-Streams werden alle 5 Minuten aktualisiert und suchen nach Inhalten, die nicht bereits in Livefyre vorhanden sind, aus den ersten 20 Elementen im Feed. Livefyre ignoriert alles, was über die ersten 20 Elemente im Feed hinausgeht.

Um Tumblr-Regeln zu erstellen, um Inhalte aus Tumblr in Ihre App oder Ihren Ordner zu ziehen, können Sie nach folgenden Kriterien filtern:

* **[!UICONTROL Blog]**

   * Geben Sie das **[!UICONTROL Blog Name]** für das Tumblr-Blog ein. Geben Sie die URL (*employee.tumblr.com*) oder den Namen des Blogs (*employee*) ein.

   * Schließen Sie bis zu einem **[!UICONTROL Tag]** ein, um die Ergebnisse nach Beiträgen einschließlich eines angegebenen Tags zu filtern.

* **[!UICONTROL Include recent items.]** Wenn dies auf Folgendes festgelegt ist:

   * **[!UICONTROL Enabled]** hinzugefügt, fügt Livefyre die ersten 20 Inhaltselemente in Ihrem Feed unabhängig vom Veröffentlichungsdatum zum Stream hinzu.
   * **[!UICONTROL Disabled]** hinzugefügt, fügt Livefyre die ersten 20 Inhaltselemente in Ihrem Feed mit einem Veröffentlichungsdatum hinzu, das dem Erstellungsdatum der Stream-Regel oder höher entspricht.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
