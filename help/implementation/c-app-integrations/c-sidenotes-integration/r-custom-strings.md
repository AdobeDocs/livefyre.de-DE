---
description: 'null '
seo-description: 'null '
seo-title: Benutzerdefinierte Zeichenfolgen
title: Benutzerdefinierte Zeichenfolgen
uuid: 73745273-d 3 fb -4569-8910-d 149 fb 37 a 7 b 4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Benutzerdefinierte Zeichenfolgen{#sidenotes-custom-strings}

Benutzerdefinierte Zeichenfolgen werden über ein Objekt angewendet, das in den DOM-Konstruktor eingefügt wurde, und überschreiben Standardzeichenfolgen, die über die Anwendung verwendet werden. Mit diesen können Sie beliebige Teile der Sprache anpassen, um sie an Ihre Stil- oder Sprachspezifikationen anzupassen. Zeichenfolgen werden automatisch mit Standardeinstellungen zusammengeführt.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Schlüssel | Standard |
|---|---|
| Appname | Zielgruppen |
| Commentmoderatortag | Mod |
| Commentpendingtag | Ausstehend |
| Commentreadmorelink | Mehr lesen |
| Commentreplylink | Siehe {number} Antworten |
| Commentreplylinksing | Siehe Antwort |
| Commentvotecount | Stimmen |
| Commentvotecountsing | abstimmen |
| Editorplaceholder | Was glauben Sie? |
| Editorpostbtn | Posts posten |
| Editorpostbtnmobile | Beitrag |
| Editorposting | Beitrag… |
| Editorreplybtn | Post-Antwort |
| Editorreplytitle | Antwort schreiben |
| Editortitle | Notiz schreiben |
| Emptyimageblocktxt | Was glauben Sie? |
| Emptytextblocktxt | + |
| Errorconnection | Uh-oh. Sie haben keine gute Verbindung. |
| Errorduplicate | Wir haben auch Ihre Notiz, aber Sie können sie nicht zweimal posten. |
| Errorgeneral | Es ist ein Fehler aufgetreten. Bitte erneut versuchen. |
| Errorserver | Bei unserem Server ist etwas falsch. Versuchen Sie es erneut? |
| Facebooksharecaption | Sidenotes für &quot; {title} « |
| Menuauthsignedinmsg | Sie müssen bei {action} angemeldet sein. |
| Menuauthsigninbtn | Anmelden |
| Menubackbtn | Zurück |
| Menuconfirmaccept | Ja, {action} |
| Menuconfirmcancel | Abbrechen |
| Menuconfirmtitle | Sind Sie sicher? |
| Menuetcoptionapprove | Genehmigen |
| Menuetcoptiondelete | Löschen |
| Menuetcoptionedit | Bearbeiten |
| Menuetcoptionflag | Flag |
| Menuetcoptionshare | Freigeben |
| Menuetcpostedat | Gepostet am {date} |
| Menuetctitle | Mehr |
| Menuflagoptiondisagree | Nicht zustimmen |
| Menuflagoptionoffensive | Offensive |
| Menuflagoptionofftopic | Aus Thema |
| Menuflagoptionspam | Spam |
| Menuflagtitle | Markieren als… |
| Menuinfocopyright | © Livefyre, Inc. 2014 |
| Menuinfohelp | Hilfe |
| Menuinfolivefyrelink | Besuchen Sie Livefyre.com |
| Menurepliesviewreply | Besprechungen beantworten |
| Menurepliesviewtitle | Details |
| Menushareoptionfacebook | Facebook |
| Menushareoptionlink | Permalink kopieren |
| Menushareoptionlinkcomplete | Kopiert |
| Menushareoptionlinkfailed | Kopieren fehlgeschlagen |
| Menushareoptiontwitter | Twitter |
| Menusharetitle | Freigeben |
| Notificationapproved | Genehmigt |
| Notificationdeleted | Gelöscht |
| Notificationflag | Gekennzeichnet |
| Permalinkbackbtn | Alle |
| Permalinktitle | Permalink |
| Questionexplain | Sie können Kommentare jetzt direkt in Sätzen, Absätzen, Bildern und Anführungszeichen lesen und schreiben.<br><br>Markieren Sie Text und klicken Sie auf das Symbol &quot;fycon-write&quot; oder klicken Sie am Ende jedes Absatzes auf das Symbol&quot; fycon-action-view&quot; . |
| Questionmocktext | Was genau bekannt ist, wird nicht korrekt bekannt, sondern nur aus dem Grund, aus dem sie &quot;bekannt&quot; ist. |
| Questiontitle | Was ist eine Sidenote? |
| Queuedcommentsplural | {number} Neue Zielgruppen |
| Queuedcommentssingular | 1 Neue Sidenote |
| Queuedrepliesplural | {number} Neue Antworten |
| Queuedrepliessingular | 1 Neue Antwort |
| Replybtn | Antworten |
| Signintopost | Melden Sie sich an, um eine Zielgruppe zu schreiben |
| Slidercommenttally | of |
| Sliderinviteread | Lesen |
| Sliderinvitewrite | Schreiben |
| Sliderwritetext | Was glauben Sie? Zum Schreiben tippen |
| Threadcollapsebtn | Reduzieren |
| Threadexpandbtnplural | {number} Antworten erweitern |
| Threadexpandbtnsingular | 1 Antwort erweitern |
| Threadreplybtn | Besprechungen beantworten |
