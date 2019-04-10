---
description: Mit Übersetzungssätzen können Sie alternative Sprache für Apps angeben.
seo-description: Mit Übersetzungssätzen können Sie alternative Sprache für Apps angeben.
seo-title: Übersetzungssätze
solution: Experience Manager
title: Übersetzungssätze
uuid: 88 b 705 e 5-57 c 8-4065-8 a 41-a 73546 bd 929 a
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Übersetzungssätze{#translation-sets}

Mit Übersetzungssätzen können Sie alternative Sprache für Apps angeben.

Verwenden Sie Übersetzungseinstellungen, um Apps in verschiedenen Sprachen zu lokalisieren oder alternativen Text für mehrere Apps an einem Ort in Studio anzugeben. Sie können beispielsweise sicherstellen, dass alle spanischen Sites für alle App-Felder Spanisch-Sprache verwenden. Sie können den Text auch so ändern, dass alle Felder mit der Stimme Ihrer Site oder Ihrem Netzwerk übereinstimmen.

Sie können Übersetzungseinstellungen für alle Apps mit Ausnahme von Storify 2 angeben. Weitere Informationen zu den Feldern, die Sie lokalisieren können, finden Sie unter [Lokalisieren von Zeichenfolgen](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings).

Kommentare, Live-Blog und Chat geben dieselbe Zeichenfolge in einem Übersetzungssatz frei.

Geben Sie einen Übersetzungssatz für ein Netzwerk, eine Site, eine App oder eine API an.

Die Übersetzungssätze auf verschiedenen Ebenen setzen sich gegenseitig außer Kraft:

Der API-Übersetzungssatz setzt alle Übersetzungssätze auf jeder Ebene (App-, Netzwerk- und Site-App)
außer Kraft, wenn die Übersetzungs-Übersetzungs-Sets auf Netzwerkebene und auf Site-Ebene außer Kraft gesetzt werden.
Übersetzungs-Sets auf Site-Ebene überschreiben die Übersetzungssätze auf Netzwerkebene.

## Textzeichenfolgen überprüfen {#c_review_text_strings}

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
|  | Reviewbtn | Überprüfung schreiben |
|  | Reviewsclosed | Überprüfungen geschlossen |
|  | Showreviewbtn | Überprüfung anzeigen |
|  | folgen | Ich bin interessiert |
|  | Sharetext | Ich habe gerade einen Review geschrieben. Überprüfen Sie es! |
| Quickinfos | Variabvalues | Ein Array. Standard = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Hinweis: Werte im Array müssen dupliziert werden, um sowohl links als auch rechte Hälfte jedes Stern denselben Namen zuzuweisen. |
| Bewertungsunterteilungen | Getrosubpartplaceholders | Ein Array. Standard = [] |
|  | Getrosubparttitles | Ein Array. Standard = [] |
|  | Reviewstreamtitle | Standardmäßig leer. Titel des Übersichtsabschnitts der Überprüfung. |
| Misc | Averagerating | Durchschnittliche Benutzerbewertung |
|  | Breakdownheader | Bewertungsaufschlüsselung |
|  | hilfreich | % s von % s gefunden |
|  | Helpfulplural | % s von % s gefunden |
|  | Outof | / |
|  | Variabtype | Stern |

## Stream-Info {#section_wmv_yj4_xz}

Für Content Stream-Informationen verfügbare Zeichenfolgen und Anzeigen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Sortieren | Sortby | *Standardmäßig leer.* |
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

## Textzeichenfolgen-Zeichenfolgen {#c_sidenotes_text_strings}

Anpassen der Textzeichenfolgen für Livefyre-Kritiker

Auf dieser Seite werden alle für die Anpassung in den DOM-Apps verfügbaren Zeichenfolgen aufgeführt und beschrieben. Informationen zu Zeichenfolgen für die Core-Livefyre-Apps finden Sie unter Zeichenfolgenanpassungen.

Moderationsoberflächen für Implementierungs-Authentifizierungs-/Content
Info-Benutzeraktionen
- Moderations-Benutzeraktionen
- Fehler

## Implementierung {#section_wp2_ql4_xz}

Übergeben Sie zur Implementierung dieser Funktion eine 1-1 Objektzuordnung der Zeichenfolgen, die Sie dem Javascript-Konfigurationsobjekt überschreiben möchten. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

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

Für den Authentifizierungsprozess verfügbare Zeichenfolgen und aus den authentifizierten Benutzermenüs.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Auth-Menüzeichenfolgen | Menuauthsigninbtn | Anmelden |
|  | Menuauthsignedinmsg | Sie müssen bei {action} angemeldet sein. |
|  | Menuusereditprofile | Profil bearbeiten |
|  | Menuuseradmin | Admin-Konsole |
|  | Menuuserlogout | Abmelden |
|  | Menuuserbackbtn | Alle |

## Stream-Info {#section_wpy_gl4_xz}

Für Content Stream-Informationen verfügbare Zeichenfolgen und Anzeigen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Optionen für Infomenüs | Menuinfocopyright | © Livefyre, Inc. 2014 |
|  | Menuinfohelp | Hilfe |
|  | Menuinfolivefyrelink | Besuchen Sie Livefyre.com |

## Autoren-/Inhaltsinformationen {#section_dhb_gl4_xz}

Für Autor und individuelle Inhaltsinformationen verfügbare Stings.

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | Commentmoderatortag | Mod |
|  | Commentpendingtag | Ausstehend |
|  | Commentreadmorelink | Mehr lesen |
|  | Commentreplylink | Siehe {number} Antworten |
|  | Commentreplylinksing | Siehe Antwort |
|  | Commentvotecount | Stimmen |
|  | Commentvotecountsing | abstimmen |
|  | Datetimeminuteprefix | m |
|  | Datetimemonths | Ein Array. Standard =[ ' Januar ',' Februar ',' März ',' April ',' Mai ',' Juni ',' Juli ',' August ',' September ',' Oktober ',' November ',' Dezember ' ] |
|  | Questionexplain | Sie können Kommentare jetzt direkt in Sätzen, Absätzen, Bildern und Anführungszeichen lesen und schreiben.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Markieren Sie Text</span> und klicken Sie auf das <span class="&rdquo;fycon-write&rdquo;"></span> Symbol oder klicken Sie am Ende jedes Absatzes auf das <span class="&rdquo;fycon-action-view&rdquo;"></span> Symbol. |
|  | Questionmocktext | Was genau bekannt ist, wird nicht korrekt bekannt, sondern nur aus dem Grund, aus dem sie "bekannt" ist. |
|  | Questiontitle | Was ist eine Sidenote? |

## Benutzeraktionen {#section_qxd_fl4_xz}

Für Benutzeraktionen verfügbare Zeichenfolgen: Kennzeichnung, Freigabe und Nutzung vorhandener Inhalte.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Optionen für Antworten auf Antworten | Menurepliesviewtitle | Details |
|  | Menurepliesviewreply | Besprechungen beantworten |
| Optionen für Freigeben-Menüs | Menushareoptionfacebook | Facebook |
|  | Menushareoptiontwitter | Twitter |
|  | Menusharetitle | Freigeben |
| Optionen für die Markierung | Menuflagoptiondisagree | Nicht zustimmen |
|  | Menuflagoptionoffensive | Offensive |
|  | Menuflagoptionofftopic | Aus Thema |
|  | Menuflagoptionspam | Spam |
|  | Menuflagtitle | Markieren als… |
|  | Facebooksharecaption | Zielgruppen für " {title} « |
| Mobile Benutzeroptionen | Slidercommenttally | of |
|  | Sliderinviteread | Lesen |
|  | Sliderinvitewrite | Schreiben |
|  | Sliderloading | Wird geladen… |
|  | Sliderwritetext | Was glauben Sie? Zum Schreiben tippen. |

## Beitragsfunktionen {#section_xzf_2l4_xz}

Zeichenfolgen, die für Benutzer, die Inhalte posten, verfügbar sind.

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | Editoreditbtn | Speichern |
|  | Editoreditposting | Speichern… |
|  | Editoreditreplytitle | Antwort bearbeiten |
|  | Editoredittitle | Insider bearbeiten |
|  | Editorplaceholder | Was glauben Sie? |
|  | Editorpostbtn | Posts posten |
|  | Editorpostbtnmobile | Beitrag |
|  | Editorposting | Beitrag… |
|  | Editorreplybtn | Post-Antwort |
|  | Editorreplytitle | Antwort schreiben |
|  | Editortitle | Autote schreiben |
|  | Emptyimageblocktxt | Was glauben Sie? |
|  | Emptytextblocktxt | + |
|  | Replybtn | Antworten |
|  | Threadreplybtn | Besprechungen beantworten |
| Menüoptionen löschen | Menuconfirmaccept | Ja, {action} |
|  | Menuconfirmcancel | Abbrechen |
|  | Menuconfirmtitle | Sind Sie sicher? |
| Menüoptionen | Menuetcoptionapprove | Genehmigen |
|  | Menuetcoptiondelete | Löschen |
|  | Menuetcoptionedit | Bearbeiten |
|  | Menuetcoptionflag | Flag |
|  | Menuetcoptionshare | Freigeben |
|  | Menuetcpostedat | Gepostet am {date} |
|  | Menuetctitle | Mehr |

## Moderatorschnittstelle {#section_o5f_dl4_xz}

Für die benutzerauthentifizierte Moderationsoberfläche verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Bestätigungsmeldungen im Menü "Mehr « | Notificationapproved | Genehmigt |
|  | Notificationdeleted | Gelöscht |
|  | Notificationflag | Gekennzeichnet |

## Fehler {#section_gtk_cl4_xz}

Für allgemeine Fehlermeldungen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | Errorconnection | Uh-oh. Sie haben keine gute Verbindung. |
|  | Errorduplicate | Wir haben auch Ihre Notiz, aber Sie können sie nicht zweimal posten. |
|  | Errorgeneral | Es ist ein Fehler aufgetreten. Bitte erneut versuchen. |
|  | Errorserver | Bei unserem Server ist etwas falsch. Versuchen Sie es erneut? |

