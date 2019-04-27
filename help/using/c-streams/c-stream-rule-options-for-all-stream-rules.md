---
description: Diese Optionen gelten für alle Stream-Regeln aus allen sozialen Netzwerken oder Beiträgen.
seo-description: Diese Optionen gelten für alle Stream-Regeln aus allen sozialen Netzwerken oder Beiträgen.
seo-title: Stream-Regeloptionen für alle Stream-Regeln
solution: Experience Manager
title: Stream-Regeloptionen für alle Stream-Regeln
uuid: 4072 ee 83-31 e 7-4 de 6-918 c -134 b 8 b 8032 e 1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2

---


# Stream-Regeloptionen für alle Stream-Regeln{#stream-rule-options-for-all-stream-rules}

Diese Optionen gelten für alle Stream-Regeln aus allen sozialen Netzwerken oder Beiträgen.

Suchfunktionen für Text und Suchbegriffsfelder:

* Wenn Sie Suchbegriffe eingeben, verwendet Livefyre automatisch den booleschen Operator **ODER** , wenn Sie einzelne Wörter verwenden. Wenn Sie z. B. nach Beiträgen mit dem Wort *&quot;Cake* «oder *&quot; Rezept*«suchen möchten, geben Sie *&quot;cake&quot; ein*und geben Sie *dann Rezept* in das **[!UICONTROL keyword]** Feld ein.

* Sie können nach genauem Wortlaut suchen, indem Sie den exakten Wortlaut der Wortgruppe in Anführungszeichen setzen. Wenn Sie beispielsweise nach dem genauen Wortlaut der Wortgruppe *suchen*möchten, geben *Sie* in das **[!UICONTROL keyword]** Feld &quot;cke rezeppe&quot; ein.

* Sie können die booleschen und exakten Wortsuchen in einer Stream-Regel kombinieren. Sie können z. B. nach *Cake*, *Rezept*und *&quot;Cake Rezept&quot; suchen,* indem Sie die einzelnen Wortgruppen einzeln eingeben.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Wählen Sie eine der folgenden Optionen aus:

   * **[!UICONTROL All Content.]** Zulassen von Inhalten.
   * **[!UICONTROL Media Required.]** Nur Inhalte mit Bildern und Videos zulassen. (Für Instagram- und Facebook-Inhalte können Sie angeben **[!UICONTROL Photos]** oder **[!UICONTROL Videos]** nur).

* **[!UICONTROL Language]**. Wählen Sie die gewünschte Sprache aus. Englisch ist die Standardsprache.
* **[!UICONTROL Smart Tags]**. Wählen Sie die Tags aus, die zur Identifizierung von Inhalten verwendet werden sollen. Livefyre verwendet Computervision-Technologie zur Identifizierung von Fotos und Videos mit bestimmten intelligenten Tags, um diese Suche genauer zu gestalten. Verwenden Sie den **[!UICONTROL ANY]** Modifikator, um Inhalte mithilfe eines beliebigen Tags oder **[!UICONTROL ALL]** des Modifikators in den Stream zu filtern, um Inhalte in den Stream zu filtern, der alle Tags verwendet. Verwenden Sie das **[!UICONTROL Image contains none of these smart tags]** Feld, um Tags für Fotos einzugeben, die Inhalte enthalten, die nicht im Stream enthalten sein sollen. Diese Option funktioniert nicht für Textinhalte.

* **[!UICONTROL Products]**. Fügen Sie Produkt-Tags hinzu, um die Stream-Regel mit Produkten aus Ihrem Produktkatalog zu vergleichen.
* **[!UICONTROL Premoderate]**. Wählen Sie eine der folgenden Optionen aus:

   * **[!UICONTROL On]**. Vormoderieren aller eingehenden Regelinhalte. Sie können vormoderierte Inhalte im Abschnitt Streams von modq anzeigen. **[!UICONTROL On]** überschreibt die Einstellungen in den App-Einstellungen.
   * **[!UICONTROL Off]**. Stellen Sie keine eingehenden Regelinhalte vor. **[!UICONTROL Off]** überschreibt die Einstellungen in den App-Einstellungen.
   * **[!UICONTROL Inherited (Off)]**. Verwenden Sie die vormoderierten Einstellungen der Site (unter **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Wählen Sie eine der folgenden Optionen aus:
   * **[!UICONTROL Apply SAFE Rules]**. Wenden Sie alle sicheren Regeln auf diesen Stream an.
   * **[!UICONTROL Apply SAFE Rules for:]** Wählen Sie eine oder mehrere der Optionen aus, um SAFE Rules für diese Stream-Regel anzuwenden.
   * **[!UICONTROL Disable SAFE Rules]**. Wenden Sie keine SAFE-Regeln auf diesen Stream an.

Spezifische Stream-Regeloptionen für ein soziales Netzwerk oder einen Inhaltstyp finden Sie in der folgenden Dokumentation für das jeweilige soziale Netzwerk oder den entsprechenden Inhaltstyp:

* [Facebook-Seiten](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [E-Mail](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [Youtube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
