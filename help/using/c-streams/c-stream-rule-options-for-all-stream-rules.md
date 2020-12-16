---
description: Diese Optionen gelten für alle Stream-Regeln aus allen sozialen Netzwerken oder Posting-Methoden.
seo-description: Diese Optionen gelten für alle Stream-Regeln aus allen sozialen Netzwerken oder Posting-Methoden.
seo-title: Stream-Regeloptionen für alle Stream-Regeln
solution: Experience Manager
title: Stream-Regeloptionen für alle Stream-Regeln
uuid: 4072ee83-31e7-4de6-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 1%

---


# Stream-Regeloptionen für alle Stream-Regeln{#stream-rule-options-for-all-stream-rules}

Diese Optionen gelten für alle Stream-Regeln aus allen sozialen Netzwerken oder Posting-Methoden.

Suchfunktionen für Text- und Suchbegriffsfelder:

* Wenn Sie Suchbegriffe eingeben, verwendet Livefyre automatisch den booleschen Operator **OR**, wenn es sich um einzelne Wörter handelt. Um beispielsweise nach Beiträgen mit dem Wort *cake* oder *recipe* zu suchen, geben Sie *cake* ein und geben Sie dann *recipe* in das Feld **[!UICONTROL keyword]** ein.

* Sie können nach genauen Wortgruppen suchen, indem Sie den genauen Wortlaut in Anführungszeichen setzen. Um beispielsweise nach dem genauen Wortlaut *cake recipe* zu suchen, geben Sie *&quot;cake recipe&quot;* in das Feld **[!UICONTROL keyword]** ein.

* Sie können die Suche nach booleschen und exakten Wortgruppen in einer Stream-Regel kombinieren. Sie können beispielsweise nach *cake*, *recipe* und *&quot;cake recipe&quot;* suchen, indem Sie die einzelnen Phrasen einzeln eingeben.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Wählen Sie eine der folgenden Optionen:

   * **[!UICONTROL All Content.]** Zulassen von Inhalten
   * **[!UICONTROL Media Required.]** Nur Inhalte mit Bildern und Videos zulassen (Für Instagram- und Facebook-Inhalte können Sie nur **[!UICONTROL Photos]** oder **[!UICONTROL Videos]** angeben.)

* **[!UICONTROL Language]**. Wählen Sie die Sprache, in der gesucht werden soll. Englisch ist die Standardsprache.
* **[!UICONTROL Smart Tags]**. Wählen Sie die Tags aus, die zur Identifizierung des Inhalts verwendet werden sollen. Livefyre nutzt die Technologie zur Computervisualisierung, um Fotos und Videos mit bestimmten Smart-Tags zu identifizieren, um diese Suche präziser zu gestalten. Verwenden Sie den Modifikator **[!UICONTROL ANY]**, um Inhalte mit einem beliebigen Tag in den Stream zu filtern, oder den Modifikator **[!UICONTROL ALL]**, um Inhalte in den Stream zu filtern, der alle Tags verwendet. Verwenden Sie das Feld **[!UICONTROL Image contains none of these smart tags]**, um Tags für Fotos einzugeben, die Inhalte enthalten, die Sie nicht im Stream haben möchten. Diese Option funktioniert nicht für Textinhalte.

* **[!UICONTROL Products]**. hinzufügen Produkt-Tags zur Übereinstimmung der Stream-Regel mit Produkten aus Ihrem Produktkatalog.
* **[!UICONTROL Premoderate]**. Wählen Sie eine der folgenden Optionen:

   * **[!UICONTROL On]**. Moderieren Sie den gesamten Inhalt der eingehenden Regel. Sie können vormoderierte Ansichten aus dem Streams-Bereich von ModQ erstellen. **[!UICONTROL On]** überschreibt die Einstellungen in den App-Einstellungen.
   * **[!UICONTROL Off]**. Keine Inhalten eingehender Regeln vormoderieren. **[!UICONTROL Off]** überschreibt die Einstellungen in den App-Einstellungen.
   * **[!UICONTROL Inherited (Off)]**. Verwenden Sie die voreingestellten Einstellungen der Site (unter **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Wählen Sie eine der folgenden Optionen:
   * **[!UICONTROL Apply SAFE Rules]**. Wenden Sie alle SAFE-Regeln auf diesen Stream an.
   * **[!UICONTROL Apply SAFE Rules for:]** Wählen Sie eine oder mehrere der Optionen aus, um SAFE-Regeln für diese Stream-Regel anzuwenden.
   * **[!UICONTROL Disable SAFE Rules]**. Wenden Sie keine SAFE-Regeln auf diesen Stream an.

Informationen zu Stream-Regeloptionen, die für ein soziales Netzwerk oder einen Inhaltstyp spezifisch sind, finden Sie in der folgenden Dokumentation zum jeweiligen sozialen Netzwerk oder Inhaltstyp:

* [Facebook-Seiten](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [E-Mail](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
