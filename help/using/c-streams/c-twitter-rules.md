---
description: Sie können Stream-Regeln erstellen, die Inhalte aus Twitter abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte aus Twitter abrufen.
seo-title: Twitter-Regeln
solution: Experience Manager
title: Twitter-Regeln
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Twitter-Regeln{#twitter-rules}

You can create Stream rules that pull content from Twitter.

Erstellen Sie Twitter-Regeln basierend auf Hashtags, Keywords, @mentions oder Autor.

Wenn Sie **[!UICONTROL Words]** und eine **[!UICONTROL Username]** Regel hinzufügen, werden Inhalte zurückgegeben, die beide Einträge enthalten.

>[!NOTE]
>
>Livefyre adheres to Twitter display guidelines, and customers are responsible for adhering to these guidelines as well. Weitere Informationen finden Sie in der Dokumentation zu den [Anzeigeanforderungen](https://dev.twitter.com/terms/display-requirements)von Twitter.

Um Twitter-Regeln zu erstellen, mit denen Sie Inhalte aus Twitter-Feeds in Ihre App oder Ihren Ordner ziehen können, können Sie nach Folgendem filtern:

* **[!UICONTROL Keywords]**
   * Geben Sie ein, **[!UICONTROL Keywords]** um in Ihren Twitter-Stream eingeschlossen oder ausgeschlossen zu werden. Wenn Sie Werte für die Felder **[!UICONTROL Contains any of these words]** und **[!UICONTROL Does not contain any of these words]** die Felder angeben, werden Tweets zurückgegeben, die den ersten und den zweiten enthalten. Es können mehrere Werte für ein einzelnes Feld eingegeben werden, die Ergebnisse zurückgeben, die einen der Werte enthalten. Wenn Sie den Booleschen Operator UND verwenden möchten, um nach Tweets mit zwei oder mehr Wörtern zu suchen, verwenden Sie zwei kaufmännische *&amp;&amp;* Zeichen, um die beiden Wörter zu trennen.
   * For example, entering **[!UICONTROL Contains any of these words]** keywords Giants, Posey, and **[!UICONTROL Does not contain any of these words]** keyword Dodger, will return all Tweets which include the word *Giants* or *Posey* and do not include the word *Dodger*.
Um nach Tweets zu suchen, die die Wörter *Giants* und *Posey* enthalten, geben Sie "Giants &amp;&amp; Posey"ein. Diese Funktion wird nur für die **[!UICONTROL Contains any of these words]** und **[!UICONTROL Does not contain any of these words]** Felder in Twitter-Regeln unterstützt.

* **[!UICONTROL Hashtags]**.
   * Geben Sie ein, **[!UICONTROL Hashtags]** um in Ihren Twitter-Stream eingeschlossen oder ausgeschlossen zu werden. Specifying values for both the  and  fields will return Tweets which contain hashtags in the first field, and do not contain hashtags in the second field. **[!UICONTROL Contains any of these words]****[!UICONTROL Does not contain any of these words]** Sie können mehrere Werte für ein einzelnes Feld eingeben. Der Stream gibt Ergebnisse zurück, die einen der Werte enthalten.

* **[!UICONTROL Usernames]**
   * Geben Sie ein **[!UICONTROL @mentions]** oder **[!UICONTROL authors]** ziehen Sie in den Stream oder schließen Sie ihn aus dem Stream. Verwenden Sie die Kontrollkästchen, um festzulegen, ob auch ausgewählte Autoren einbezogen werden sollen **[!UICONTROL Retweets]** oder **[!UICONTROL replies]** nicht.
   >[!NOTE]
   >
   >Sie können Autoren ein- oder ausschließen. Sie können diese beiden Felder nicht zu einer einzigen Twitter-Regel kombinieren.

* **[!UICONTROL Minimum number of followers.]** Wählen Sie die Mindestanzahl der Follower aus, die der Benutzer aus den Beiträgen abrufen muss.
* **[!UICONTROL Location]**

   * Geben Sie den Ort (Stadt, Postleitzahl, Adresse oder Geocode im allgemeinen Breiten-/Längengradformat (+/- 90, +/- 180)) ein. Geben Sie eine Position ein, um ein Dropdown-Menü mit Empfehlungen anzuzeigen. Select a location from the drop down. Auf der Karte wird ein Pin dieser Position angezeigt. Adjust the slider to select a radius of one mile to 25 miles for each location. Wenn Sie keinen Radius auswählen, wählt Livefyre automatisch einen Standardwert von acht Meilen.
   >[!NOTE]
   >
   >For both fields, distance will be calculated from the center of the input location.

   * Sie können mehr als eine Position und einen Radius hinzufügen. You can delete a location by clicking the X next to the name of a location in the box.
   * Combine the  and  fields to pull content within locations in the  field, but not near the locations in the  field.**[!UICONTROL Is near this location]****[!UICONTROL Is not near this location]****[!UICONTROL Is near this location]****[!UICONTROL Is not near this location]**


* **[!UICONTROL Additional Filters]**
   * Use Additional Filters to further refine your Twitter Rule. Legen Sie fest, ob Sie:
      * Include  to the targeted Tweets (If the stream becomes high velocity, this feature will automatically be disabled.).**[!UICONTROL Replies]**
      * Include Tweets from **[!UICONTROL Verified Twitter accounts only.]**
      * Include , or , or **[!UICONTROL All Content]****[!UICONTROL Vines Only]****[!UICONTROL Images Only.]**
      * Include only Tweets which originate from accounts with the selected  (any, 100, 500, 1000, 10,000, or 100,000).**[!UICONTROL Minimum number of followers]**

For additional Stream rule options for all Stream rules, see Stream Rule Options for All Stream Rules.[](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)
