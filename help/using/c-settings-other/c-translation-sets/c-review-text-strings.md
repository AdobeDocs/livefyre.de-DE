---
description: Anpassen der Textzeichenfolgen für Livefyre-Reviews.
seo-description: Anpassen der Textzeichenfolgen für Livefyre-Reviews.
seo-title: Textzeichenfolgen überprüfen
solution: Experience Manager
title: Textzeichenfolgen überprüfen
uuid: 86251 e 49-bc 73-4 eec -9 f 9 b-b 4 b 0 a 5 b 42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Textzeichenfolgen überprüfen{#review-text-strings}

Anpassen der Textzeichenfolgen für Livefyre-Reviews.

Auf dieser Seite werden die für die Anpassung verfügbaren Zeichenfolgen in den Review-Apps aufgeführt und beschrieben. Die hier aufgeführten Zeichenfolgen sind zusätzlich zu den Standardzeichenfolgen für Livefyre-Core-Apps, die in Zeichenfolgen-Anpassungen aufgeführt sind. Wenn Duplikate aufgeführt werden, sind die in diesen Tabellen aufgeführten Zeichenfolgen die Standardeinstellung für Review-Apps.

Fehler bei der Implementierung/Bewertung
von Stream-Infofeld-Stream-Info-/Content
Info-Benutzeraktionen
- Fehlermeldungen

## Implementierung {#section-vsy-1k4-xz}

Übergeben Sie zur Implementierung dieser Funktion eine 1-1 Objektzuordnung der Zeichenfolgen, die Sie dem Javascript-Konfigurationsobjekt überschreiben möchten. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

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

## Review-/Bewertungsschnittstelle {#section_iyv_zj4_xz}

Für die Benutzeroberfläche "Review and Rating" verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|--- |--- |--- |
| Schaltflächen | Editreviewbtn | Review bearbeiten |
|  | Reviewbtn | [Überprüfung schreiben](https://d.pr/i/QscA) |
|  | Reviewsclosed | [Überprüfungen geschlossen](https://d.pr/i/zr7M) |
|  | Showreviewbtn | [Überprüfung anzeigen](https://d.pr/i/onxU) |
|  | folgen | Ich bin interessiert |
|  | Sharetext | Ich habe gerade einen Review geschrieben. Überprüfen Sie es! |
| Quickinfos | Variabvalues | Ein Array. Standard = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Hinweis: Werte im Array müssen dupliziert werden, um sowohl links als auch rechte Hälfte jedes Stern denselben Namen zuzuweisen. |
| Bewertungsunterteilungen | Getrosubpartplaceholders | Ein Array. Standard = `[]` |
|  | Getrosubparttitles | Ein Array. Standard = `[]` |
|  | Reviewstreamtitle | Standardmäßig leer. Titel des Übersichtsabschnitts der Überprüfung. |
| Misc | Averagerating | [Durchschnittliche Benutzerbewertung](https://d.pr/i/QscA) |
|  | Breakdownheader | [Bewertungsaufschlüsselung](https://d.pr/i/QscA) |
|  | hilfreich | % s von % s gefunden |
|  | Helpfulplural | % s von % s gefunden |
|  | Outof | / |
|  | Variabtype | Stern |

## Stream-Info {#section_wmv_yj4_xz}

Für Content Stream-Informationen verfügbare Zeichenfolgen und Anzeigen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Sortieren | Sortby | Standardmäßig leer. |
|  | Sorthighestrated | [Höchste Bewertung](https://d.pr/i/huTd) |
|  | Sortlowestrated | [Niedrigste Bewertung](https://d.pr/i/huTd) |
|  | Sortmomentarelpful | [Am nützlichsten](https://d.pr/i/huTd) |
| Stream-Misc. | Showmore | Mehr anzeigen |
| Hohe Geschwindigkeit streamen | Newcomment | Neue Überprüfung |
|  | Newcomments | Neue Überprüfungen |
| Listener-Zähler | Listenercount | Person Listening |
|  | Listenercountplural | people listening |
| Anzahl der Kommentare | Commentcountlabel | Livereviews<strong> | </strong>% s |
|  | Commentcountlabelplural | Livereviews<strong> | </strong>% s |
| Anzahl der Benachrichtigungsbenachrichtigungen | Commentnotifier | Neue Überprüfung |
|  | Commentnotifierplural | Neue Überprüfungen |

## Autoren-/Inhaltsinformationen {#section_osx_xj4_xz}

Für Autor und individuelle Inhaltsinformationen verfügbare Stings.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Thread-Aufteilung | Reviewscontentnotfoundmsg | [Diese Überprüfung ist nicht mehr sichtbar.](https://d.pr/i/svXs) |
|  | Backtocomments | Zurück zu Reviews |

## Benutzeraktionen {#section_tlx_wj4_xz}

Für Benutzeraktionen verfügbare Zeichenfolgen: Markieren, Freigeben und Markieren bestehender Inhalte als nützlich.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Fußzeile | Wasreviewhelpful | [Hilfreich?](https://d.pr/i/Q0mA) |
|  | Wasreviewhelpfulmobile | Hilfreich? |
|  | Ownwasreviewhelpful | [Es wurde hilfreich gefunden.](https://d.pr/i/Q0mA) |
|  | Reviewwasassist | [Ja](https://d.pr/i/Q0mA) |
|  | Helpfuldivider | [& amp; vert;](https://d.pr/i/Q0mA) |
|  | Reviewwasnothelpful | [Nein](https://d.pr/i/Q0mA) |
| Abstimmung modaler Stimmen | Votetitle | Wurde diese Überprüfung hilfreich? |
|  | Votedownsession | Nein |
|  | Votereplytitle | War diese Antwort hilfreich? |
|  | Votetitle | War dieser Kommentar hilfreich? |
|  | Voteupvoice | Ja |
| Flag markieren | Flagtitle | Überprüfung von % s's |
|  | Flagsuccessmsg | Überprüfung wurde gekennzeichnet. |
| Markieren von Mobilgeräten | Flagconfirmationmessage | Die Überprüfung % s als % s kennzeichnen? |
| Erwähnung von Modal | Mentiondefaulttext | Ich habe Sie in einer Livefyre-Überprüfung erwähnt! |
| Modale Freigabe | Sharetitle | Überprüfung freigeben |

## Beitragsfunktionen {#section_yl1_wj4_xz}

Für Benutzer verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Editor | Bodyplaceholder | Review schreiben… |
|  | Posteditbutton | Bearbeiten |
|  | Posteditcancelbutton | Abbrechen |
|  | Postasbutton | Überprüfung als… |
|  | Postbutton | Beitragsprüfung |
|  | Postreplyasbutton | Als… posten |
|  | Postreplybutton | Beitrag |
|  | Sharebutton | Freigeben |
|  | Titleplaceholder | Titel… |

## Fehler {#section_jbc_vj4_xz}

Für allgemeine Fehlermeldungen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Fehler | Erroralreadypublished | Sie können nur eine Überprüfung posten. |
|  | Errorautherror | Sie sind nicht autorisiert, eine Überprüfung bei dieser Konversation zu posten. |
|  | Errorcommentsnotallowed | Reviews können derzeit nicht veröffentlicht werden |
|  | Errordislikeowncomment | Sie können Ihre eigene Überprüfung nicht stören. |
|  | Errorduplicate | Genauso wie Sie Ihren Review bewertet haben, können Sie ihn nicht zweimal posten. |
|  | Erroreditduplicate | Sie müssen den Text der Überprüfung ändern, wenn Sie sie bearbeiten. |
|  | Erroreditnotallowed | Sie dürfen keine Reviews zu dieser Konversation bearbeiten. |
|  | Erroredittimeexceeded | Der Review-Bearbeitungszeitraum ist abgelaufen. |
|  | Errorempty | Anscheinend versuchen Sie, eine leere Überprüfung zu posten. |
|  | Erroremptytitle | Anscheinend versuchen Sie, einen leeren Titel zu posten. |
|  | Errorfieldrating | Bewertungssterne |
|  | Errorfieldreview | lesen |
|  | Errorfieldtitle | Titel |
|  | Errormaxchars | Ihre Überprüfung ist zu lang. Bitte bearbeiten und versuchen Sie es erneut. |
|  | Errormissingfields | Bitte ein |
|  | Errorratingempty | Sie können keine leere Bewertung senden |
|  | Errorvariabnotset | Alle Bewertungen müssen festgelegt werden |
|  | Errorvariabnotvalid | Die Bewertung muss ein Objekt sein. |
|  | Errorshowmore | Beim Laden weiterer Überprüfungen ist ein Fehler aufgetreten. |
|  | Errortitlemaxchars | Der Titel ist zu lang. Bitte bearbeiten und versuchen Sie es erneut. |
|  | Errorvoteowncomment | Sie können nicht über Ihre eigene Überprüfung abstimmen. |

