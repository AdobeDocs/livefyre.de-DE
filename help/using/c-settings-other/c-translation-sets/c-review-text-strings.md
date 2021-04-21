---
description: Anpassen der Textzeichenfolgen für Livefyre-Reviews.
title: Textzeichenfolgen überprüfen
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 5%

---

# Überprüfen von Textzeichenfolgen{#review-text-strings}

Anpassen der Textzeichenfolgen für Livefyre-Reviews.

Auf dieser Seite werden die zur Anpassung in Review-Apps verfügbaren Zeichenfolgen Liste und beschrieben. Die hier aufgeführten Zeichenfolgen werden zusätzlich zu den Standardzeichenfolgen für Livefyre-Core-Apps und deren Überschreibungen angezeigt, die unter Zeichenfolgenanpassung aufgeführt sind. Wo Duplikat aufgeführt sind, sind die in diesen Tabellen aufgeführten Zeichenfolgen die Standardwerte für Reviews-Apps.

Implementierung
Benutzeroberfläche für Review/Bewertung
Stream-Info
Autor-/Inhaltsinformationen
Benutzeraktionen
Post-Funktionen
Fehler

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
|--- |--- |--- |
| Schaltflächen | editReviewBtn | Review bearbeiten |
|  | reviewBtn | [Überprüfung schreiben](https://d.pr/i/QscA) |
|  | reviewsClosed | [Abgeschlossene Reviews](https://d.pr/i/zr7M) |
|  | showReviewBtn | [Review anzeigen](https://d.pr/i/onxU) |
|  | follow | Ich interessiere mich |
|  | shareText | Ich habe gerade eine Rezension geschrieben. Schau es dir an! |
| Ratings-QuickInfos | ratingValues | Als Array. Standard = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Hinweis: Die Werte im Array müssen dupliziert werden, damit sowohl die linke als auch die rechte Hälfte jedes Sterns denselben Namen erhalten. |
| Bewertungsunterteile | ratingSubpartPlaceholders | Als Array. Standardeinstellung = `[]` |
|  | ratingSubpartTitles | Als Array. Standardeinstellung = `[]` |
|  | reviewStreamTitle | Standardmäßig leer. Titel des Übersichtsabschnitts der Überprüfung. |
| Misc | averageRating | [Durchschnittliche Benutzerbewertung](https://d.pr/i/QscA) |
|  | breakHeader | [Bewertungsaufschlüsselung](https://d.pr/i/QscA) |
|  | help | %s von %s als hilfreich gefunden |
|  | assistancePlural | %s von %s als hilfreich gefunden |
|  | outOf | / |
|  | ratingType | star |

## Stream-Info {#section_wmv_yj4_xz}

Für Informationen und Anzeigen von Inhaltsströmen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Sortieren | sortBy | Standardmäßig leer. |
|  | sortHighestRated | [Höchste Bewertung](https://d.pr/i/huTd) |
|  | sortLowestRated | [Niedrigste Bewertung](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Am meisten hilfreich](https://d.pr/i/huTd) |
| Stream-Fehler. | showMore | Mehr anzeigen |
| Stream mit hoher Geschwindigkeit | newComment | Neue Überprüfung |
|  | newComments | Neue Reviews |
| Listener-Zähler | listenerCount | Person hört |
|  | listenerCountPlural | zuhörende Personen |
| Anzahl der Kommentare | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Anzahl der Notifizierer | commentNotifier | Neue Überprüfung |
|  | commentNotifierPlural | Neue Reviews |

## Autor-/Inhaltsinformationen {#section_osx_xj4_xz}

Stings verfügbar für Autor- und individuelle Inhaltsinformationen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Thread-Aufschlüsselung | reviewsContentNotFoundMsg | [Diese Überprüfung ist nicht mehr sichtbar](https://d.pr/i/svXs) |
|  | backToComments | Zurück zu Reviews |

## Benutzeraktionen {#section_tlx_wj4_xz}

Für Benutzeraktionen verfügbare Zeichenfolgen: Kennzeichnung, Freigabe und Kennzeichnung vorhandener Inhalte als hilfreich.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Fußzeile kommentieren | wasReviewHelpful | [Hilfreich?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | Hilfreich? |
|  | ownWarReviewHelpful | [Hilfreich gefunden.](https://d.pr/i/Q0mA) |
|  | reviewWarHelpful | [Ja](https://d.pr/i/Q0mA) |
|  | assistDivider | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWarNotHelpful | [Nein](https://d.pr/i/Q0mA) |
| modale Abstimmung | optTitle | War diese Überprüfung hilfreich? |
|  | optionDownAbstimmung | Nein |
|  | optionReplyTitle | War diese Antwort hilfreich? |
|  | optTitle | War dieser Kommentar hilfreich? |
|  | optionUpVT | Ja |
| Modale Kennzeichnung | FlagTitle | Überprüfung von %s markieren |
|  | FlagSuccessMsg | Die Überprüfung wurde markiert. |
| Mobiles Flag | flagConfirmationMessage | %s Überprüfung als %s kennzeichnen? |
| Erwähnungsmodal | ErwähnungDefaultText | Ich habe Sie in einem Livefyre Review erwähnt! |
| Modal freigeben | shareTitle | Review freigeben |

## Post-Funktionen {#section_yl1_wj4_xz}

Zeichenfolgen für Benutzer, die Reviews posten.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Editor | bodyPlaceholder | Überprüfung schreiben... |
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
| Fehler | errorAlreadyPosted | Sie können nur einen Review posten. |
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
