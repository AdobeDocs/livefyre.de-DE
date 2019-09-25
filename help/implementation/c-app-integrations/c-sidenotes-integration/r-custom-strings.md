---
description: 'null '
seo-description: 'null '
seo-title: Benutzerdefinierte Zeichenfolgen für Sidebar
title: Benutzerdefinierte Zeichenfolgen für Sidebar
uuid: 73745273-d3fb-4569-8910-d149fb37a7b4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Benutzerdefinierte Zeichenfolgen für Sidebar{#sidenotes-custom-strings}

Benutzerdefinierte Zeichenfolgen werden über ein Objekt angewendet, das in den Siunterschiedlichsten Konstruktor eingefügt wird, und überschreiben Standardzeichenfolgen, die über die Anwendung verwendet werden. Diese können verwendet werden, um einen beliebigen Teil der Sprache an Ihre Stil- oder Sprachspezifikationen anzupassen. Strings werden automatisch mit den Standardeinstellungen zusammengeführt.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Schlüssel | Standardeinstellung |
|---|---|
| appName | Sir |
| commentModeratorTag | Mod |
| commentPendingTag | In Bearbeitung |
| commentReadMoreLink | Weitere Info |
| commentReplyLink | Siehe {number} Antworten |
| commentReplyLinkSing | Siehe Antwort |
| commentVoteCount | stimmen |
| commentVoteCountSing | Stimme |
| editorPlaceholder | Was denkst du? |
| editorPostBtn | Post Sidennote |
| editorPostBtnMobile | Posten |
| editorPosting | Beitrag… |
| editorReplyBtn | Antworten |
| editorReplyTitle | Antwort schreiben |
| editorTitle | Notiz schreiben |
| emptyImageBlockTxt | Was denkst du? |
| emptyTextBlockTxt | + |
| errorConnection | Oh-oh. Du scheinst keine gute Verbindung zu haben. |
| errorDuplicate | Ihre Notiz gefällt uns ebenfalls, aber Sie können sie nicht zweimal posten. |
| errorGeneral | Es ist ein Fehler aufgetreten. Bitte versuchen Sie es erneut. |
| errorServer | Etwas ist mit unserem Server schiefgelaufen. Versuch das noch einmal? |
| facebookShareCaption | SideNotes zu "{title}" |
| menuAuthSignedInMsg | Sie müssen bei {action} angemeldet sein |
| menuAuthSignInBtn | Anmelden |
| menuBackBtn | Zurück |
| menuConfirmAccept | Ja, {Aktion} |
| menuConfirmCancel | Abbrechen |
| menuConfirmTitle | Sind Sie sicher? |
| menuEtcOptionApprove | Genehmigen |
| menuEtcOptionDelete | Löschen |
| menuEtcOptionEdit | Vorlage      |
| menuEtcOptionFlag | Markierung |
| menuEtcOptionShare | Freigabe |
| menuEtcPostedAt | Gepostet am {Datum} |
| menuEtcTitle | Mehr |
| menuFlagOptionDismatch | widersprechen |
| menuFlagOptionOffensive | Offensive |
| menuFlagOptionOffTopic | Off-Thema |
| menuFlagOptionSpam | Spam |
| menuFlagTitle | Kennzeichnung als... |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | Hilfe |
| menuInfoLivefyreLink | Besuch Livefyre.com |
| menuRepliesViewReply | Antwort auf Konversation |
| menuRepliesViewTitle | Details |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Permalink kopieren |
| menuShareOptionLinkComplete | Kopiert |
| menuShareOptionLinkFailed | Kopieren fehlgeschlagen |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | Freigabe |
| notificationApproved | Genehmigt |
| notificationDeleted | Gelöscht |
| notificationGekennzeichnet | Gekennzeichnet |
| permalinkBackBtn | Alle |
| permalinkTitle | Permalink |
| QuestionExplanation | Sie können Kommentare jetzt direkt zu Sätzen, Absätzen, Bildern und Anführungszeichen lesen und schreiben.<br><br>Markieren Sie Text und klicken Sie auf das Symbol "fycon-write"oder klicken Sie am Ende jedes Absatzes auf das Symbol "fycon-action-view". |
| QuestionMockText | Was "vertraut" ist, ist nicht richtig bekannt, nur weil es "vertraut" ist. |
| QuestionTitle | Was ist ein Sidenote? |
| queuedCommentsPlural | {number} Neues Attribut |
| queuedCommentsSingular | 1 Neuer Sidente |
| queuedRepliesPlural | {number} Neue Antworten |
| queuedRepliesSingular | 1 Neue Antwort |
| responseBtn | Antwort |
| signInToPost | Melden Sie sich an, um eine Präsidentschaft zu schreiben |
| reglerCommentTally | of |
| reglerInviteRead | Gelesen |
| reglerInviteWrite | schreiben |
| reglerWriteText | Was denkst du? Zum Schreiben tippen |
| threadCollapseBtn | Ausblenden |
| threadExpandBtnPlural | {number} Antworten erweitern |
| threadExpandBtnSingular | 1 Antwort erweitern |
| threadReplyBtn | Antwort auf Konversation |
