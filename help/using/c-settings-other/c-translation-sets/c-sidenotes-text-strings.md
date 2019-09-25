---
description: Anpassen der Textzeichenfolgen für Livefyre Sibezeichnet
seo-description: Anpassen der Textzeichenfolgen für Livefyre Sibezeichnet
seo-title: Seitenzeichenfolgen
solution: Experience Manager
title: Seitenzeichenfolgen
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Seitenzeichenfolgen{#sidenotes-text-strings}

Anpassen der Textzeichenfolgen für Livefyre Sibezeichnet

Auf dieser Seite werden alle Zeichenfolgen aufgelistet, die für die Anpassung in Sidebar-Apps verfügbar sind. Informationen zu den für die Livefyre-Core-Apps verfügbaren Zeichenfolgen finden Sie unter Zeichenfolgen-Anpassungen.

ImplementationAuthStream InfoAuthor/Content InfoBenutzeraktionenPost-FunktionenModerator-SchnittstelleFehler

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
| Auth-Menüzeichenfolgen | menuAuthSignInBtn | Anmelden |
|  | menuAuthSignedInMsg | Sie müssen bei {action} angemeldet sein |
|  | menuUserEditProfile | Profil bearbeiten |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Abmelden |
|  | menuUserBackBtn | Alle |

## Stream-Info {#section_wpy_gl4_xz}

Für Informationen und Anzeigen von Inhaltsströmen verfügbare Zeichenfolgen.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Optionen im Menü "Info" | menuInfoCopyright | © Livefyre, Inc. 2014 |
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
|  | datetimeMonths | Als Array. Standardeinstellung =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | QuestionExplanation | Sie können Kommentare jetzt direkt zu Sätzen, Absätzen, Bildern und Anführungszeichen lesen und schreiben.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Markieren Sie Text</span> und klicken Sie auf das <span class="&rdquo;fycon-write&rdquo;"></span> Symbol oder klicken Sie auf das <span class="&rdquo;fycon-action-view&rdquo;"></span> Symbol am Ende jedes Absatzes. |
|  | QuestionMockText | Was "vertraut" ist, ist nicht richtig bekannt, nur weil es "vertraut" ist. |
|  | QuestionTitle | Was ist ein Sidenote? |

## Benutzeraktionen {#section_qxd_fl4_xz}

Für Benutzeraktionen verfügbare Zeichenfolgen: Markieren, Freigeben und Verknüpfen vorhandener Inhalte.

| Element | Schlüssel | Standardtext |
|---|---|---|
| Optionen des Antwortmenüs | menuRepliesViewTitle | Details |
|  | menuRepliesViewReply | Antwort auf Konversation |
| Menüoptionen freigeben | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Freigabe |
| Optionen im Menü "Flag" | menuFlagOptionDismatch | widersprechen |
|  | menuFlagOptionOffensive | Offensive |
|  | menuFlagOptionOffTopic | Off-Thema |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Kennzeichnung als... |
|  | facebookShareCaption | Simit auf "{title}" |
| Mobile Benutzeroptionen | reglerCommentTally | of |
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
| Menüoptionen löschen | menuConfirmAccept | Ja, {Aktion} |
|  | menuConfirmCancel | Abbrechen |
|  | menuConfirmTitle | Sind Sie sicher? |
| Optionen des ETC-Menüs | menuEtcOptionApprove | Genehmigen |
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
| Bestätigungsmeldungen im Menü "Mehr" | notificationApproved | Genehmigt |
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

