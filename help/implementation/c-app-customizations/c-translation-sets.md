---
description: Mithilfe von Übersetzungssets können Sie alternative Sprachen für Apps angeben.
title: Übersetzungs-Sets
exl-id: 688138bf-f8e9-4fe5-99e2-2451deefd217
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '1302'
ht-degree: 7%

---

# Übersetzungs-Sets {#translation-sets}

Mithilfe von Übersetzungssets können Sie alternative Sprachen für Apps angeben.

Verwenden Sie Übersetzungseinstellungen, um Apps in verschiedenen Sprachen zu lokalisieren oder Alternativtext für mehrere Apps von einem Ort in Studio aus anzugeben. Sie können beispielsweise sicherstellen, dass alle Sites mit spanischer Sprache für alle App-Felder die spanische Sprache verwenden. Sie können den Text auch so ändern, dass alle Felder mit der Stimme und dem Gefühl Ihrer Site oder Ihres Netzwerks übereinstimmen.

Sie können Übersetzungseinstellungen für alle Apps außer &quot;Storify 2&quot;festlegen. Weitere Informationen dazu, welche Felder lokalisiert werden können, finden Sie unter [Strings lokalisieren](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Kommentare, Live-Blog und Chat verwenden denselben Zeichensatz innerhalb eines Übersetzungssatzes.

Geben Sie einen Übersetzungssatz für ein Netzwerk, eine Site, eine App oder eine API an.

Die Übersetzungssätze auf unterschiedlichen Ebenen überschreiben sich gegenseitig nach folgendem Muster:

* API-Übersetzungs-Set überschreibt alle Übersetzungssätze auf allen Ebenen (App, Netzwerk und Site)
* Der App-Übersetzungs-Satz setzt Übersetzungssätze auf Netzwerk- und Site-Ebene außer Kraft.
* Übersetzungssätze auf Site-Ebene überschreiben Übersetzungssätze auf Netzwerkebene.

## Überprüfen von Textzeichenfolgen {#c-review-text-strings}

Anpassen der Textzeichenfolgen für Livefyre-Prüfungen.

Auf dieser Seite werden die zur Anpassung in Review-Apps verfügbaren Zeichenfolgen aufgelistet und beschrieben. Die hier aufgeführten Zeichenfolgen werden zusätzlich zu den Standardzeichenfolgen für Livefyre-Core-Apps und deren Überschreibungen angezeigt, die unter Zeichenfolgenanpassung aufgeführt sind. Wo Duplikate aufgelistet sind, sind die in diesen Tabellen aufgeführten Zeichenfolgen die Standardwerte für die Reviews-Apps.

* Implementierung
* Benutzeroberfläche für Überprüfung/Bewertung
* Stream-Informationen
* Autor-/Inhaltsinformationen
* Benutzeraktionen
* Post-Funktionen
* Fehler

## Implementierung {#section-vsy-1k4-xz}

Um diese Funktion zu implementieren, übergeben Sie eine 1-1-Objektzuordnung der Zeichenfolgen, die Sie überschreiben möchten, an das JavaScript-Konfigurationsobjekt. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

Beispiel:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" }; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Benutzeroberfläche für Überprüfung/Bewertung {#section_iyv_zj4_xz}

Zeichenfolgen, die für die Benutzeroberfläche &quot;Überprüfen und bewerten&quot;verfügbar sind.

| Element | Schlüssel | Standardtext |
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Schaltflächen |  |  |
|  | editReviewBtn | Prüfung bearbeiten |
|  | reviewBtn | Überprüfung schreiben |
|  | viewsClosed | Abgeschlossene Überprüfungen |
|  | showReviewBtn | Überprüfung anzeigen |
|  | folgen | Ich interessiere mich |
|  | shareText | Ich habe gerade eine Überprüfung geschrieben. Schau es dir an! |
| QuickInfos zur Bewertung |  |  |
|  | ratingValues | Als Array. Standard = [&quot;Poor&quot;, &quot;Poor&quot;, &quot;Fair&quot;, &quot;Fair&quot;, &quot;Average&quot;, &quot;Average&quot;, &quot;Good&quot;, &quot;Good&quot;, &quot;Excellent&quot;, &quot;Excellent&quot;]; |
|  |  | Hinweis: Die Werte im Array müssen dupliziert werden, damit sowohl die linke als auch die rechte Hälfte jedes Sterns denselben Namen erhalten. |
| Bewertungsunterteile |  |  |
|  | ratingSubpartPlaceholders | Als Array. Standardeinstellung = [] |
|  | ratingSubpartTitles | Als Array. Standardeinstellung = [] |
|  | reviewStreamTitle | Standardmäßig leer. Titel des Zusammenfassungsabschnitts der Überprüfung. |
| Verschiedenes |  |  |
|  | averageRating | Durchschnittliche Benutzerbewertung |
|  | breakHeader | Bewertungsaufschlüsselung |
|  | help | %s von %s gefunden hilfreich |
|  | assistancePlural | %s von %s gefunden hilfreich |
|  | outOf | / |
|  | ratingType | star |

## Stream-Informationen {#section_wmv_yj4_xz}

Zeichenfolgen, die für Informationen und Anzeigen des Inhalts-Streams verfügbar sind.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Sortieren* |  |  |
|  | sortBy | *Standardmäßig leer.* |
|  | sortHighestRated | Höchste Bewertung |
|  | sortLowestRated | Niedrigste Bewertung |
|  | sortMostHelpful | Am meisten hilfreich |
| *Stream misc.* |  |  |
|  | showMore | Mehr anzeigen |
| *Stream-Hochgeschwindigkeit* |  |  |
|  | newComment | Neue Prüfung |
|  | newComments | Neue Überprüfungen |
| *Listener-Anzahl* |  |  |
|  | listenerCount | Personen, die |
|  | listenerCountPlural | Personen, die zuhören |
| *Anzahl der Kommentare* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *Anzahl der Benachrichtigungen* |  |  |
|  | commentNotifier | Neue Prüfung |
|  | commentNotifierPlural | Neue Überprüfungen |

## Autor-/Inhaltsinformationen {#section_osx_xj4_xz}

Für Autoren- und individuelle Inhaltsinformationen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Thread-Aufschlüsselung* |  |  |
|  | viewsContentNotFoundMsg | Diese Überprüfung ist nicht mehr sichtbar. |
|  | backToComments | Zurück zu Prüfungen |

## Benutzeraktionen {#section_tlx_wj4_xz}

Für Benutzeraktionen verfügbare Zeichenfolgen: Kennzeichnen, Freigeben und Kennzeichnen vorhandener Inhalte als hilfreich.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Kommentar-Fußzeile* |  |  |
|  | wasReviewHelpful | Nützlich? |
|  | wasReviewHelpfulMobile | Nützlich? |
|  | ownWarReviewHelpful | Es fand hilfreich. |
|  | reviewWarHelpful | Ja |
|  | assistanceDivider | &amp;vert; |
|  | reviewWarNotHelpful | Nein |
| *modale Abstimmung* |  |  |
|  | optionTitle | War diese Überprüfung hilfreich? |
|  | optionDownvoice | Nein |
|  | optionReplyTitle | War diese Antwort hilfreich? |
|  | optionTitle | War dieser Kommentar hilfreich? |
|  | VVTutum | Ja |
| *Modal kennzeichnen* |  |  |
|  | flagTitle | Überprüfung von %s kennzeichnen |
|  | flagSuccessMsg | Die Überprüfung wurde gekennzeichnet. |
| *Flag Mobile* |  |  |
|  | flagConfirmationMessage | %s Überprüfung als %s kennzeichnen? |
| *Erwähnungsmodal* |  |  |
|  | mentionDefaultText | Ich habe Sie in einem Livefyre-Review erwähnt. |
| *Modal freigeben* |  |  |
|  | shareTitle | Weitergeben |

## Post-Funktionen {#section_yl1_wj4_xz}

Zeichenfolgen stehen Benutzern zur Verfügung, die Rezensionen posten.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Editor* |  |  |
|  | bodyPlaceholder | Überprüfung schreiben... |
|  | postEditButton | Vorlage      |
|  | postEditCancelButton | Abbrechen |
|  | postAsButton | Beitragsüberprüfung als ... |
|  | postButton | Beitragsüberprüfung |
|  | postReplyAsButton | Posten als... |
|  | postReplyButton | Posten |
|  | shareButton | Freigabe |
|  | titlePlaceholder | Titel… |

## Fehler {#section_jbc_vj4_xz}

Für allgemeine Fehlermeldungen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Fehler |  |  |
|  | errorAlreadyPosted | Sie können nur eine Überprüfung posten. |
|  | errorAuthError | Sie sind nicht berechtigt, einen Review zu dieser Unterhaltung zu posten |
|  | errorCommentsNotAllowed | Bewertungen können derzeit nicht veröffentlicht werden |
|  | errorDislikeOwnComment | Sie können Ihre eigene Überprüfung nicht ablehnen |
|  | errorDuplicate | So sehr Sie Ihre Überprüfung mögen, Sie dürfen sie nicht zweimal posten. |
|  | errorEditDuplicate | Sie müssen den Text des Reviews ändern, wenn Sie ihn bearbeiten. |
|  | errorEditNotAllowed | Sie dürfen keine Rezensionen zu diesem Gespräch bearbeiten. |
|  | errorEditTimeExceeded | Ihre Revisionsbearbeitungszeit ist leider abgelaufen. |
|  | errorEmpty | Es scheint, dass Sie versuchen, eine leere Überprüfung zu posten. |
|  | errorEmptyTitle | Sie versuchen anscheinend, einen leeren Titel zu posten |
|  | errorFieldRating | Sternbewertung |
|  | errorFieldReview | Überprüfung |
|  | errorFieldTitle | title |
|  | errorMaxChars | Tut mir leid, Ihre Überprüfung ist zu lang. Bitte bearbeiten und versuchen Sie es erneut. |
|  | errorMissingFields | Bitte geben Sie eine |
|  | errorRatingEmpty | Sie können keine leere Bewertung einreichen |
|  | errorRatingNotSet | Alle Bewertungen müssen festgelegt werden |
|  | errorRatingNotValid | Die Bewertung muss ein Objekt sein |
|  | errorShowMore | Beim Laden weiterer Überprüfungen ist ein Fehler aufgetreten. |
|  | errorTitleMaxChars | Entschuldigung, dein Titel ist zu lang. Bitte bearbeiten und versuchen Sie es erneut. |
|  | errorVoteOwnComment | Sie können nicht über Ihre eigene Überprüfung abstimmen |

## Anmerkungen: Textzeichenfolgen {#c_sidenotes_text_strings}

Anpassen der Textzeichenfolgen für Livefyre Sideinformationen

<!-- 

c_sidenotes_text_strings.dita

 -->

Auf dieser Seite werden alle Zeichenfolgen aufgelistet und beschrieben, die zur Anpassung in Sidebar-Apps verfügbar sind. Informationen zu den für die Livefyre-Hauptanwendungen verfügbaren Zeichenfolgen finden Sie unter Zeichenfolgenanpassungen .

* Implementierung
* Auth
* Stream-Informationen
* Autor-/Inhaltsinformationen
* Benutzeraktionen
* Post-Funktionen
* Moderatorschnittstelle
* Fehler

## Implementierung {#section_wp2_ql4_xz}

Um diese Funktion zu implementieren, übergeben Sie eine 1-1-Objektzuordnung der Zeichenfolgen, die Sie überschreiben möchten, an das JavaScript-Konfigurationsobjekt. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

Beispiel:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Authentifizierung {#section_pqf_3l4_xz}

Zeichenfolgen, die für den Authentifizierungsprozess und die authentifizierten Benutzermenüs verfügbar sind.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Authentifizierungsmenüzeichenfolgen* |  |  |
|  | menuAuthSignInBtn | Anmelden |
|  | menuAuthSignedInMsg | Sie müssen bei {action} angemeldet sein. |
|  | menuUserEditProfile | Profil bearbeiten |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Abmelden |
|  | menuUserBackBtn | Alle |

## Stream-Informationen {#section_wpy_gl4_xz}

Zeichenfolgen, die für Informationen und Anzeigen des Inhalts-Streams verfügbar sind.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Menüoptionen &quot;Info&quot;* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Hilfe |
|  | menuInfoLivefyreLink | Besuch Livefyre.com |

## Autor-/Inhaltsinformationen {#section_dhb_gl4_xz}

Für Autoren- und individuelle Inhaltsinformationen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | In Bearbeitung |
|  | commentReadMoreLink | Weitere Info |
|  | commentReplyLink | Siehe {number} Antworten |
|  | commentReplyLinkSing | Siehe Antwort |
|  | commentVoteCount | abstimmen |
|  | commentVoteCountSing | Stimme |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *Als Array. Standard = *[ &quot;Januar&quot;, &quot;Februar&quot;, &quot;März&quot;, &quot;April&quot;, &quot;Mai&quot;, &quot;Juni&quot;, &quot;Juli&quot;, &quot;August&quot;, &quot;September&quot;, &quot;Oktober&quot;, &quot;November&quot;, &quot;Dezember&quot; ] |
|  | QuestionExplanation | Sie können jetzt Kommentare zu Sätzen, Absätzen, Bildern und Anführungszeichen direkt lesen und schreiben. <br>Markieren Sie Text und klicken Sie auf das Symbol oder klicken Sie auf das Symbol am Ende jedes Absatzes. |
|  | QuestionMockText | Was &quot;familiär bekannt&quot; ist, ist nicht richtig bekannt, nur weil es &quot;bekannt&quot; ist. |
|  | QuestionTitle | Was ist ein Sidenote? |

## Benutzeraktionen {#section_qxd_fl4_xz}

Für Benutzeraktionen verfügbare Zeichenfolgen: Kennzeichnen, Freigeben und Verknüpfen vorhandener Inhalte.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Optionen des Antwortmenüs* |  |  |
|  | menuRepliesViewTitle | Details |
|  | menuRepliesViewReply | Antwort auf Unterhaltung |
| *Menüoptionen freigeben* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Freigabe |
| *Menüoptionen für Kennzeichnungen* |  |  |
|  | menuFlagOptionDisübereinkommen | Uneinigkeit |
|  | menuFlagOptionOffensive | Offensive |
|  | menuFlagOptionOffTopic | Aus Thema |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Markierung als... |
|  | facebookShareCaption | Anmerkungen auf &quot;{title}&quot; |
| *Mobilbenutzeroptionen* |  |  |
|  | reglerCommentTally | of |
|  | reglerInviteRead | Gelesen |
|  | reglerInviteWrite | Schreiben |
|  | reglerLoading | Wird geladen… |
|  | reglerWriteText | Was denkst du? Tippen Sie zum Schreiben. |

## Post-Funktionen {#section_xzf_2l4_xz}

Zeichenfolgen sind für Benutzer verfügbar, die Inhalte posten.

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | editorEditBtn | Speichern |
|  | editorEditPosting | Speichern... |
|  | editorEditReplyTitle | Antwort bearbeiten |
|  | editorEditTitle | Sidenote bearbeiten |
|  | editorPlaceholder | Was denkst du? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Posten |
|  | editorPosting | Beitrag… |
|  | editorReplyBtn | Antworten |
|  | editorReplyTitle | Antwort schreiben |
|  | editorTitle | Sidenote schreiben |
|  | emptyImageBlockTxt | Was denkst du? |
|  | emptyTextBlockTxt | + |
|  | responseBtn | Antwort |
|  | threadReplyBtn | Antwort auf Unterhaltung |
| *Menüoptionen löschen* |  |  |
|  | menuConfirmAccept | Ja, {action} |
|  | menuConfirmCancel | Abbrechen |
|  | menuConfirmTitle | Sind Sie sicher? |
| *Menüoptionen etc* |  |  |
|  | menuEtcOptionApprove | Genehmigen |
|  | menuEtcOptionDelete | Löschen |
|  | menuEtcOptionEdit | Vorlage      |
|  | menuEtcOptionFlag | Markierung |
|  | menuEtcOptionShare | Freigabe |
|  | menuEtcPostedAt | Veröffentlicht am {date} |
|  | menuEtcTitle | Mehr |

## Moderatorschnittstelle {#section_o5f_dl4_xz}

Zeichenfolgen, die für die Benutzeroberfläche des authentifizierten Moderators verfügbar sind.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Bestätigungsnachrichten aus dem Menü &quot;Mehr&quot;* |  |  |
|  | notificationApproved | Genehmigt |
|  | notificationDeleted | Gelöscht |
|  | notificationGekennzeichnet | Gekennzeichnet |

## Fehler {#section_gtk_cl4_xz}

Für allgemeine Fehlermeldungen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | errorConnection | Oh-oh. Du scheinst keine gute Verbindung zu haben. |
|  | errorDuplicate | Wir mögen Ihre Notiz auch, aber Sie können sie nicht zweimal posten. |
|  | errorGeneral | Es ist ein Fehler aufgetreten. Bitte versuchen Sie es erneut. |
|  | errorServer | Mit unserem Server ist etwas schiefgelaufen. Probieren Sie das noch einmal aus? |
