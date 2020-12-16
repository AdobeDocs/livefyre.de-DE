---
description: Sie können Stream-Regeln erstellen, die Inhalte aus Twitter abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte aus Twitter abrufen.
seo-title: Twitter-Regeln
solution: Experience Manager
title: Twitter-Regeln
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---


# Twitter-Regeln{#twitter-rules}

Sie können Stream-Regeln erstellen, die Inhalte aus Twitter abrufen.

Erstellen Sie Twitter-Regeln basierend auf Hashtags, Keywords, @mentions oder Autor.

Wenn Sie **[!UICONTROL Words]** und **[!UICONTROL Username]** für Ihre Regel hinzufügen, werden Inhalte zurückgegeben, die beide Einträge enthalten.

>[!NOTE]
>
>Livefyre befolgt die Twitter-Anzeigenrichtlinien und Kunden sind auch für die Einhaltung dieser Richtlinien verantwortlich. Weitere Informationen finden Sie in der Dokumentation zu Twitter unter den [Anzeigeanforderungen](https://dev.twitter.com/terms/display-requirements).

Um Twitter-Regeln zu erstellen, mit denen Sie Inhalte aus Twitter-Feeds in Ihre App oder Ihren Ordner ziehen können, können Sie nach Folgendem filtern:

* **[!UICONTROL Keywords]**
   * Geben Sie **[!UICONTROL Keywords]** ein, um in Ihren Twitter-Stream eingeschlossen oder ausgeschlossen zu werden. Wenn Sie Werte für die Felder **[!UICONTROL Contains any of these words]** und **[!UICONTROL Does not contain any of these words]** angeben, werden Tweets zurückgegeben, die das erste und das zweite enthalten. Es können mehrere Werte für ein einzelnes Feld eingegeben werden, die Ergebnisse zurückgeben, die einen der Werte enthalten. Wenn Sie den Booleschen Operator UND verwenden möchten, um nach Tweets mit zwei oder mehr Wörtern zu suchen, verwenden Sie zwei kaufmännische Und (*&amp;*), um die beiden Wörter zu trennen.
   * Wenn Sie z. B. **[!UICONTROL Contains any of these words]** die Suchbegriffe Giants, Posey und **[!UICONTROL Does not contain any of these words]** Suchbegriff Dodger eingeben, werden alle Tweets zurückgegeben, die das Wort *Giants* oder *Posey* enthalten und das Wort *Dodger* nicht enthalten.
Um nach Tweets zu suchen, die die Wörter *Giants* und *Posey* enthalten, geben Sie &quot;Giants &amp;&amp; Posey&quot;ein. Diese Funktion wird nur für die Felder **[!UICONTROL Contains any of these words]** und **[!UICONTROL Does not contain any of these words]** in Twitter-Regeln unterstützt.

* **[!UICONTROL Hashtags]**.
   * Geben Sie **[!UICONTROL Hashtags]** ein, um in Ihren Twitter-Stream eingeschlossen oder ausgeschlossen zu werden. Wenn Werte für die Felder **[!UICONTROL Contains any of these words]** und **[!UICONTROL Does not contain any of these words]** angegeben werden, werden Tweets zurückgegeben, die Hashtags im ersten Feld enthalten, keine Hashtags im zweiten Feld. Sie können mehrere Werte für ein einzelnes Feld eingeben. Der Stream gibt Ergebnisse zurück, die einen der Werte enthalten.

* **[!UICONTROL Usernames]**
   * Geben Sie **[!UICONTROL @mentions]** oder **[!UICONTROL authors]** ein, um in den Stream zu ziehen, oder schließen Sie ihn vom Stream aus. Verwenden Sie die Kontrollkästchen, um festzulegen, ob **[!UICONTROL Retweets]** oder **[!UICONTROL replies]** von ausgewählten Autoren ebenfalls einbezogen werden soll.

   >[!NOTE]
   >
   >Sie können Autoren ein- oder ausschließen. Sie können diese beiden Felder nicht zu einer einzigen Twitter-Regel kombinieren.

* **[!UICONTROL Minimum number of followers.]** Wählen Sie die Mindestanzahl Follower-Anzahlen aus, die Benutzer aus ihren Beiträgen abrufen müssen.
* **[!UICONTROL Location]**

   * Geben Sie den Ort (Stadt, Postleitzahl, Adresse oder Geocode im allgemeinen Breiten-/Längengradformat (+/- 90, +/- 180)) ein. Geben Sie eine Position ein, um ein Dropdown-Menü mit Empfehlungen anzuzeigen. Wählen Sie eine Position aus der Dropdownliste. Auf der Karte wird ein Pin dieser Position angezeigt. Passen Sie den Schieberegler an, um einen Radius von einer Meile bis zu 25 Meilen für jede Position auszuwählen. Wenn Sie keinen Radius auswählen, wählt Livefyre automatisch einen Standardwert von acht Meilen.
   >[!NOTE]
   >
   >Für beide Felder wird der Abstand vom Mittelpunkt des Eingabeorts berechnet.

   * Sie können mehr als eine Position und einen Radius hinzufügen. Sie können eine Position löschen, indem Sie auf das X neben dem Namen einer Position im Feld klicken.
   * Kombinieren Sie die Felder **[!UICONTROL Is near this location]** und **[!UICONTROL Is not near this location]**, um Inhalte an Positionen im Feld **[!UICONTROL Is near this location]**, jedoch nicht in der Nähe der Positionen im Feld **[!UICONTROL Is not near this location]** abzurufen.


* **[!UICONTROL Additional Filters]**
   * Verwenden Sie zusätzliche Filter, um Ihre Twitter-Regel weiter zu verfeinern. Legen Sie fest, ob Sie Folgendes tun:
      * Schließen Sie **[!UICONTROL Replies]** in die zielgerichteten Tweets ein (wird der Stream mit hoher Geschwindigkeit, wird diese Funktion automatisch deaktiviert).
      * Tweets von **[!UICONTROL Verified Twitter accounts only.]** einschließen
      * Schließen Sie **[!UICONTROL All Content]** oder **[!UICONTROL Vines Only]** oder **[!UICONTROL Images Only.]** ein.
      * Schließen Sie nur Tweets ein, die von Konten mit dem ausgewählten **[!UICONTROL Minimum number of followers]** stammen (beliebige, 100, 500, 1000, 10.000 oder 100.000).

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
