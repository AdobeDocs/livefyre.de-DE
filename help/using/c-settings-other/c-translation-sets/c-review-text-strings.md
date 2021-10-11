---
description: Anpassen der Textzeichenfolgen für Livefyre-Prüfungen.
title: Überprüfen von Textzeichenfolgen
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
source-git-commit: 1d9088eecf797e1af881cb6be55b3c96284f75e5
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 5%

---

# Überprüfen von Textzeichenfolgen{#review-text-strings}

Anpassen der Textzeichenfolgen für Livefyre-Prüfungen.

Auf dieser Seite werden die zur Anpassung in Review-Apps verfügbaren Zeichenfolgen aufgelistet und beschrieben. Die hier aufgeführten Zeichenfolgen werden zusätzlich zu den Standardzeichenfolgen für Livefyre-Core-Apps und deren Überschreibungen angezeigt, die unter Zeichenfolgenanpassung aufgeführt sind. Wo Duplikate aufgelistet sind, sind die in diesen Tabellen aufgeführten Zeichenfolgen die Standardwerte für die Reviews-Apps.

Implementierung
Benutzeroberfläche für Überprüfung/Bewertung
Stream-Informationen
Autor-/Inhaltsinformationen
Benutzeraktionen
Post-Funktionen
Fehler

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
|--- |--- |--- |
| Schaltflächen | editReviewBtn | Prüfung bearbeiten |
|  | reviewBtn | Überprüfung schreiben |
|  | viewsClosed | Abgeschlossene Überprüfungen |
|  | showReviewBtn | Überprüfung anzeigen |
|  | folgen | Ich interessiere mich |
|  | shareText | Ich habe gerade eine Überprüfung geschrieben. Schau es dir an! |
| QuickInfos zur Bewertung | ratingValues | Als Array. Standard = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Hinweis: Die Werte im Array müssen dupliziert werden, damit sowohl die linke als auch die rechte Hälfte jedes Sterns denselben Namen erhalten. |
| Bewertungsunterteile | ratingSubpartPlaceholders | Als Array. Standardeinstellung = `[]` |
|  | ratingSubpartTitles | Als Array. Standardeinstellung = `[]` |
|  | reviewStreamTitle | Standardmäßig leer. Titel des Zusammenfassungsabschnitts der Überprüfung. |
| Verschiedenes | averageRating | Durchschnittliche Benutzerbewertung |
|  | breakHeader | Bewertungsaufschlüsselung |
|  | help | %s von %s gefunden hilfreich |
|  | assistancePlural | %s von %s gefunden hilfreich |
|  | outOf | / |
|  | ratingType | star |

## Stream-Informationen {#section_wmv_yj4_xz}

Zeichenfolgen, die für Informationen und Anzeigen des Inhalts-Streams verfügbar sind.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Sortieren | sortBy | Standardmäßig leer. |
|  | sortHighestRated | Höchste Bewertung |
|  | sortLowestRated | Niedrigste Bewertung |
|  | sortMostHelpful | Am meisten hilfreich |
| Stream misc. | showMore | Mehr anzeigen |
| Stream-Hochgeschwindigkeit | newComment | Neue Prüfung |
|  | newComments | Neue Überprüfungen |
| Listener-Anzahl | listenerCount | Personen, die |
|  | listenerCountPlural | Personen, die zuhören |
| Anzahl der Kommentare | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Anzahl der Benachrichtigungen | commentNotifier | Neue Prüfung |
|  | commentNotifierPlural | Neue Überprüfungen |

## Autor-/Inhaltsinformationen {#section_osx_xj4_xz}

Für Autoren- und individuelle Inhaltsinformationen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Thread-Aufschlüsselung | viewsContentNotFoundMsg | Diese Überprüfung ist nicht mehr sichtbar. |
|  | backToComments | Zurück zu Prüfungen |

## Benutzeraktionen {#section_tlx_wj4_xz}

Für Benutzeraktionen verfügbare Zeichenfolgen: Kennzeichnen, Freigeben und Kennzeichnen vorhandener Inhalte als hilfreich.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Kommentar-Fußzeile | wasReviewHelpful | Nützlich? |
|  | wasReviewHelpfulMobile | Nützlich? |
|  | ownWarReviewHelpful | Es fand hilfreich. |
|  | reviewWarHelpful | Ja |
|  | assistanceDivider | &amp;vert; |
|  | reviewWarNotHelpful | Nein |
| modale Abstimmung | optionTitle | War diese Überprüfung hilfreich? |
|  | optionDownvoice | Nein |
|  | optionReplyTitle | War diese Antwort hilfreich? |
|  | optionTitle | War dieser Kommentar hilfreich? |
|  | VVTutum | Ja |
| Modal kennzeichnen | flagTitle | Überprüfung von %s kennzeichnen |
|  | flagSuccessMsg | Die Überprüfung wurde gekennzeichnet. |
| Flag Mobile | flagConfirmationMessage | %s Überprüfung als %s kennzeichnen? |
| Erwähnungsmodal | mentionDefaultText | Ich habe Sie in einem Livefyre-Review erwähnt. |
| Modal freigeben | shareTitle | Weitergeben |

## Post-Funktionen {#section_yl1_wj4_xz}

Zeichenfolgen stehen Benutzern zur Verfügung, die Rezensionen posten.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Editor | bodyPlaceholder | Überprüfung schreiben... |
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
| Fehler | errorAlreadyPosted | Sie können nur eine Überprüfung posten. |
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
