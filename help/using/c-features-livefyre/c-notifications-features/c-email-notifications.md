---
description: Erlauben Sie Benutzern, ihre Benachrichtigungsfrequenz und ihren Inhalt auszuwählen.
seo-description: Erlauben Sie Benutzern, ihre Benachrichtigungsfrequenz und ihren Inhalt auszuwählen.
seo-title: E-Mail-Benachrichtigungen
solution: Experience Manager
title: E-Mail-Benachrichtigungen
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# E-Mail-Benachrichtigungen{#email-notifications}

Erlauben Sie Benutzern, ihre Benachrichtigungsfrequenz und ihren Inhalt auszuwählen.

**Aktivieren Sie E-Mail-Benachrichtigungen für Ihre Benutzer und Moderatoren.**

Mit Livefyre-Apps können Sie E-Mail-Benachrichtigungen für Benutzer und Moderatoren basierend auf bestimmten Aktionen aktivieren. Benachrichtigungen basieren auf dem Zeitpunkt, zu dem Inhalte in den Stream gepostet werden, und ermöglichen Ihren Benutzern, an Gesprächen teilzunehmen, die ihnen wichtig sind, und benachrichtigt zu werden, wenn jemand einen ihrer Kommentare gefällt oder darauf antwortet.

Benutzer und Moderatoren können die E-Mail-Benachrichtigung ein- oder abwählen und die Häufigkeit festlegen, mit der E-Mails empfangen werden. In diesem Abschnitt wird beschrieben, wie Sie diese E-Mail-Benachrichtigungen konfigurieren und anpassen.

* E-Mail-Optionen für Benutzer: verfügbare Benutzerbenachrichtigungsoptionen.
* Moderator-E-Mail-Optionen: verfügbare Benachrichtigungsoptionen für Moderatoren.
* Optionen für Livefyre-Identitäts-E-Mails: E-Mails, die als Teil von Livefyre Identity gesendet werden. Diese E-Mails sind nur für Livefyre Identity Customers relevant.
* Datensynchronisierung mit Livefyre: die Voreinstellungen mit Livefyre synchronisieren.
* E-Mails anpassen: verfügbare E-Mail-Anpassungen.

Verwenden Sie die Optionen **Einstellungen &gt; Integrationseinstellungen &gt; E-Mail-Benachrichtigungseinstellungen** , um E-Mail-Benachrichtigungen für Ihr Netzwerk anzupassen.

>[!NOTE]
>
>Um sicherzustellen, dass Ihre Endbenutzer keine unbeabsichtigte Post erhalten, werden keine E-Mail-Benachrichtigungen von der Livefyre UAT-Umgebung gesendet.

**E-Mail-Optionen für Benutzer**

Mit Livefyre können Sie Benutzern ermöglichen, E-Mail-Benachrichtigungen über Site-Aktivitäten zu erhalten. Verwenden Sie die in Livefyre bereitgestellten Einstellungen zur Benutzerprofilintegration, um Benutzern die Auswahl ihrer Voreinstellungen für Benachrichtigungspläne zu ermöglichen.

>[!NOTE]
>
>E-Mails werden nur für Inhalte gesendet, die manuell in den Stream gepostet werden, nicht für Inhalte, die aus SocialSync abgerufen werden.

Damit Benutzer ihre Benachrichtigungseinstellungen festlegen können, fügen Sie in den Benutzereinstellungen für Ihr Benutzerprofilsystem den Abschnitt "E-Mail-Benachrichtigung"ein. Fügen Sie die entsprechenden Felder zum Benutzerprofildatenbankschema hinzu und verwalten Sie dann Ihre Benutzereinstellungen mit Ping for Pull. (Arbeiten Sie mit Ihrem Technical Integration Manager zusammen, um Standardfrequenzen für Ihr Netzwerk zu definieren. Wenn Sie Enterprise Profiles-Kunde sind, übergeben Sie Ihre ausgewählten Standardwerte zur Konfiguration in der Livefyre-Datenbank an Ihr Livefyre-Bereitstellungsteam.)

Benutzer auf Ihrer Site können dann eine Konversation verfolgen und E-Mail-Benachrichtigungen empfangen, indem sie im Kommentareditor auf die **[!UICONTROL +Follow]** Schaltfläche klicken. Benachrichtigungseinstellungen werden auf Livefyre-Netzwerkebene definiert. Alle Benutzereinstellungen gelten für alle Sites und Konversationen im Netzwerk.

**Empfohlene Standardwerte**

* Jemand kommentiert in einer Unterhaltung Ich bin:** Stündliche Zusammenfassung**
* Einer meiner Kommentare gefällt:** Stündlich verdauen**
* Jemand antwortet auf eine meiner Bemerkungen:** sofort**
* Unterhaltungen automatisch ausführen, wenn ich einen Kommentar hinterlasse:*** off* (nicht markiert)

**Hinweis**: E-Mail-Benachrichtigungen basieren auf dem Zeitpunkt, zu dem der Inhalt für die Aufnahme in den Stream genehmigt wurde.

Livefyre bietet zwei Optionen für die E-Mail-Frequenz:

* Sofort
* Stündlich

**Sofort**

E-Mails, die sofort gesendet werden, zeigen den Text des Beitrags, den Artikeltitel, den Benutzernamen des Autors und einen Link zur **Antwort** an, über den der Benutzer zu den Inhalten auf der Seite gelangt. Diese E-Mails enthalten auch einen Link zum **Abmelden** in der Fußzeile, über den Benutzer sich von E-Mail-Benachrichtigungen für diese Sammlung abmelden können. Durch Klicken auf **Abbestellen **werden sie auf eine Bestätigungsseite geleitet, auf der sie wissen, dass sie von der Sammlung abgemeldet wurden.

**Stündlich**

In einer stündlichen Zusammenfassung gesendete E-Mails zeigen alle Inhalte, Antworten auf Inhalte und "Gefällt mir"-Klicks innerhalb der letzten Stunde (oder so) pro App an, der der Benutzer folgt. Wenn der Benutzer mehrere Apps in Ihrem Netzwerk verfolgt, erhält er für jede App eine Digest-E-Mail.

>[!NOTE]
>
>Bei Konversationen ohne neuen Inhalt für mehr als mehrere Stunden erhalten Benutzer mit aktivierter stündlicher Zusammenfassung sofort eine Benachrichtigung bei einem neuen Inhaltsbeitrag.

**Moderator-E-Mail-Optionen**

Moderatoren können sich für den Erhalt von E-Mails für Inhalte entscheiden, die in einer App veröffentlicht werden, denen sie folgen, und für Kommentare, die in einer App als Spam oder Offensive gekennzeichnet sind, moderieren sie. **** Hinweis: Es werden keine E-Mails gesendet, wenn Benutzer einen Kommentar mit "Nicht einverstanden"oder "Nicht-Thema"kennzeichnen, da diese Kategorien für die Moderatorbenachrichtigung nicht als wichtig erachtet werden.

Die Felder "moderator_comments"und "moderator_flags"sollten auch dem Datenbankschema Ihrer Seite "Benutzerprofileinstellungen"für Moderatoren hinzugefügt werden, damit Ihre Moderatoren die Häufigkeit ihrer E-Mail-Benachrichtigungen aktualisieren können und die Möglichkeit haben, diese bei Bedarf abzuwählen. Livefyre empfiehlt, diese beiden E-Mail-Benachrichtigungsfelder des Moderators auf **nie** festzulegen. Zu den Optionen gehören **never** (Standard), **once** und **oft**.

**Moderator-E-Mail (gekennzeichneter Inhalt):**

Wenn Inhalte in einer moderierten App markiert werden, zeigt die E-Mail, die an den Moderator gesendet wird, den gekennzeichneten Inhalt, den Benutzernamen, der den Inhalt markiert hat, und einen Link zurück zur Inhaltsseite an.

Wenn ein Benutzer seine Voreinstellungen für E-Mail-Benachrichtigungen auf Ihrer Site in Ihrem Profilsystem ändert, synchronisieren Sie das Update mit Livefyre Ping for Pull mit dem LiveFeyre-Remote-Profilsystem.

**Datensynchronisierung mit Livefyre**

## Anpassen von E-Mails {#section_jxb_c5k_yy}

Mehrere Felder in den E-Mail-Benachrichtigungsvorlagen können an Ihren Stil und Ihre Marke angepasst werden.

* **[!UICONTROL From Email Address]**

   Die "Von-E-Mail-Adresse"für alle E-Mail-Benachrichtigungen kann an Ihre Marke angepasst werden. Livefyre empfiehlt, **noreply@customerdomain.com** zu ersetzen, indem **** customerdomainname durch Ihren Domänennamen ersetzt wird. (Die Standardeinstellung ist **noreply@livefyre.com**.) Bitte senden Sie zur Konfiguration in der Livefyre-Datenbank für Ihr Netzwerk Ihre bevorzugte "Von E-Mail-Adresse"an Ihren Technical Integration Manager.

   >[!NOTE]
   >
   >Lassen Sie dieses Feld leer, um E-Mail-Benachrichtigungen für Ihr Netzwerk zu deaktivieren

* **[!UICONTROL Email Logo]**

   Das in E-Mail-Benachrichtigungen angezeigte Logo kann angepasst werden, um Ihr Firmenlogo anstelle des standardmäßigen Livefyre-Logos anzuzeigen, und zwar über die Registerkarte "Branding"auf der Seite " **Netzwerkeinstellungen** "von Studio. Diese Anpassung steht nur auf Netzwerkebene und nicht auf Site-Ebene zur Verfügung und ist nur für kostenpflichtige Livefyre-Kunden verfügbar.

* **[!UICONTROL Custom Templates]**

   Sie können auf Wunsch eine vollständig angepasste E-Mail-Vorlage implementieren. Dies erfordert jedoch gewisse Entwicklungsbemühungen und kann mit Kosten für freiberufliche Dienstleistungen verbunden sein. Weitere Informationen erhalten Sie von Ihrem Kundenbetreuer.



Apps, die diese Funktion verwenden:

* [Karussell](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Funktionskarte](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Medienwall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

