---
description: Zum benutzerdefinierten Stilinhalt für Benutzergruppen müssen Sie zuerst
  ein Benutzertag zum Konto hinzufügen und dann den Inhalt mit CSS formatieren.
seo-description: Zum benutzerdefinierten Stilinhalt für Benutzergruppen müssen Sie
  zuerst ein Benutzertag zum Konto hinzufügen und dann den Inhalt mit CSS formatieren.
seo-title: Anwenden benutzerdefinierter Stile
solution: Experience Manager
title: Anwenden benutzerdefinierter Stile
uuid: 0556 aa 2 f -4 fcd -4 bde-abb 5-479 ec 682 f 573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Anwenden benutzerdefinierter Stile{#applying-custom-styles}

Zum benutzerdefinierten Stilinhalt für Benutzergruppen müssen Sie zuerst ein Benutzertag zum Konto hinzufügen und dann den Inhalt mit CSS formatieren.

Für jedes vom Studio oder Ping für Pull hinzugefügte Benutzertag erstellt Livefyre zwei CSS-Klassen, die beide zum Gestalten des Gruppeninhalts verwendet werden können.

Beim Konvertieren von Benutzertags in CSS-Klassen:

* Livefyre erstellt zwei Klassen: fyre-author-tag-*** < ihre_ Gruppe >*** und fyre-tag-author-*** < ihre_ Gruppe >***. Beide können zum Gestalten des Inhalts verwendet werden.

* Alle im Tag enthaltenen Leerzeichen werden in Unterstriche umgewandelt. Beispiel: Favoritenbenutzer wird favorit_ user.
* Unicode-Zeichen, die in Gruppennamen enthalten sind, werden nicht konvertiert und erscheinen in den Klassennamen als Unicode. Beispiel: Benutzergruppe "modérateur" wird" fyre-comment-author-tag-modérateur" .

Sobald Ihre Benutzergruppen erstellt wurden, verwenden Sie die CSS-Klassen von Livefyre, um benutzerdefinierte Stile für den Inhalt anzuwenden.

## Stilinhalte für Moderatoren (und Inhaber) {#section_vjv_2cv_xz}

* Verwenden Sie den CSS-Klasse. fyre-moderator.

   >[!NOTE]
   >
   >Eigentümer, da sie auch Moderatoren sind, haben diese Klasse auch auf ihren Inhalt im Stream angewendet.

* Erstellen Sie eine CSS-Regel, um ein Zeichen für die Gruppe anzuzeigen oder zu gestalten:

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## Stilinhalt für Benutzergruppen {#section_ghn_s1v_xz}

Erstellen Sie eine CSS-Regel, um ein Zeichen für die Gruppe anzuzeigen oder zu gestalten:

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

Verwenden Sie die CSS-Klasse fyre-author-tag-*** < ihre_ Gruppe >*** oder fyre-tag-author-*** < Ihre_ Gruppe >***, um die Schriftart und den Hintergrund für jedes Element zu gestalten, das mit dem ausgewählten Tag verknüpft ist.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

