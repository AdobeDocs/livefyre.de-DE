---
description: Um Inhalte mit benutzerdefinierten Stilen für Benutzergruppen zu erstellen, müssen Sie dem Konto zunächst ein Benutzer-Tag hinzufügen und dann den Inhalt mit CSS formatieren.
seo-description: Um Inhalte mit benutzerdefinierten Stilen für Benutzergruppen zu erstellen, müssen Sie dem Konto zunächst ein Benutzer-Tag hinzufügen und dann den Inhalt mit CSS formatieren.
seo-title: Anwenden benutzerdefinierter Stile
solution: Experience Manager
title: Anwenden benutzerdefinierter Stile
uuid: 0556aa2f-4fcd-4bde-abb5-479ec682f573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Anwenden benutzerdefinierter Stile{#applying-custom-styles}

Um Inhalte mit benutzerdefinierten Stilen für Benutzergruppen zu erstellen, müssen Sie dem Konto zunächst ein Benutzer-Tag hinzufügen und dann den Inhalt mit CSS formatieren.

Für jeden Benutzer-Tag, der über Studio oder Ping für Pull hinzugefügt wird, erstellt Livefyre zwei CSS-Klassen, die beide zum Formatieren des Gruppeninhalts verwendet werden können.

Beim Konvertieren von Benutzer-Tags in CSS-Klassen:

* Livefyre erstellt zwei Klassen: fyre-author-tag-****** und fyre-tag-author-*****. Beides kann zum Formatieren des Inhalts verwendet werden.

* Alle im Tag enthaltenen Leerzeichen werden in Unterstriche umgewandelt. Beispiel: "Favoritenbenutzer"wird zu "favorite_user".
* In Gruppennamen enthaltene Unicode-Zeichen werden nicht konvertiert und in den Klassennamen als Unicode angezeigt. Beispiel: Die Benutzergruppe "modérateur"wird fyre-comment-author-tag-modérateur.

Nachdem Sie Ihre Benutzergruppen erstellt haben, verwenden Sie die CSS-Klassen von Livefyre, um benutzerdefinierte Stile für den Inhalt anzuwenden.

## Stilinhalte für Moderatoren (und Inhaber) {#section_vjv_2cv_xz}

* Verwenden Sie die CSS-Klasse .fyre-moderator.

   >[!NOTE]
   >
   >Inhaber, da sie auch Moderatoren sind, können diese Klasse auch auf ihren Inhalt im Stream anwenden.

* Erstellen Sie eine CSS-Regel, um eine Markierung für die Gruppe anzuzeigen oder zu formatieren:

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## Stylesheet-Inhalt für Benutzergruppen {#section_ghn_s1v_xz}

Erstellen Sie eine CSS-Regel, um eine Markierung für die Gruppe anzuzeigen oder zu formatieren:

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

Verwenden Sie die CSS-Klasse fyre-author-tag-***** oder fyre-tag-author-****&lt;Ihre_Gruppe&gt;*****, um die Schriftart und den Hintergrund für jedes Element zu gestalten, das von einem Konto veröffentlicht wird, das mit dem ausgewählten Tag verknüpft ist.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

