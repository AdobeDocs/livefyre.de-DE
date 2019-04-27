---
description: Anpassen der Zeichenfolgen der Livefyre-Apps.
seo-description: Anpassen der Zeichenfolgen der Livefyre-Apps.
seo-title: Zeichenfolgen lokalisieren
solution: Experience Manager
title: Zeichenfolgen lokalisieren
uuid: c 0 ab 352 d -5 d 3 a -45 d 7-bbd 0-aed 165835646
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Zeichenfolgen lokalisieren{#localize-strings}

Anpassen der Zeichenfolgen der Livefyre-Apps.

Die Textzeichenfolgen für die meisten HTML-Elemente in jeder Livefyre-App können angepasst werden. Dies bietet die Flexibilität, den Text gerenderter HTML-Elemente wie die Schaltfläche &quot;Veröffentlichen als&quot; , den Text&quot; Kommentarzähler&quot; oder die Schaltfläche &quot;Anmelden&quot; zu jeder gültigen UTF -8-Zeichenfolge zu ändern. Verwenden Sie diese Funktion, um Ihrer Implementierung des Streams persönliche Persönlichkeit hinzuzufügen oder um die Sprache in der App für Ihre Benutzerbasis zu lokalisieren.

* Kommentare, Chat und Live Blog

   * [Implementierung](#c-localize-strings/section_im4_224_xz)
   * [Kontozugriff](#c-localize-strings/section_cm3_d24_xz)
   * [Stream-Info](#c-localize-strings/section_wx1_c24_xz)
   * [Stream-Sortierung](#c-localize-strings/section_ih2_124_xz)
   * [Inhaltsinformationen](#c-localize-strings/section_llv_yd4_xz)
   * [Dargebotenen Inhalt](#c-localize-strings/section_gmw_vd4_xz)
   * [Texteditor](#c-localize-strings/section_ky5_td4_xz)
   * [Antwortoptionen](#c-localize-strings/section_zvt_qd4_xz)
   * [Kommentar-Benachrichtigung](#c-localize-strings/section_qqt_pd4_xz)
   * [Fehlermeldungen](#c-localize-strings/section_omz_jxn_xz)

* [Uhrzeit- und Datumsformat](#c-localize-strings/section_yz4_g5n_xz)
* [Medienpinnwand](#c-localize-strings/section_vwt_d5n_xz)
* [Map](#c-localize-strings/section_fxv_c5n_xz)
* [Mosaik](#c-localize-strings/section_e2s_b5n_xz)
* [Karussell](#c-localize-strings/section_l2z_hkn_xz)
* [Feature Card](#c-localize-strings/section_mw2_hkn_xz)
* [Umfrage](#c-localize-strings/section_pdg_fwh_xz)
* [Livefyre-Identität](#c-localize-strings/section_zc3_xvh_xz)
* Mehr:
   * [Textzeichenfolgen überprüfen](/help/using/c-settings-other/c-translation-sets/c-review-text-strings.md#c_review_text_strings)
   * [Zielgruppen](/help/using/c-settings-other/c-translation-sets/c-sidenotes-text-strings.md#c_sidenotes_text_strings)

## Implementierung {#section_im4_224_xz}

Übergeben Sie zur Implementierung dieser Funktion eine 1-1 Objektzuordnung der Zeichenfolgen, die Sie dem javascript-Konfigurationsobjekt überschreiben möchten. Wenn Sie kein Feld angeben, wird der Standardtext verwendet.

Beispiel:

```
var customStrings = {     
   postAsButton: "New Post As Text",     
   postEditButton: "New Post Edit Text"  
};   
   convConfig["strings"] = customStrings; fyre.conv.load(     
   networkConfig,     
   [convConfig],     
   function(){}  
);
```

Auf dieser Seite werden alle Textzeichenfolgen aufgelistet, die für die Livefyre-Core-Apps angepasst werden können.

## Kontozugriff {#section_cm3_d24_xz}

Für den Authentifizierungsprozess verfügbare Zeichenfolgen und aus den authentifizierten Benutzermenüs.

![](assets/strings_threadheader-150x40.png)

| Element | Schlüssel | Standardtext |
|---|---|---|
|  | Displayname | % s |
|  | Editprofile | Profil bearbeiten |
|  | Notificationsettings | Benachrichtigungseinstellungen |
|  | Siteadmin | Admin-Konsole (Links zu Studio) |
|  | Signout | Abmelden |

## Stream-Info {#section_wx1_c24_xz}

Für Content Stream-Informationen verfügbare Zeichenfolgen und Anzeigen. Listet die Anzahl der Personen auf, die Listening, die Anzahl der Beiträge für die App, die Anmeldung oder den Zugriff auf ihre Kontoinformationen.

| Schlüssel | Standardtext | Stream-Daten |
|---|---|---|
|  | Commentcountlabelzero | % s Kommentar |
|  | Commentcountlabel | % s Kommentar |
|  | Commentcountlabelplural | % s Kommentare |
|  | Listenercount | Person Listening |
|  | Listenercountplural | people listening |
|  | Liveblogpostcountlabelzero | post |
|  | Liveblogpostcountlabel | post |
|  | Liveblogpostcountlabelplural | Posts |
| Thread-Optionen | Threadbreakoutbutton | Gesamte Thread anzeigen |
|  | Togglecollapse | Reduzieren umschalten |
| Kommentare mit hoher Geschwindigkeit/in Warteschlange | aktualisieren | Aktualisieren |
|  | Newcomment | Neuer Kommentar |
|  | Newcomments | Neue Kommentare |
|  | Newresponse | neue Antwort |
|  | Newanswers | neue Antworten |

## Stream-Sortierung {#section_ih2_124_xz}

Ermöglicht es, zurückgegebene Inhalte nach Alter oder Beliebtheit zu sortieren.

![](assets/strings_newestoldesttop-1-150x56.png)

| Schlüssel | Standardtext | Kopfzeilenoptionen |
|---|---|---|
|  | Sortnewest | Neueste |
|  | Sortoldest | Älteste |
|  | Sorttopcomments | Top-Kommentare |
|  | Sorthotthreads | Hot Threads |
|  | Sortseparator |  |  |
|  | Streamsorting | Wird geladen |
|  | Topcommentscontentnotfoundmsg | Es gibt noch nicht genügend &quot;Gefällt mir&quot; -Klicks. |
|  | Hotthreadscontentnotfoundmsg | Es sind noch nicht genügend Threads vorhanden. |
|  | Streamrefreshmsg | Sehen Sie sich die neuen Funktionen an. |
| Fußzeilenoptionen | Archiveheadertitle | Aus dem Archiv |
|  | Archiveshowmore | Mehr anzeigen |
|  | Showmore | Weitere Kommentare anzeigen |
|  | Showmoreliveblog | Mehr Beiträge anzeigen |

![](assets/strings_threadend-150x47.png)

## Inhaltsinformationen {#section_llv_yd4_xz}

Listet Beitragsinformationen auf: Benutzername, alle angewendeten Benutzer-Tags und die Zeit des Beitrags.

![](assets/strings_authorinfo-150x52.png)  ![](assets/strings_posttime-150x45.png)

| Schlüssel | Standardtext | Autor |
|---|---|---|
|  | Moderator | Moderator |
|  | Hovercardviewprofile | Vollständigen Profil anzeigen |
| Post-Info | Timejustnow | just now |
|  | Timeminutesago | Minute |
|  | Timeminutesagoplural | Vor Minuten |
|  | Timehoursago | Stunde |
|  | Timehoursagoplural | Vor Stunden |
|  | Timedaysago | ago |
|  | Timedaysagoplural | Tage vor Tagen |
|  | Likesplural | &quot; Gefällt mir&quot; -Klicks |
|  | Likessingular | Gefällt mir |
|  | Moderatoredittimestamp | Von einem Moderator bearbeitet |
|  | Commenttombstones | Dieser Kommentar wurde gelöscht. |
|  | Permalinknotfoundmsg | Dieser Kommentar ist nicht mehr sichtbar. |
|  | Quickprofiletooltip | Schnellprofil |

## Dargebotenen Inhalt {#section_gmw_vd4_xz}

Sofern aktiviert, wird der spezielle Inhalt oben im Stream aufgeführt.

|  | Schlüssel | Standardtext |
|---|---|---|
| Beschriftte Bezeichnungen |  |  |
| ![](assets/strings_featuredcontent-150x40.png) | Featuredcommentstag | Empfohlen |
|  | Featuredcommentstitleplural | Hervorgehobene Kommentare |

## Texteditor {#section_ky5_td4_xz}

Standardmäßig oben auf der Seite für alle Benutzer verfügbar.

![](assets/strings_texteditor-1-150x77.png)

|  | Schlüssel | Standardtext |
|---|---|---| 
| Editor-Schaltflächen | folgen | + Befolgen |
|  | nicht folgen | - Nicht befolgen |
|  | Liveblogfollow | Live-Blog |
|  | Liveblogunfollow | Aufheben des Live-Blogs |
|  | Postbutton (für angemeldete Benutzer verfügbar) | Kommentar posten |
|  | Postasbutton (für nicht authentifizierte Benutzer verfügbar.) | Kommentar als… |
|  | Posteditbutton | Kommentar bearbeiten |
|  | Posteditasbutton | Kommentar bearbeiten als… |
|  | Posteditcancelbutton | Abbrechen |
|  | Editordisabled | Diese Unterhaltung ist derzeit für neue Kommentare geschlossen. |
| Chat-Optionen | Livechatpostbuttonlabel | Beitrag |
|  | Livechatposteditbutton | Bearbeiten |
|  | Livechatwindowsinstruction | Drücken Sie Strg + Eingabetaste, um zu posten. |
|  | Livechatotherinstructions | Drücken Sie Befehl + Eingabetaste, um zu posten. |

## Antwortoptionen {#section_zvt_qd4_xz}

Sofern nicht anderweitig vermerkt, steht für alle angemeldeten Benutzer zur Verfügung. Bewegen Sie den Mauszeiger über ein Inhaltsbedienfeld, um Zugriff zu haben.

![](assets/strings_banusermodal-150x36.png)

| Schlüssel | Standardtext |  |
|---|---|---|
| Benutzerantwortoptionen | Für Endbenutzer verfügbar. |  |
| Flagbutton | Flag |
|  | Flagcommenttooltip | Flag |
|  | Editbutton (nur für Autoren und Moderatoren verfügbar, falls aktiviert) | Bearbeiten |
|  | Deletebutton (nur für Autoren und Moderatoren verfügbar, falls aktiviert) | Löschen |
|  | Deletecommenttooltip | Löschen |
|  | Sharebutton | Freigeben |
|  | Sharecommenttooltip | Freigeben |
|  | Likebutton | Gefällt mir |
|  | Unlikebutton | Anders |
|  | Replybutton | Antworten |
|  | Replybuttonsingular (Verfügbar für Chat und Live Blog) | Antworten |
|  | Replybuttonplural (Verfügbar für Chat und Live Blog) | Antworten |

![](assets/strings_responseoptions-150x35.png)

| Schlüssel | Standardtext |  |
|---|---|---|
| Flag Modal | Flagtitle | Kommentar % s&#39;s |
|  | Flagsubtitle | Flag als |
|  | Flagdefaultselectoption | Auswählen |
|  | Flagspam | Spam |
|  | Flagspambutton | Spam |
|  | Flagspamcommenttooltip | Spam |
|  | Flagpress | Offensive |
|  | Flagdistsivebutton | Offensive |
|  | Flagdistsivecommenttooltip | Offensive |
|  | Flagdisagree | Nicht zustimmen |
|  | Flagdisagreebutton | Nicht zustimmen |
|  | Flagdisagreecommenttooltip | Nicht zustimmen |
|  | Flagofftopic | Aus Thema |
|  | Flagofftopicbutton | Aus Thema |
|  | Flagofftopiccommenttooltip | Aus Thema |
|  | Flagemail | E-Mail |
|  | Flagemailplaceholder | you@example.com |
|  | Flagnotes | Hinweise |
|  | Flagnotesplaceholder | Eingabe hier beginnen… |
|  | Flagconfirmbutton | OK |
|  | Flagcancelbutton | Abbrechen |
|  | Flagconfirmationmessage | Kommentar % s als % s markieren? |
|  | Flagsuccessmsg | Kommentar wurde markiert. |

![](assets/strings_flagmodal-150x87.png)

| Schlüssel | Standardtext |  |
|---|---|---|
| Modal freigeben | Sharetitle | Kommentar freigeben |
|  | Shareplaceholdertext | Was glauben Sie? |
|  | Sharelabel | Teilen auf: |
|  | Sharetexttwitter | blank |
|  | Sharetextfacebook | blank |
|  | Sharetextlinkedin | blank |
|  | Sharebuttontext | Freigeben |
|  | Sharepermalink | Permalink |
|  | Loadingpermalink | Kurze URL wird geladen… |
|  | Sharetext | Ich habe gerade einen Kommentar gepostet. Überprüfen Sie es! |

![](assets/strings_sharemodal-150x59.png)

| Schlüssel | Standardtext |  |
|---|---|---|
| Antwort-Modal | Postreplyasbutton | Kommentar als… |
|  | Postreplybutton (für angemeldete Benutzer verfügbar) | Kommentar posten |
|  | Backtohotthreads | Zurück zu Hot Threads |

![](assets/strings_backto-150x48.png)

| Schlüssel | Standardtext |  |
|---|---|---|
| Twitter @ mention modal | Mentiontitle | Erwähnung freigeben |
|  | Mentionsubtitletwitter | Tweet freigeben für: |
|  | Mentiondefaulttext | Ich habe Sie in einem Livefyre-Kommentar erwähnt! |
|  | Mentionconfirmbutton | OK |
|  | Mentioncancelbutton | Abbrechen |
|  | Mentionerrorgeneral | Oops! Etwas ist falsch! Livefyre wurde benachrichtigt. |
|  | Mentionerrornoneselected | Sie müssen mindestens eine Erwähnung aktivieren. |
|  | Mentionmenutitle | So können Sie Ihre Freunde anzeigen und erwähnen |
|  | Mentiontwitterconnect | Verbindung zu Twitter herstellen |
|  | Mentiontwitterfetching | Freunde werden abgerufen… |
|  | Mentionsuccessmsg | Erwähnungen wurden erfolgreich gesendet. |

![](assets/strings_sharemention-150x60.png)

| Schlüssel | Standardtext |  |
|---|---|---|
| Modal bearbeiten | Für Studio-Administratoren, Benutzermanager oder Moderatoren verfügbar |  |
| @ (@ mention.) | &lt;/&gt; (Öffnet das benutzerdefinierte HTML-Fenster.) |  |
|  | Customhtmldialogtitle (Wird als Header für das Modal angezeigt.) | Benutzerdefinierte HTML hinzufügen |

![](assets/strings_moderatoreditmodal-150x49.png)

| Schlüssel | Standardtext |  |
|---|---|---|
| Moderatorantwortoptionen | Für Studio-Administratoren, Benutzermanager oder Moderatoren verfügbar. |  |
| Pendingcomment | ausstehend |
|  | Banuserbutton | Benutzer sperren |
|  | Banusertooltip | Benutzer sperren |
|  | Bozobutton | Bozo |
|  | Bozocommenttooltip | Bozo |
|  | Featurebutton | Funktion |
|  | Featurecommenttooltip | Funktion |
|  | Unfeaturebutton | Unfeature |
|  | Featuredcommenttooltip | Unfeature |

![](assets/strings_adminoptions-150x33.png)

| Schlüssel | Standardtext |  |
|---|---|---|
| Benutzer-Modal verbieten | Für Studio-Administratoren, Benutzermanager oder Moderatoren verfügbar. |  |
| Bantitle | Benutzer sperren |  |
|  | Banconfirmation | Sind Sie sicher, dass Sie diesen Benutzer verbieten möchten? |
|  | Banconfirmbutton | OK |
|  | Bancancelbutton | Abbrechen |

## Kommentar-Benachrichtigung {#section_qqt_pd4_xz}

Falls aktiviert, steht unten auf der Seite für alle Livefyre-Unterhaltungen-Apps zur Verfügung.

![](assets/strings_notifier-150x112.png)

|  | Schlüssel | Standardtext |
|---|---|---|
| Benachrichtigungsbeschriftungen | Commentnotifier | Neuer Kommentar |
|  | Commentnotifierplural | Neue Kommentare |
|  | Liveblognotifier | Neuer Beitrag |
|  | Liveblognotifierplural | Neue Beiträge |

## Fehlermeldungen {#section_omz_jxn_xz}

Für anpassbare Fehlermeldungen verfügbare Zeichenfolgen.

| Schlüssel | Standardtext |
|---|---|
| Errorautherror | Sie sind nicht berechtigt, einen Kommentar zu dieser Unterhaltung zu posten. |
| Errorcommentsnotallowed | Kommentare sind für diese Unterhaltung nicht zulässig |
| Errordefault | Es ist ein Fehler aufgetreten. Bitte erneut versuchen. |
| Errorduplicate | Solange Sie Ihren Kommentar gefallen haben, können Sie ihn nicht zweimal posten. |
| Erroreditduplicate | Sie müssen den Text des Kommentars ändern, wenn Sie es bearbeiten. |
| Erroreditnotallowed | Sie dürfen Kommentare zu dieser Unterhaltung nicht bearbeiten. |
| Erroredittimeexceeded | Ihr Kommentar-Bearbeitungszeitraum ist abgelaufen. |
| Errorempty | Anscheinend versuchen Sie, einen leeren Kommentar zu posten. |
| Errorexpired | Ihre Sitzung ist abgelaufen. Laden Sie die Seite erneut ein. |
| Errorflagnotselected | Wählen Sie einen Markentyp aus. |
| Errorguestliked | Leider können nur solche mit Konten Inhalte haben. |
| Errorinsufficientpermissions | Unzureichende Berechtigungen |
| Errorinvalidchar | Anscheinend versuchen Sie, ein ungültiges Zeichen zu posten. |
| Errorlikeowncomment | Sie können Ihren eigenen Kommentar nicht verwenden. |
| Errormalformed | Anscheinend versuchen Sie, fehlerhafte Inhalte zu posten. |
| Errormaxchars | Der Kommentar ist zu lang. Bitte bearbeiten und versuchen Sie es erneut. |
| Errormedianotavailable | Medien sind nicht mehr sichtbar. |
| Errorshowmore | Beim Laden weiterer Kommentare ist ein Fehler aufgetreten. |
| Multiplemedianotallowederror | Ihre Berechtigungen gewähren Ihnen nur jeweils eine Medienanlage. |

## Uhrzeit- und Datumsformat {#section_yz4_g5n_xz}

Übersetzen und anpassen der Darstellung von Datumsbereichen in Inhaltskarten in Visualisierungs-Apps.

| Schlüssel | Standardtext |
|---|---|
| Hoursago | {number} h |
| Hoursagosingular | {number} h |
| Justnow | 1s |
| Minutesago | {number} m |
| Minutesagosingular | {number} m |
| Monthdayformat | {day} {monthabbrev} |
| Monthdayyearformat | {day} {monthabbrev} {year} |
| Monthnames | Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember |
| Monthnamesabbrev | Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oq, Nov, Dec |
| Secondsago | {number} s |
| Secondsagosingular | {number} s |

## Medienpinnwand {#section_vwt_d5n_xz}

Für die Medienwall-App verfügbare Zeichenfolgen.

| Schlüssel | Standardtext |
|---|---|
| Featuredtext | Empfohlen |
| Sharebuttontext | Freigeben |

| Schlüssel | Standardtext |
|---|---|
| Postbuttontext | Was ist Ihre Meinung? |
| Postmodaltitle | Kommentar posten |
| Postmodalbutton | Kommentar posten |
| Postmodalplaceholder | Was möchten Sie sagen? |
| Showmorebuttontext | Mehr laden |
| Sharebuttontext | Freigeben |

## Map {#section_fxv_c5n_xz}

Für Maps verfügbare Zeichenfolgen.

| Schlüssel | Standardtext |
|---|---|
| Featuredtext | Empfohlen |
| Sharebuttontext | Freigeben |

## Mosaik {#section_e2s_b5n_xz}

Für Mosaiken verfügbare Zeichenfolgen.

| Schlüssel | Standardtext |
|---|---|
| Featuredtext | Empfohlen |
| Sharebuttontext | Freigeben |

## Karussell {#section_l2z_hkn_xz}

Für Karussell verfügbare Zeichenfolgen.

| Schlüssel | Standardtext |
|---|---|
| Featuredtext | Empfohlen |
| Sharebuttontext | Freigeben |

## Feature Card {#section_mw2_hkn_xz}

Für die Feature Card verfügbare Zeichenfolgen.

| Schlüssel | Standardtext |
|---|---|
| Featuredtext | Empfohlen |
| Sharebuttontext | Freigeben |

## App hochladen {#section_grc_gkn_xz}

Für die Upload-App verfügbare Zeichenfolgen.

| Schlüssel | Standardtext |
|---|---|
| Postbuttontext | Was ist Ihre Meinung? |
| Postmodaltitle | Kommentar posten |
| Postmodalbutton | Kommentar posten |
| Postmodaltitleplaceholder | Titel eingeben |
| Postmodalplaceholder | Was möchten Sie sagen? |
| Postmodalconfirationtitle | Vielen Dank für die Veröffentlichung! |
| Postmodalconfirmationmessage | Ihr Beitrag wird geprüft. |
| Postmodalconfirmationbutton | Fertig |
| Titel |  |
| message |  |
| Editorerrorattachmentsrequired | Eine Anlage erforderlich |
| Editorerrorbody | Bitte eine Nachricht hinzufügen |
| Editorerrorduplicate | Genauso wie Sie Ihren Hinweis erhalten, können Sie ihn nicht zweimal posten. |
| Editorerrorgenerisch | Es ist ein Fehler aufgetreten. |
| Editorerrortitlerequired | Ein Titel ist erforderlich. |

## Umfrage {#section_pdg_fwh_xz}

Für Umfragen verfügbare Zeichenfolgen.

| Schlüssel | Standardtext |
|---|---|
| Totalvoteslabel | % s Stimmen insgesamt |
| Sharestringtext | Ich habe gerade über % s abgestimmt. |
| Pollclosedlabel | Diese Umfrage ist zur Zeit geschlossen. |

## Livefyre-Identität {#section_zc3_xvh_xz}

Für die Livefyre-Identität verfügbare Zeichenfolgen.

| Schlüssel | Standardtext |
|--- |--- |
| Automaticallyfollowtalk | Konversationen, die ich verbinde, automatisch befolgen |
| back | Zurück |
| biografisch | Biografie |
| create | Erstellen |
| Createanewaccount | Neues Konto erstellen |
| Createnewaccountwithemail | Erstellen eines neuen Kontos mit E-Mail |
| Changeavatar | Avatar ändern |
| Select sefile | Datei auswählen |
| Completeaccount | Vollständiges Konto |
| Emailwhensomeonereplies | E-Mail, wenn jemand auf mich antwortet |
| Emailcommentsifollow | E-Mail-Kommentare in Unterhaltungen |
| Emailsenttoresetpassword | E-Mail gesendet! Überprüfen Sie Ihren Posteingang auf einen Link, um Ihr Passwort zurückzusetzen. |
| Emailverificationsent | E-Mail-Überprüfung gesendet |
| Firstname | Vorname |
| Forgotpassword | Kennwort vergessen? |
| Forgotyourpassword | Vergessen Sie Ihr Passwort? |
| Forgotyourpasswordinstructions | Geben Sie unten Ihren Benutzernamen oder die E-Mail-Adresse ein und senden Sie einen Link, um Ihr Kennwort zu ändern. |
| Forminputclosebuttontext | Schließen |
| Forminputcancelbuttontext | Abbrechen |
| Forminputsavebuttontext | Speichern |
| Hasnotleftanycomments | keine Kommentare hinterlassen |
| Locationisfrom | stammt aus |
| Labelavatar | Avatar |
| Labelcomments | Kommentare |
| Labelconfirmnewpassword | Neues Passwort bestätigen |
| Labelconfirmpassword | Kennwort bestätigen |
| Labelemail | E-Mail-Adresse |
| Labellikes | &quot; Gefällt mir&quot; -Klicks |
| Labelloading | Wird geladen |
| Labelnewpassword | Neues Kennwort |
| Labelnotification | Benachrichtigungen |
| Labelpassword | Kennwort |
| Labelprofile | Profil |
| Labelusername | Benutzername |
| Labelusernameoremail | Benutzername oder E-Email |
| Lastname | Nachname |
| Livefyreaccount | Livefyre-Konto |
| Ort | Position |
| Loadingprofile | Profil wird geladen |
| Newpassword | Neues Kennwort |
| Oldpassword | Alte Passwort |
| on | on |
| or | or |
| Passwordlinkexpired | Der Link, auf den Sie klicken, um Ihr Passwort zurückzusetzen, ist abgelaufen. Setzen Sie Ihr Passwort erneut zurück und wir senden Ihnen einen neuen Link. |
| Commenecheckemailtocomplete | Bitte überprüfen Sie Ihre E-Mail, um Ihre Registrierung abzuschließen. |
| gepostet | Gepostet |
| Poweredby | powered by |
| Profilenotificationimmediate | sofort |
| Profilenotificationhourly | stündlich |
| Profilenotificationnever | never |
| Recentcomments | Letzte Kommentare |
| zurücksetzen | Zurücksetzen |
| Resetpassword | Kennwort zurücksetzen |
| Signin | Anmelden |
| Signinwith | Anmelden mit |
| Signinwithemail | Mit E-Mail anmelden |
| Signup | Anmelden |
| Socialaccount | Social-Konto |
| Successpasswordchanged | Erfolg! Ihr Passwort wurde geändert und Sie werden jetzt angemeldet. |
| Termsandconditions | Nutzungsbedingungen |
| Termsandconditionsintro | Wenn Sie sich registrieren, akzeptieren Sie die |
| Termsofuse | Nutzungsbedingungen |
| Termsofuseintro | Indem Sie sich anmelden, stimmen Sie zu |
| Thisuser | Dieser Benutzer |
| Verifypassword | Kennwort überprüfen |
| Filesizelimit | Max. 2 MB |
| accountnotfound | Konto nicht gefunden |
| Avatarimageexceedsize | Ihr Avatar-Bild überschreitet die maximale Dateigröße von 2 MB. |
| fieldisrequired | Feld akzeptiert nur eine Ganzzahl |
| fieldonlyacceptsavalidemail | Feld akzeptiert nur eine gültige E-Mail |
| fieldonlyacceptsletters | Feld akzeptiert nur Buchstaben |
| Filesizemustbelessthanmb | Dateigröße muss kleiner {#}als MB sein |
| invalidusernameorpassword | Ungültiger Benutzername oder ungültiges Kennwort |
| minimumverlängern thofcharacters | Mindestlänge {#} von Zeichen |
| maximumverlängern thofcharacters | Maximale {#} Zeichenlänge |
| therewasanerror | Es ist ein Fehler aufgetreten. |
| thisfieldisrequired | Dieses Feld ist erforderlich. |
| validfileextensions | Gültige Dateierweiterungen |
| valuemustmatch | Wert muss übereinstimmen |
| Passwordlength | zwischen 6 und 32 Zeichen lang sein. |
| Passwordcharacters | einschließlich Kleinbuchstaben und Großbuchstaben. |
| Passwordsymbols | geben Sie mindestens eine Zahl und ein Symbol ein. |
| Passwordusername | Ihren Benutzernamen nicht enthalten. |
| Passwordpoarm PasswordPopoverTitle | Ihr Passwort muss: |
| Passworderrorcontainsfirstname | Das eingegebene Kennwort enthält entweder Ihren Benutzernamen, Ihren Vornamen oder Ihren Nachnamen. Geben Sie aus Sicherheitsgründen ein Kennwort ein, das Ihren Benutzernamen, Ihren Vornamen oder Ihren Nachnamen nicht enthält. Beachten Sie außerdem, dass Ihr Passwort Folgendes enthalten muss: 6 bis 32 Zeichen Großbuchstaben A Kleinbuchstabe Zeichen Ein Symbol |
| Passworderrorcontainslastname | Das eingegebene Kennwort enthält entweder Ihren Benutzernamen, Ihren Vornamen oder Ihren Nachnamen. Geben Sie aus Sicherheitsgründen ein Kennwort ein, das Ihren Benutzernamen, Ihren Vornamen oder Ihren Nachnamen nicht enthält. Beachten Sie außerdem, dass Ihr Passwort Folgendes enthalten muss: 6 bis 32 Zeichen Großbuchstaben A Kleinbuchstabe Zeichen Ein Symbol |
| Passworderrorcontainsusername | Das eingegebene Kennwort enthält entweder Ihren Benutzernamen, Ihren Vornamen oder Ihren Nachnamen. Geben Sie aus Sicherheitsgründen ein Kennwort ein, das Ihren Benutzernamen, Ihren Vornamen oder Ihren Nachnamen nicht enthält. Beachten Sie außerdem, dass Ihr Passwort Folgendes enthalten muss: 6 bis 32 Zeichen Großbuchstaben A Kleinbuchstabe Zeichen Ein Symbol |
| Passworderrortooshort | Mindestzeichen von 6 Zeichen für Passagen |
| Passworderrortoolong | Maximal 32 Zeichen für Kennwort |
| Passworderrormissinguppercase | Kennwort sollte mindestens ein Großbuchstaben enthalten |
| Passworderrormissinglowercase | Kennwort muss mindestens ein Kleinbuchstaben enthalten |
| Passworderrormissingsymbol | Das Kennwort muss mindestens ein Symbol im Satz enthalten. `!@#$%^&*()?.,<>\’;:”[]{}|` |


