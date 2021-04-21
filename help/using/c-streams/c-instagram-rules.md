---
description: Sie können Stream-Regeln erstellen, die Inhalte aus Instagram abrufen.
title: Instagram-Regeln
exl-id: ac00a12c-94b1-4464-ad3f-991382759d71
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Instagram Rules{#instagram-rules}

Sie können Stream-Regeln erstellen, die Inhalte aus Instagram abrufen.

>[!NOTE]
>
>Bevor Sie einen Instagram-Stream erstellen, müssen Sie mindestens ein Instagram-Geschäftskonto zum Abschnitt **[!UICONTROL Social Accounts]** in **[!UICONTROL Network Settings]** hinzufügen. Weitere Informationen zum Konfigurieren eines Instagram-Kontos finden Sie unter [Informationen zu Instagram-Konten](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

Erstellen Sie Instagram-Regeln basierend auf @mentions oder Hashtag.

>[!NOTE]
>
>Alle Instagram-Regeln erfordern mindestens ein Hashtag. Wenn Sie Suchbegriffe und einen Benutzernamen für Ihre Regel hinzufügen, werden Inhalte zurückgegeben, die beide Einträge enthalten.

Um Instagram-Regeln zum Abrufen von Inhalten aus Instagram-Feeds in Ihre App oder Ihren Ordner zu erstellen, filtern Sie nach:

* **[!UICONTROL Words]**

   * Geben Sie **[!UICONTROL hashtags]** ein, um in Ihren Instagram-Stream eingeschlossen oder ausgeschlossen zu werden. Wenn Sie Werte für die Felder **[!UICONTROL Contains]** und **[!UICONTROL Does not contain]** angeben, werden Bilder zurückgegeben, die das erste und das zweite enthalten.

   * Wenn Sie z. B. **[!UICONTROL Contains]** die Suchbegriffe Giants, Posey und **[!UICONTROL Does not contain]** Suchbegriff Dodger eingeben, werden alle Beiträge zurückgegeben, die das Wort Giants oder Posey enthalten, ohne das Wort Dodger.

      >[!NOTE]
      >
      >Instagram Rules gibt Beiträge zurück, die das aufgelistete Hashtag in den Kommentaren des Autors enthalten, was möglicherweise nicht im Stream angezeigt wird.

* **[!UICONTROL Mentions]**

   * Geben Sie **[!UICONTROL @mentions]** ein, um in den Stream zu ziehen, oder schließen Sie ihn vom Stream aus.

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >Sie müssen über ein Instagram-Geschäftskonto in Livefyre verfügen, um die Autorensuche in einer Instagram Stream-Regel verwenden zu können. Weitere Informationen zum Einrichten von Instagram-Geschäftskonten in Livefyre finden Sie unter [Informationen zu Instagram-Konten](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

   * Geben Sie **[!UICONTROL @usernames]** ein, um in den Stream zu ziehen. Das mit dem **@username** verknüpfte Konto muss ein Instagram-Geschäftskonto sein.

   * Geben Sie die **@usernames** ein, die vom Stream ausgeschlossen werden sollen.

* **[!UICONTROL Additional Filters]**

   * Wählen Sie aus, ob **[!UICONTROL All Content]**, **[!UICONTROL Videos Only]** oder **[!UICONTROL Photos Only]** in den Stream einbezogen werden sollen.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
