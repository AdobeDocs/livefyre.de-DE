---
description: Anpassen der Textzeichenfolgen für Livefyre-Kritiker
seo-description: Anpassen der Textzeichenfolgen für Livefyre-Kritiker
seo-title: Textzeichenfolgen-Zeichenfolgen
solution: Experience Manager
title: Textzeichenfolgen-Zeichenfolgen
uuid: a 3735237-e 55 d -4 bc 0-b 88 d -8 a 323980 ee 09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Textzeichenfolgen-Zeichenfolgen{#sidenotes-text-strings}

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
|  | Datetimemonths | Ein Array. Standard =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
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

