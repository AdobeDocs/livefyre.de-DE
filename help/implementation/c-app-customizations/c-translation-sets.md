---
description: Mit Übersetzungssätzen können Sie eine andere Sprache für Apps festlegen.
title: Übersetzungssätze
exl-id: 688138bf-f8e9-4fe5-99e2-2451deefd217
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 7%

---

# Übersetzungssätze {#translation-sets}

Mit Übersetzungssätzen können Sie eine andere Sprache für Apps festlegen.

<!-- 
c_translation_sets.dita
-->

Verwenden Sie Übersetzungseinstellungen, um Apps in verschiedenen Sprachen zu lokalisieren oder um alternativen Text für mehrere Apps von einer Position in Studio aus anzugeben. Sie können beispielsweise sicherstellen, dass alle Sites in spanischer Sprache für alle App-Felder Spanisch verwenden. Sie können den Text auch so ändern, dass alle Felder der Stimme und dem Gefühl Ihrer Site oder Ihres Netzwerks entsprechen.

Sie können Übersetzungseinstellungen für alle Apps mit Ausnahme von Storify 2 angeben. Weitere Informationen darüber, welche Felder lokalisiert werden können, finden Sie unter [Strings lokalisieren](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md).

Kommentare, Live-Blog und Chat verwenden dieselben Zeichenfolgen innerhalb eines Übersetzungssatzes.

Geben Sie einen Übersetzungssatz für ein Netzwerk, eine Site, eine App oder eine API an.

Die Übersetzungssätze auf verschiedenen Ebenen setzen sich gegenseitig außer Kraft, indem sie diesem Muster folgen:

* Übersetzungsset der API setzt alle Übersetzungssätze auf jeder Ebene (App, Netzwerk und Site) außer Kraft
* Der Übersetzungssatz der App setzt Übersetzungssätze auf Netzwerk- und Site-Ebene außer Kraft.
* Übersetzungssätze auf Site-Ebene setzen Übersetzungssätze auf Netzwerkebene außer Kraft.

## Überprüfen von Textzeichenfolgen {#c-review-text-strings}

Anpassen der Textzeichenfolgen für Livefyre-Reviews.

Auf dieser Seite werden die zur Anpassung in Review-Apps verfügbaren Zeichenfolgen Liste und beschrieben. Die hier aufgeführten Zeichenfolgen werden zusätzlich zu den Standardzeichenfolgen für Livefyre-Core-Apps und deren Überschreibungen angezeigt, die unter Zeichenfolgenanpassung aufgeführt sind. Wo Duplikat aufgeführt sind, sind die in diesen Tabellen aufgeführten Zeichenfolgen die Standardwerte für Reviews-Apps.

* Implementierung
* Benutzeroberfläche für Review/Bewertung
* Stream-Info
* Autor-/Inhaltsinformationen
* Benutzeraktionen
* Post-Funktionen
* Fehler

## Implementierung {#section-vsy-1k4-xz}

Übergeben Sie zur Implementierung dieser Funktion eine 1-1-Objektzuordnung der Zeichenfolgen, die Sie überschreiben möchten, an das JavaScript-Konfigurationsobjekt. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

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

## Überprüfungs-/Bewertungsschnittstelle {#section_iyv_zj4_xz}

Für die Benutzeroberfläche &quot;Review and Rating&quot;verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Schaltflächen |  |  |
|  | editReviewBtn | Review bearbeiten |
|  | reviewBtn | Überprüfung schreiben |
|  | reviewsClosed | Abgeschlossene Reviews |
|  | showReviewBtn | Review anzeigen |
|  | follow | Ich interessiere mich |
|  | shareText | Ich habe gerade eine Rezension geschrieben. Schau es dir an! |
| Ratings-QuickInfos |  |  |
|  | ratingValues | Als Array. Standard = [&quot;Poor&quot;, &quot;Poor&quot;, &quot;Fair&quot;, &quot;Fair&quot;, &quot;Average&quot;, &quot;Average&quot;, &quot;Good&quot;, &quot;Good&quot;, &quot;Excellent&quot;, &quot;Excellent&quot;]; |
|  |  | Hinweis: Die Werte im Array müssen dupliziert werden, damit sowohl die linke als auch die rechte Hälfte jedes Sterns denselben Namen erhält. |
| Bewertungsunterteile |  |  |
|  | ratingSubpartPlaceholders | Als Array. Standardeinstellung = [] |
|  | ratingSubpartTitles | Als Array. Standardeinstellung = [] |
|  | reviewStreamTitle | Standardmäßig leer. Titel des Übersichtsabschnitts der Überprüfung. |
| Misc |  |  |
|  | averageRating | Durchschnittliche Benutzerbewertung |
|  | breakHeader | Bewertungsaufschlüsselung |
|  | help | %s von %s als hilfreich gefunden |
|  | assistancePlural | %s von %s als hilfreich gefunden |
|  | outOf | / |
|  | ratingType | star |

## Stream-Info {#section_wmv_yj4_xz}

Für Informationen und Anzeigen von Inhaltsströmen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Sortieren* |  |  |
|  | sortBy | *Standardmäßig leer.* |
|  | sortHighestRated | [Höchste Bewertung](https://d.pr/i/huTd) |
|  | sortLowestRated | [Niedrigste Bewertung](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Am meisten hilfreich](https://d.pr/i/huTd) |
| *Stream-Fehler.* |  |  |
|  | showMore | Mehr anzeigen |
| *Stream mit hoher Geschwindigkeit* |  |  |
|  | newComment | Neue Überprüfung |
|  | newComments | Neue Reviews |
| *Listener-Zähler* |  |  |
|  | listenerCount | Person hört |
|  | listenerCountPlural | zuhörende Personen |
| *Anzahl der Kommentare* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *Anzahl der Notifizierer* |  |  |
|  | commentNotifier | Neue Überprüfung |
|  | commentNotifierPlural | Neue Reviews |

## Autor-/Inhaltsinformationen {#section_osx_xj4_xz}

Stings verfügbar für Autor- und individuelle Inhaltsinformationen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Thread-Aufschlüsselung* |  |  |
|  | reviewsContentNotFoundMsg | [Diese Überprüfung ist nicht mehr sichtbar](https://d.pr/i/svXs) |
|  | backToComments | Zurück zu Reviews |

## Benutzeraktionen {#section_tlx_wj4_xz}

Für Benutzeraktionen verfügbare Zeichenfolgen: Kennzeichnung, Freigabe und Kennzeichnung vorhandener Inhalte als hilfreich.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Fußzeile kommentieren* |  |  |
|  | wasReviewHelpful | [Hilfreich?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Hilfreich? |
|  | ownWarReviewHelpful | [Hilfreich gefunden.](https://d.pr/i/Q0mA) |
|  | reviewWarHelpful | [Ja](https://d.pr/i/Q0mA) |
|  | assistDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWarNotHelpful | [Nein](https://d.pr/i/Q0mA) |
| *modale Abstimmung* |  |  |
|  | optTitle | War diese Überprüfung hilfreich? |
|  | optionDownAbstimmung | Nein |
|  | optionReplyTitle | War diese Antwort hilfreich? |
|  | optTitle | War dieser Kommentar hilfreich? |
|  | optionUpVT | Ja |
| *Modale Kennzeichnung* |  |  |
|  | FlagTitle | Überprüfung von %s markieren |
|  | FlagSuccessMsg | Die Überprüfung wurde markiert. |
| *Mobiles Flag* |  |  |
|  | flagConfirmationMessage | %s Überprüfung als %s kennzeichnen? |
| *Erwähnungsmodal* |  |  |
|  | ErwähnungDefaultText | Ich habe Sie in einem Livefyre Review erwähnt! |
| *Modal freigeben* |  |  |
|  | shareTitle | Review freigeben |

## Post-Funktionen {#section_yl1_wj4_xz}

Zeichenfolgen für Benutzer, die Reviews posten.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Editor* |  |  |
|  | bodyPlaceholder | Überprüfung schreiben... |
|  | postEditButton | Vorlage      |
|  | postEditCancelButton | Abbrechen |
|  | postAsButton | Beitragsüberprüfung als... |
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
|  | errorAlreadyPosted | Sie können nur einen Review posten. |
|  | errorAuthError | Sie sind nicht berechtigt, einen Review zu dieser Unterhaltung zu posten |
|  | errorCommentsNotAllowed | Reviews können derzeit nicht gepostet werden |
|  | errorDislikeOwnComment | Sie können Ihre eigene Überprüfung nicht ablehnen |
|  | errorDuplicate | So sehr Sie Ihren Review mögen, können Sie ihn nicht zweimal posten. |
|  | errorEditDuplicate | Sie müssen den Text des Reviews ändern, wenn Sie ihn bearbeiten. |
|  | errorEditNotAllowed | Sie dürfen keine Rezensionen zu dieser Unterhaltung bearbeiten. |
|  | errorEditTimeExceeded | Ihre Revisionsbearbeitungszeit ist leider abgelaufen. |
|  | errorEmpty | Es scheint, dass Sie versuchen, eine leere Überprüfung zu posten. |
|  | errorEmptyTitle | Sie versuchen anscheinend, einen leeren Titel zu posten |
|  | errorFieldRating | Sternbewertung |
|  | errorFieldReview | überprüfen |
|  | errorFieldTitle | title |
|  | errorMaxChars | Entschuldige! Deine Überprüfung ist zu lang. Bearbeiten Sie die Datei und versuchen Sie es erneut. |
|  | errorMissingFields | Bitte geben Sie eine |
|  | errorRatingEmpty | Sie können keine leere Bewertung senden |
|  | errorRatingNotSet | Alle Ratings müssen eingestellt werden |
|  | errorRatingNotValid | Die Bewertung muss ein Objekt sein |
|  | errorShowMore | Beim Laden weiterer Überprüfungen ist ein Fehler aufgetreten. |
|  | errorTitleMaxChars | Tut mir leid, dein Titel ist zu lang. Bearbeiten Sie die Datei und versuchen Sie es erneut. |
|  | errorVoteOwnComment | Sie können nicht über Ihre eigene Überprüfung abstimmen |

## Seitenzeichenfolgen {#c_sidenotes_text_strings}

Anpassen der Textzeichenfolgen für Livefyre Sibezeichnet

<!-- 

c_sidenotes_text_strings.dita

 -->

Auf dieser Seite werden alle Zeichenfolgen, die zur Anpassung in Sidebar-Apps verfügbar sind, Liste und beschrieben. Informationen zu Zeichenfolgen, die für die Core-Livefyre-Apps verfügbar sind, finden Sie unter Zeichenfolgen-Anpassungen.

* Implementierung
* Auth
* Stream-Info
* Autor-/Inhaltsinformationen
* Benutzeraktionen
* Post-Funktionen
* Moderator-Oberfläche
* Fehler

## Implementierung {#section_wp2_ql4_xz}

Übergeben Sie zur Implementierung dieser Funktion eine 1-1-Objektzuordnung der Zeichenfolgen, die Sie überschreiben möchten, an das JavaScript-Konfigurationsobjekt. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

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

Für den Authentifizierungsprozess verfügbare Zeichenfolgen und in den authentifizierten Benutzermenüs.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Auth-Menüzeichenfolgen* |  |  |
|  | menuAuthSignInBtn | Anmelden |
|  | menuAuthSignedInMsg | Sie müssen bei {action} angemeldet sein |
|  | menuUserEditProfile | Profil bearbeiten |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Abmelden |
|  | menuUserBackBtn | Alle |

## Stream-Info {#section_wpy_gl4_xz}

Für Informationen und Anzeigen von Inhaltsströmen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Optionen im Menü &quot;Info&quot;* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Hilfe |
|  | menuInfoLivefyreLink | Besuch Livefyre.com |

## Autor-/Inhaltsinformationen {#section_dhb_gl4_xz}

Stings verfügbar für Autor- und individuelle Inhaltsinformationen.

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | In Bearbeitung |
|  | commentReadMoreLink | Weitere Info |
|  | commentReplyLink | Siehe {number} Antworten |
|  | commentReplyLinkSing | Siehe Antwort |
|  | commentVoteCount | stimmen |
|  | commentVoteCountSing | Stimme |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *Als Array. Standard = *[ &quot;Januar&quot;, &quot;Februar&quot;, &quot;März&quot;, &quot;April&quot;, &quot;Mai&quot;, &quot;Juni&quot;, &quot;Juli&quot;, &quot;August&quot;, &quot;September&quot;, &quot;Oktober&quot;, &quot;November&quot;, &quot;Dezember&quot;] |
|  | QuestionExplanation | Sie können Kommentare jetzt direkt zu Sätzen, Absätzen, Bildern und Anführungszeichen lesen und schreiben. <br>Markieren Sie den Text und klicken Sie auf das Symbol oder klicken Sie auf das Symbol am Ende jedes Absatzes. |
|  | QuestionMockText | Was &quot;vertraut&quot; ist, ist nicht richtig bekannt, nur weil es &quot;vertraut&quot; ist. |
|  | QuestionTitle | Was ist ein Sidenote? |

## Benutzeraktionen {#section_qxd_fl4_xz}

Für Benutzeraktionen verfügbare Zeichenfolgen: Markieren, Freigeben und Verknüpfen vorhandener Inhalte.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Optionen des Antwortmenüs* |  |  |
|  | menuRepliesViewTitle | Details |
|  | menuRepliesViewReply | Antwort auf Konversation |
| *Menüoptionen freigeben* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Freigabe |
| *Optionen im Menü &quot;Flag&quot;* |  |  |
|  | menuFlagOptionDismatch | widersprechen |
|  | menuFlagOptionOffensive | Offensive |
|  | menuFlagOptionOffTopic | Off-Thema |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Kennzeichnung als... |
|  | facebookShareCaption | Simit auf &quot;{title}&quot; |
| *Mobile Benutzeroptionen* |  |  |
|  | reglerCommentTally | of |
|  | reglerInviteRead | Gelesen |
|  | reglerInviteWrite | schreiben |
|  | reglerLoading | Wird geladen… |
|  | reglerWriteText | Was denkst du? Tippen Sie zum Schreiben. |

## Post-Funktionen {#section_xzf_2l4_xz}

Für Benutzer, die Inhalte veröffentlichen, verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | editorEditBtn | Speichern |
|  | editorEditPosting | Speichern... |
|  | editorEditReplyTitle | Antwort bearbeiten |
|  | editorEditTitle | Sidente bearbeiten |
|  | editorPlaceholder | Was denkst du? |
|  | editorPostBtn | Post Sidennote |
|  | editorPostBtnMobile | Posten |
|  | editorPosting | Beitrag… |
|  | editorReplyBtn | Antworten |
|  | editorReplyTitle | Antwort schreiben |
|  | editorTitle | Sidenote schreiben |
|  | emptyImageBlockTxt | Was denkst du? |
|  | emptyTextBlockTxt | + |
|  | responseBtn | Antwort |
|  | threadReplyBtn | Antwort auf Konversation |
| *Menüoptionen löschen* |  |  |
|  | menuConfirmAccept | Ja, {Aktion} |
|  | menuConfirmCancel | Abbrechen |
|  | menuConfirmTitle | Sind Sie sicher? |
| *Optionen des ETC-Menüs* |  |  |
|  | menuEtcOptionApprove | Genehmigen |
|  | menuEtcOptionDelete | Löschen |
|  | menuEtcOptionEdit | Vorlage      |
|  | menuEtcOptionFlag | Markierung |
|  | menuEtcOptionShare | Freigabe |
|  | menuEtcPostedAt | Gepostet am {Datum} |
|  | menuEtcTitle | Mehr |

## Moderatorschnittstelle {#section_o5f_dl4_xz}

Zeichenfolgen, die für die benutzerdefinierte Moderatoroberfläche verfügbar sind.

| Element | Schlüssel | Standardtext |
|---|---|---|
| *Bestätigungsmeldungen im Menü &quot;Mehr&quot;* |  |  |
|  | notificationApproved | Genehmigt |
|  | notificationDeleted | Gelöscht |
|  | notificationGekennzeichnet | Gekennzeichnet |

## Fehler {#section_gtk_cl4_xz}

Für allgemeine Fehlermeldungen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | errorConnection | Oh-oh. Du scheinst keine gute Verbindung zu haben. |
|  | errorDuplicate | Ihre Notiz gefällt uns ebenfalls, aber Sie können sie nicht zweimal posten. |
|  | errorGeneral | Es ist ein Fehler aufgetreten. Bitte versuchen Sie es erneut. |
|  | errorServer | Etwas ist mit unserem Server schiefgelaufen. Versuch das noch einmal? |
