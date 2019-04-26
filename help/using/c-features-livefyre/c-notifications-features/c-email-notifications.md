---
description: Erlauben Sie Benutzern, ihre Benachrichtigungsfrequenz und den Inhalt
  auszuwählen.
seo-description: Erlauben Sie Benutzern, ihre Benachrichtigungsfrequenz und den Inhalt
  auszuwählen.
seo-title: E-Mail-Benachrichtigungen
solution: Experience Manager
title: E-Mail-Benachrichtigungen
uuid: 27 dad 133-bd 8 d -4949-8146-1254 c 160 d 3 af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# E-Mail-Benachrichtigungen{#email-notifications}

Erlauben Sie Benutzern, ihre Benachrichtigungsfrequenz und den Inhalt auszuwählen.

**Aktivieren Sie E-Mail-Benachrichtigungen für Ihre Benutzer und Moderatoren.**

Mithilfe von Livefyre-Apps können Sie E-Email-Benachrichtigungen für Ihre Benutzer und Moderatoren aktivieren, basierend auf bestimmten Aktionen. Benachrichtigungen basieren auf dem Zeitpunkt, zu dem Inhalte im Stream gepostet werden, wodurch Ihre Benutzer an Unterhaltungen beteiligt bleiben, die sie interessiert, und benachrichtigt werden, wenn jemand einen ihrer Kommentare gefällt oder beantwortet.

Benutzer und Moderatoren können E-Email-Benachrichtigungen ein- oder auswählen und die Häufigkeit festlegen, mit der E-Emails empfangen werden. In diesem Abschnitt wird beschrieben, wie Sie diese E-Mail-Benachrichtigungen konfigurieren und anpassen.

* Benutzer-E-Mail-Optionen: verfügbare Benutzerbenachrichtigungsoptionen.
* Moderator-E-Mail-Optionen: verfügbare Moderatorbenachrichtigungsoptionen.
* Optionen für Livefyre-Identitätse-Mails: E-Emails, die als Teil der Livefyre-Identität gesendet werden. Diese E-Emails sind nur für Livefyre-Identitätskunden relevant.
* Datensynchronisierung mit Livefyre: Synchronisierung von Voreinstellungen mit Livefyre.
* Anpassen von E-Mails: verfügbare E-Email-Anpassungen.

Verwenden Sie **die Einstellungen "Einstellungen" >" Integrationseinstellungen" > "E-Mail-Benachrichtigungs-Einstellungen** " , um E-Email-Benachrichtigungen für Ihr Netzwerk anzupassen.

>[!NOTE]
>
>Um sicherzustellen, dass Endbenutzer keine unbeabsichtigte E-Mail erhalten, werden keine E-Email-Benachrichtigungen aus der UIN-Umgebung von Livefyre gesendet.

**Benutzer-E-Mail-Optionen**

Livefyre ermöglicht es Ihnen, Benutzern das Empfangen von E-Email-Benachrichtigungen über die Site-Aktivität zu ermöglichen. Verwenden Sie die Einstellungen für die Livefyre-bereitgestellte Benutzerprofile, damit Benutzer ihre Voreinstellungen für Benachrichtigungspläne auswählen können.

>[!NOTE]
>
>E-Mails werden nur für Inhalte gesendet, die manuell im Stream veröffentlicht werden, nicht für Inhalte, die aus socialsync bezogen werden.

Damit Benutzer ihre Benachrichtigungseinstellungen festlegen können, müssen Sie in den Benutzereinstellungen für Ihr Benutzerprofilsystem einen Abschnitt "E-Mail-Benachrichtigungen" angeben. Fügen Sie die entsprechenden Felder Ihrem Benutzerprofildatenbankschema hinzu und verwalten Sie dann Ihre Benutzereinstellungen mit Ping für Pull. (Wenden Sie sich an Ihren Technical Integration Manager, um Standardfrequenzen für Ihr Netzwerk zu definieren. Wenn Sie ein Kunde von Unternehmensprofilen sind, übergeben Sie die ausgewählte Standardeinstellung an Ihr Livefyre-Bereitstellungsteam, um es in der Livefyre-Datenbank zu konfigurieren.)

Benutzer auf Ihrer Site können dann eine Unterhaltung befolgen und E-Mail-Benachrichtigungen empfangen, indem Sie auf die **[!UICONTROL +Follow]** Schaltfläche im Kommentareditor klicken. Benachrichtigungseinstellungen werden auf der Livefyre-Netzwerkebene definiert. Alle Benutzereinstellungen gelten für alle Sites und Unterhaltungen in Ihrem Netzwerk.

**Empfohlene Standardwerte**

* Ein Kommentar in einer Unterhaltung, die ich behebe: ** stündliche Digest**
* Jemand gefällt mir einen meiner Kommentare: ** stündliche Digest**
* Antworten auf eine meiner Kommentare: ** sofort****
* Konversationen automatisch folgen, wenn ich einen Kommentar leere: ** off** (nicht aktiviert)

**Hinweis**: E-Mail-Benachrichtigungen basieren auf dem zeitlichen Inhalt, der für die Einbindung in den Stream genehmigt wurde.

Livefyre bietet zwei E-Email-Häufigkeitsoptionen:

* Sofort
* Stündliche Digest

**Sofort**

E-Mails, die sofort gesendet werden, zeigen den Text des Beitrags, den Artikeltitel, den Benutzernamen des Autors und einen **Antwort** -Link an, der den Benutzer zum Inhalt auf der Seite führt. Diese E-Emails enthalten auch einen Link **zum Abonnieren** der Fußzeile, sodass Benutzer sich von E-Email-Benachrichtigungen für diese Sammlung abmelden können. Durch Klicken auf** Abonnieren werden sie zu einer Bestätigungsseite geleitet, über die sie weiß, dass sie aus der Sammlung abonniert wurden.

**Stündliche Digest**

E-Mails, die in einer stündlichen Digest gesendet werden, zeigen alle Inhalte, Antworten auf Inhalte und "Gefällt mir" -Klicks für den Inhalt innerhalb der letzten Stunde (oder) pro App an, die der Benutzer folgt. Wenn der Benutzer mehrere Apps im Netzwerk ist, erhalten sie für jede App eine E-Email mit einer Digest-E-Email.

>[!NOTE]
>
>In Unterhaltungen ohne neue Inhalte für mehr als mehrere Stunden werden Benutzer mit aktivierter stündlicher Digest sofort auf einem neuen Inhaltsbeitrag benachrichtigt.

**Moderator-E-Mail-Optionen**

Moderatoren können sich entscheiden, E-Emails für Inhalte zu erhalten, die in einer App veröffentlicht werden, und für Kommentare, die Spam oder Offensive in einer App kennzeichnen, die sie moderiert haben. **Hinweis:** Es werden keine E-Emails gesendet, wenn Benutzer einen Kommentar mit "Nicht zutreffend" oder" Aus Thema" markieren, da diese Kategorien für die Moderatorbenachrichtigung nicht als wichtig erachtet werden.

Die Felder Moderator_ Kommentare und Moderator_ Flags sollten außerdem Ihrem Benutzerdatenbankschema für das Benutzerprofil für die Einstellungen von Moderatoren hinzugefügt werden, damit Ihre Moderatoren die Häufigkeit ihrer E-Mail-Benachrichtigungen aktualisieren und abwählen können, wenn sie gewünscht werden. Livefyre empfiehlt, dass Sie diese beiden Moderator-E-Email-Benachrichtigungsfelder nie auf **nie festlegen**. Zu den Optionen gehören **nie** (Standard), **sofort**und **häufig**.

**Moderator-E-Mail (gekennzeichneter Inhalt):**

Wenn der Inhalt in einer moderierten App gekennzeichnet wird, zeigt die an den Moderator gesendete E-Email den gekennzeichneten Inhalt an, den Benutzernamen, der den Inhalt gekennzeichnet hat, und einen Link zurück zur Inhaltsseite.

Wenn ein Benutzer ihre E-Email-Benachrichtigungseinstellungen auf Ihrer Site in Ihrem Profilsystem ändert, synchronisieren Sie das Update mit dem Remote-Profilsystem von Livefyre, indem Sie die Ping-Funktion von Livefyre verwenden.

**Datensynchronisierung mit Livefyre**

## Anpassen von E-Mails {#section_jxb_c5k_yy}

Mehrere Felder in den E-Mail-Benachrichtigungsvorlagen können so geändert werden, dass sie Ihren Stil und Ihre Marke anpassen.

* **[!UICONTROL From Email Address]**

   Die "von E-Mail-Adresse" für alle E-Mail-Benachrichtigungen kann so angepasst werden, dass sie mit Ihrer Marke konsistent ist. Livefyre empfiehlt **noreply@customerdomain.com**und ersetzt **den customerdomainwith**Ihren Domänennamen. (Die Standardeinstellung lautet **noreply@livefyre.com**.) Bitte übergeben Sie Ihre bevorzugte "from E-Email Address" an Ihren Technical Integration Manager zur Konfiguration in der Livefyre-Datenbank für Ihr Netzwerk.

   >[!NOTE]
   >
   >Lassen Sie dieses Feld leer, um E-Mail-Benachrichtigungen für Ihr Netzwerk zu deaktivieren.

* **[!UICONTROL Email Logo]**

   Das in E-Email-Benachrichtigungen angezeigte Logo kann so angepasst werden, dass es Ihr Unternehmenslogo statt des standardmäßigen Livefyre-Logos auf der Registerkarte **"Netzwerkeinstellungen** " von Studio anzeigt. Diese Anpassung ist nur auf Netzwerkebene, nicht auf der Site-Ebene verfügbar und steht nur für bezahlte Livefyre-Kunden zur Verfügung.

* **[!UICONTROL Custom Templates]**

   Falls gewünscht, können Sie eine vollständig angepasste E-Mail-Vorlage implementieren. Dies erfordert jedoch einige Entwicklungsbemühungen und kann zu professionellen Diensten führen. Weitere Informationen erhalten Sie von Ihrem Kundenbetreuer.



Apps, die diese Funktion verwenden:

* [Karussell](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Medienpinnwand](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

