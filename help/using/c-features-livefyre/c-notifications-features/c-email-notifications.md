---
description: Erlauben Sie Benutzern, ihre Benachrichtigungsfrequenz und ihren Inhalt auszuwählen.
title: E-Mail-Benachrichtigungen
exl-id: 46821382-ac93-4523-a0ac-84535e76d367
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# E-Mail-Benachrichtigungen{#email-notifications}

Erlauben Sie Benutzern, ihre Benachrichtigungsfrequenz und ihren Inhalt auszuwählen.

**Aktivieren Sie E-Mail-Benachrichtigungen für Ihre Benutzer und Moderatoren.**

Mit Livefyre-Apps können Sie E-Mail-Benachrichtigungen für Benutzer und Moderatoren basierend auf bestimmten Aktionen aktivieren. Benachrichtigungen basieren auf dem Zeitpunkt, zu dem Inhalte in den Stream gepostet werden, und ermöglichen Ihren Benutzern, an Gesprächen teilzunehmen, die ihnen wichtig sind, und benachrichtigt zu werden, wenn jemand einen ihrer Kommentare gefällt oder darauf antwortet.

Benutzer und Moderatoren können E-Mail-Benachrichtigungen Opt-in oder abbrechen und die Häufigkeit festlegen, mit der E-Mails empfangen werden. In diesem Abschnitt wird beschrieben, wie Sie diese E-Mail-Benachrichtigungen konfigurieren und anpassen.

* E-Mail-Optionen für Benutzer: verfügbare Benutzerbenachrichtigungsoptionen.
* Moderator-E-Mail-Optionen: verfügbare Benachrichtigungsoptionen für Moderatoren.
* Optionen für Livefyre-Identitäts-E-Mails: E-Mails, die als Teil von Livefyre Identity gesendet werden. Diese E-Mails sind nur für Livefyre Identity Customers relevant.
* Datensynchronisierung mit Livefyre: die Voreinstellungen mit Livefyre synchronisieren.
* Anpassen von E-Mails: verfügbare E-Mail-Anpassungen.

Verwenden Sie die Optionen **Einstellungen > Integrationseinstellungen > E-Mail-Benachrichtigungseinstellungen**, um E-Mail-Benachrichtigungen für Ihr Netzwerk anzupassen.

>[!NOTE]
>
>Um sicherzustellen, dass Ihre Endbenutzer keine unbeabsichtigte Post erhalten, werden keine E-Mail-Benachrichtigungen von der Livefyre UAT-Umgebung gesendet.

**E-Mail-Optionen für Benutzer**

Livefyre ermöglicht es Ihnen, Benutzern das Empfangen von E-Mail-Benachrichtigungen über die Site-Aktivität zu ermöglichen. Verwenden Sie die von Livefyre bereitgestellten User Profil-Integrationseinstellungen, um Benutzern die Auswahl ihrer Voreinstellungen für Benachrichtigungspläne zu ermöglichen.

>[!NOTE]
>
>E-Mails werden nur für Inhalte gesendet, die manuell in den Stream gepostet werden, nicht für Inhalte, die aus SocialSync abgerufen werden.

Um Benutzern das Festlegen ihrer Benachrichtigungseinstellungen zu ermöglichen, fügen Sie in den Benutzereinstellungen für Ihr Profil einen Abschnitt &quot;E-Mail-Benachrichtigung&quot;ein. hinzufügen Sie die entsprechenden Felder in Ihr Profil-Datenbank-Schema ein und verwalten Sie dann Ihre Benutzereinstellungen mit Ping for Pull. (Arbeiten Sie mit Ihrem Technical Integration Manager zusammen, um Standardfrequenzen für Ihr Netzwerk zu definieren. Wenn Sie Enterprise Profils-Kunde sind, übergeben Sie Ihre Standardeinstellungen zur Konfiguration in der Livefyre-Versand-Datenbank an Ihr Livefyre-Team.)

Benutzer auf Ihrer Site können dann eine Konversation verfolgen und E-Mail-Benachrichtigungen empfangen, indem sie im Kommentareditor auf die Schaltfläche **[!UICONTROL +Follow]** klicken. Benachrichtigungseinstellungen werden auf der Ebene des Livefyre-Netzwerks definiert. Alle Benutzereinstellungen gelten für alle Sites und Konversationen im Netzwerk.

**Empfohlene Standardwerte**

* Jemand kommentiert in einer Unterhaltung Ich bin:** Stündliche Zusammenfassung**
* Einer meiner Kommentare gefällt:** Stündlich verdauen**
* Jemand antwortet auf eine meiner Bemerkungen:** sofort**
* Unterhaltungen automatisch ausführen, wenn ich einen Kommentar hinterlasse:*** off* (nicht markiert)

**Hinweis**: E-Mail-Benachrichtigungen basieren auf dem Zeitpunkt, zu dem der Inhalt für die Aufnahme in den Stream genehmigt wurde.

Livefyre-Angebote: zwei Optionen für die E-Mail-Frequenz:

* Sofort
* Stündlich

**Sofort**

E-Mails, die sofort gesendet werden, zeigen den Text des Beitrags, den Artikeltitel, den Benutzernamen des Autors und den Link **Antwort** an, über den der Benutzer zu dem Inhalt auf der Seite gelangt. Diese E-Mails enthalten auch den Link **unsubscribe** in der Fußzeile, über den die Benutzer ihre E-Mail-Benachrichtigungen für diese Sammlung abbestellen können. Durch Klicken auf **Abbestellen **werden sie auf eine Bestätigungsseite geleitet, auf der sie wissen, dass sie von der Sammlung abgemeldet wurden.

**Stündlich**

In einer stündlichen Zusammenfassung gesendete E-Mails zeigen alle Inhalte, Antworten auf Inhalte und &quot;Gefällt mir&quot;-Klicks innerhalb der letzten Stunde (oder so) pro App an, der der Benutzer folgt. Wenn der Benutzer mehrere Apps in Ihrem Netzwerk verfolgt, erhält er für jede App eine Digest-E-Mail.

>[!NOTE]
>
>Bei Konversationen ohne neuen Inhalt für mehr als mehrere Stunden erhalten Benutzer mit aktivierter stündlicher Zusammenfassung sofort eine Benachrichtigung bei einem neuen Inhaltsbeitrag.

**Moderator-E-Mail-Optionen**

Moderatoren können E-Mails für Inhalte Opt-in, die in einer App veröffentlicht werden, denen sie folgen, und für Kommentare, die in einer App als Spam oder Offensive gekennzeichnet sind, moderieren. **Hinweis:** Es werden keine E-Mails gesendet, wenn der Benutzer einen Kommentar mit &quot;Nicht einverstanden&quot;oder &quot;Nicht-Thema&quot;markiert, da diese Kategorien für die Moderatorbenachrichtigung nicht als wichtig erachtet werden.

Die Felder &quot;moderator_comments&quot;und &quot;moderator_flags&quot;sollten auch dem Schema der Seite &quot;Einstellungen für Moderator-Profile&quot;hinzugefügt werden, damit Ihre Moderatoren die Häufigkeit ihrer E-Mail-Benachrichtigungen aktualisieren können und Opt-out, ob sie dies wünschen. Livefyre empfiehlt, diese beiden E-Mail-Benachrichtigungsfelder des Moderators auf **never** zu setzen. Zu den Optionen zählen **never** (Standard), **directly** und **oft**.

**Moderator-E-Mail (gekennzeichneter Inhalt):**

Wenn Inhalte in einer moderierten App markiert werden, zeigt die E-Mail, die an den Moderator gesendet wird, den gekennzeichneten Inhalt, den Benutzernamen, der den Inhalt markiert hat, und einen Link zurück zur Inhaltsseite an.

Wenn ein Benutzer seine Voreinstellungen für E-Mail-Benachrichtigungen auf Ihrer Site in Ihrem Profil-System ändert, synchronisieren Sie das Update mit Livefyre Remote Profil mit Livefyres Ping for Pull.

**Datensynchronisierung mit Livefyre**

## Anpassen von E-Mails {#section_jxb_c5k_yy}

Mehrere Felder in den E-Mail-Benachrichtigungsvorlagen können an Ihren Stil und Ihre Marke angepasst werden.

* **[!UICONTROL From Email Address]**

   Die &quot;Von-E-Mail-Adresse&quot;für alle E-Mail-Benachrichtigungen kann an Ihre Marke angepasst werden. Livefyre empfiehlt **noreply@customerdomain.com**, **customerdomain** durch Ihren Domänennamen zu ersetzen. (Die Standardeinstellung ist **noreply@livefyre.com**.) Bitte senden Sie zur Konfiguration in der Livefyre-Datenbank für Ihr Netzwerk Ihre bevorzugte &quot;Von E-Mail-Adresse&quot;an Ihren Technical Integration Manager.

   >[!NOTE]
   >
   >Lassen Sie dieses Feld leer, um E-Mail-Benachrichtigungen für Ihr Netzwerk zu deaktivieren

* **[!UICONTROL Email Logo]**

   Das in E-Mail-Benachrichtigungen angezeigte Logo kann angepasst werden, um Ihr Firma-Logo anstelle des Livefyre-Standardlogos anzuzeigen. Verwenden Sie dazu die Registerkarte &quot;Branding&quot;auf der Seite **Netzwerkeinstellungen** von Studio. Diese Anpassung steht nur auf Netzwerkebene und nicht auf Site-Ebene zur Verfügung und ist nur für kostenpflichtige Livefyre-Kunden verfügbar.

* **[!UICONTROL Custom Templates]**

   Sie können auf Wunsch eine vollständig angepasste E-Mail-Vorlage implementieren. Dies erfordert jedoch gewisse Entwicklungsbemühungen und kann mit Kosten für freiberufliche Dienstleistungen verbunden sein. Weitere Informationen erhalten Sie von Ihrem Kundenbetreuer.



Apps, die diese Funktion verwenden:

* [Karussell](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Funktionskarte](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Medienwall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
