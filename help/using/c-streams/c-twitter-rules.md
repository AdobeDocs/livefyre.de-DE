---
description: Sie können Stream-Regeln erstellen, die Inhalte von Twitter abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte von Twitter abrufen.
seo-title: Twitter-Regeln
solution: Experience Manager
title: Twitter-Regeln
uuid: a 7 fd 2398-fd 6 b -4 c 24-92 b 2-7471176 d 7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Twitter-Regeln{#twitter-rules}

Sie können Stream-Regeln erstellen, die Inhalte von Twitter abrufen.

Erstellen Sie Twitter-Regeln basierend auf Hashtags, Suchbegriffen, @ Erwähnungen oder Autor.

Durch Hinzufügen und **[!UICONTROL Words]** für **[!UICONTROL Username]** eine Regel werden Inhalte zurückgegeben, die beide Einträge enthalten.

>[!NOTE]
>
>Livefyre entspricht den Twitter-Anzeiführungsrichtlinien, und Kunden sind für die Einhaltung dieser Richtlinien verantwortlich. Weitere Informationen finden Sie in der Twitter-Dokumentation zu ihren [Anzeigeanforderungen](https://dev.twitter.com/terms/display-requirements).

Um Twitter-Regeln zum Abrufen von Inhalten aus Twitter-Feeds in Ihre App oder Ihren Ordner zu erstellen, können Sie nach Folgendem Filtern nach:

* **[!UICONTROL Keywords]**
   * Geben **[!UICONTROL Keywords]** Sie ein oder aus Ihrem Twitter-Stream ausgeschlossen. Durch die Angabe von Werten für **[!UICONTROL Contains any of these words]** beide **[!UICONTROL Does not contain any of these words]** Felder werden Tweets zurückgegeben, die das erste enthalten und die zweite nicht enthalten. Es können mehrere Werte für ein einzelnes Feld eingegeben werden und Ergebnisse zurückgegeben werden, die einen der Werte enthalten. Um den Booleschen Operator UND um nach Tweets mit zwei oder mehr Wörtern zu suchen, verwenden Sie zwei (*& &*) Zeichen, um die beiden Wörter voneinander zu trennen.
   * Wenn Sie z. B. **[!UICONTROL Contains any of these words]** Suchbegriffe "Giants" ," Posey" und **[!UICONTROL Does not contain any of these words]** "Suchbegriff Dodger" eingeben, werden alle Tweets zurückgegeben, die die Wort *" Giants* «oder *"Posey* " enthalten und nicht den Begriff *" Dodger*«enthalten.
Geben Sie "Giants & & Posey" ein, um nach Tweets zu suchen, die sowohl die Wörter *" Giants* " als auch " *Posey*" enthalten. Diese Funktion wird nur für die Felder **[!UICONTROL Contains any of these words]** und **[!UICONTROL Does not contain any of these words]** Felder in Twitter-Regeln unterstützt.

* **[!UICONTROL Hashtags]**.
   * Geben **[!UICONTROL Hashtags]** Sie ein oder aus Ihrem Twitter-Stream ausgeschlossen. Die Angabe von Werten für **[!UICONTROL Contains any of these words]** beide **[!UICONTROL Does not contain any of these words]** Felder gibt Tweets zurück, die Hashtags im ersten Feld enthalten, und enthalten keine Hashtags im zweiten Feld. Sie können mehrere Werte für ein einzelnes Feld eingeben. Der Stream gibt Ergebnisse zurück, die einen der Werte enthalten.

* **[!UICONTROL Usernames]**
   * Geben Sie ein **[!UICONTROL @mentions]** , **[!UICONTROL authors]** um in den Stream zu gelangen oder aus dem Stream auszuschließen. Verwenden Sie die Kontrollkästchen, um zu definieren, ob **[!UICONTROL Retweets]** oder **[!UICONTROL replies]** von ausgewählten Autoren ebenfalls einbezogen werden soll.
   >[!NOTE]
   >
   >Sie können entweder Autoren einschließen oder ausschließen; Sie können diese beiden Felder nicht in einer einzelnen Twitter-Regel kombinieren.

* **[!UICONTROL Minimum number of followers.]** Wählen Sie die Mindestanzahl der Follower aus, die der Benutzer benötigen muss, um Informationen aus ihren Beiträgen abzurufen.
* **[!UICONTROL Location]**

   * Geben Sie den Ort (Stadt, Zipcode, Adresse oder Geocode im Format "Allgemeine Breiten/Längengrad" (+/- 90, +/- 180) ein). Beginnen Sie mit der Eingabe eines Speicherorts, um ein Dropdown-Menü mit Vorschlägen anzuzeigen. Wählen Sie einen Ort aus der Dropdown-Liste. Die Karte zeigt einen Pin an dieser Position an. Passen Sie den Schieberegler an, um einen Radius von einer Kilometer bis 25 Meilen für jeden Ort auszuwählen. Wenn Sie keinen Radius auswählen, wählt Livefyre automatisch acht Meilen aus.
   >[!NOTE]
   >
   >Für beide Felder wird der Abstand von der Mitte des Eingabeorts aus berechnet.

   * Sie können mehr als einen Ort und einen Radius hinzufügen. Sie können einen Ort löschen, indem Sie auf das X neben dem Namen einer Position im Feld klicken.
   * Kombinieren Sie die **[!UICONTROL Is near this location]** Felder und **[!UICONTROL Is not near this location]** Felder, um Inhalte innerhalb des **[!UICONTROL Is near this location]** Feldes zu ziehen, jedoch nicht an den Stellen im **[!UICONTROL Is not near this location]** Feld.


* **[!UICONTROL Additional Filters]**
   * Verwenden Sie Zusätzliche Filter, um Ihre Twitter-Regel weiter zu verfeinern. Legen Sie fest, ob Sie:
      * In **[!UICONTROL Replies]** die Targeting-Tweets einbeziehen (wenn der Stream hohe Geschwindigkeit erhält, wird diese Funktion automatisch deaktiviert.)
      * Tweets einbeziehen aus **[!UICONTROL Verified Twitter accounts only.]**
      * Einbeziehen **[!UICONTROL All Content]**, **[!UICONTROL Vines Only]**oder **[!UICONTROL Images Only.]**
      * Schließen Sie nur Tweets ein, die aus Konten mit der ausgewählten stammen **[!UICONTROL Minimum number of followers]** (beliebige, 100, 500, 1000, 10.000 oder 100.000).

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
