---
description: Verwenden Sie verfügbare CSS-Klassen, um die Anzeige Ihrer Apps anzupassen.
seo-description: Verwenden Sie verfügbare CSS-Klassen, um die Anzeige Ihrer Apps anzupassen.
seo-title: CSS-Klassen
solution: Experience Manager
title: CSS-Klassen
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CSS-Klassen{#css-classes}

Verwenden Sie verfügbare CSS-Klassen, um die Anzeige Ihrer Apps anzupassen.

Verfügbar für Chat, Kommentare, Live-Blog, Reviews und Siegels.

Verwenden Sie CSS, um Ihre Livefyre-Apps für eine umfassendere Integration mit Ihrer Seite anzupassen, indem Sie einfach die Standard-App-CSS mit Ihrem eigenen Stylesheet überschreiben. In diesem Abschnitt werden verfügbare CSS-Anpassungen beschrieben.

* [Editor CSS](#c_css_classes/section_edx_prh_xz)
* [CSS der Sortieroptionen](#c_css_classes/section_btq_4rh_xz)
* [Kommentar-CSS](#c_css_classes/section_mlv_nrh_xz)
* [CSS für hervorgehobene Kommentare](#c_css_classes/section_m2v_mrh_xz)
* [Archivierte Kommentar-CSS](#c_css_classes/section_bs5_lrh_xz)
* [Kommentar-Benachrichtigungs-CSS](#c_css_classes/section_dy4_krh_xz)
* [CSS-Klassen formatieren](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editor CSS {#section_edx_prh_xz}

Verwenden Sie diese Klassen, um die Benutzeroberfläche des Post-Editors zu ändern.

| Class | Beschreibung |
|---|---|
| .fyre-comment-count | Der Text mit der Anzahl der Kommentare. |
| .fyre-login-bar | Der Begrenzungsrahmen, der die Anmeldeleiste und die Optionen enthält. |
| .fyre-live-container | Der Begrenzungsrahmen um die Anzahl der zuhörenden Personen und ihre Avatare. |
| .fyre-editor | Der Begrenzungsrahmen um die .fyre-login-bar, den .fyre-live-container und den Textbereich, in dem Benutzer ihre Kommentare schreiben. |
| .fyre-stream-sort | Der Begrenzungsrahmen um die Sortieroptionen. |

Sie können auch die Stile in der App-Konfiguration selbst bearbeiten, einschließlich der Hintergrundfarbe des Editors und der Schriftfarbe, -größe und -familie des Textes, der im Editor angezeigt wird.

To customize the comment editor, add the editorCss:{} object to fyre.conv.load() and include your desired styling. So aktualisieren Sie beispielsweise den Editor mit Ihrer benutzerdefinierten CSS:

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## CSS der Sortieroptionen {#section_btq_4rh_xz}

| Class | Beschreibung |
|---|---|
| .fyre-stream-sort | Die gesamten Sortieroptionen div. |
| .fyre-stream-sort-neueste | Die Option "Neueste". |
| .fyre-stream-sort-oldest | Die Option "Älteste". |
| .fyre-stream-sort-bar | Die Trennleiste zwischen den Optionen. |
| .fyre-stream-sort-selected | Die derzeit ausgewählte Sortieroption. |

HTML-Struktur:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Blenden Sie das "|"aus, indem Sie die Sortieroptionen trennen.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Kommentar-CSS {#section_mlv_nrh_xz}

| Class | Beschreibung |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre erstellt eine CSS-Klasse in diesem Format für jedes Benutzer-Tag, das über Livefyre Studio, [Profilsynchronisierung](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md), hinzugefügt wird. Diese Klasse kann verwendet werden, um den Hintergrund für alle von Benutzerkonten veröffentlichten Inhalte einschließlich dieses Tags zu gestalten. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre erstellt für jedes mit Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md)hinzugefügte Content-Tag eine CSS-Klasse in diesem Format. Diese Klasse kann verwendet werden, um alle Inhalte zu gestalten, denen Sie das Tag hinzugefügt haben. |
| .fyre-comment-user | Der Begrenzungsrahmen, der das Benutzerprofilbild enthält. |
| .fyre-comment-username | Der Benutzername. |
| .fyre-Moderator | Der Begrenzungsrahmen des Moderators. |
| .fyre-comment | Begrenzungsrahmen um den Kommentartext/Link. |
| .fyre-comment-article | Der Begrenzungsrahmen für den gesamten Kommentarinhalt. |
| .fyre-comment-date | Das Tag, das an das Element "time since published"angehängt ist. |
| .fyre-comment-media | Der Begrenzungsrahmen um den Medieninhalt. |
| .fyre-comment-actions | Der Begrenzungsrahmen um die verfügbaren Aktionen, die für einen Kommentar ausgeführt werden sollen. |
| .fyre-comment-like | Der Begrenzungsrahmen um den Link "Gefällt mir". |
| .fyre-comment-response | Der Begrenzungsrahmen um den Link "Antworten". |

## CSS für hervorgehobene Kommentare {#section_m2v_mrh_xz}

>[!NOTE]
>
>Alle CSS-Klassen für Kommentare können auch auf spezielle Inhalte angewendet werden.

| Class | Beschreibung |
|---|---|
| .fyre-special-content-wrapper | Das Container-div für den Reader. |
| .fyre-featured-header | Die führende Titelleiste. |
| .fyre-featured-header-icon | Das Quill-Symbol der Kopfzeile. |
| .fyre-featured-title | Der Kopfzeilentext. |
| .fyre-special-body | Das Container-div für speziellen Inhalt im Reader. |
| .fyre-featured-quote | Das Anführungszeichen, das jedes Inhaltselement beginnt. |

## Archivierte Kommentar-CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>Alle CSS-Klassen für Inhalte können auch auf archivierte Inhalte angewendet werden.

| Class | Beschreibung |
|---|---|
| .fyre-archive-stream-title | Der Text "Aus dem Archiv". |
| .fyre-archive-stream-title-icon | Das Logo für die Kopfzeile "From the Archive". |

## Kommentar-Benachrichtigungs-CSS {#section_dy4_krh_xz}

Mit diesen Klassen können Sie den Livefyre-Kommentar-Notifier anpassen.

| Class | Beschreibung |
|---|---|
| .fyre-Benachrichtigung | Das div für das Listenelement (neue und archivierte Inhalte). |
| .fyre-notifier | Der Wrapper für den Inhalt des Notifizierers. |
| .fyre-notification-archive | Der Wrapper für alle neuen Inhalte außer dem letzten Beitrag. |
| .fyre-notification-avatar | Das Bild für den Avatar. |
| .fyre-notification-avatar-container | Das Container-div für den Benutzer-Avatar. Ermöglicht die Definition der Positionierung. |
| .fyre-notification-avatar-shading | Die Schattierung für den Avatar Div. |
| .fyre-notification-banner | Der Container für den Vorschauinhalt des Benachrichtigers, in dem der Benutzeravatar und ein Inhaltsausschnitt für das zuletzt veröffentlichte Element angezeigt werden. |
| .fyre-notification-base | Der Container für den Informationsteil des Notifizierers, in dem die Anzahl der neuen Kommentare, die Beschriftung des Notifizierers und die Schaltfläche zum Schließen aufgeführt sind. |
| .fyre-notification-base-close | Das Container-div für die Schließen-Schaltfläche (x) für den Notifizierer. |
| .fyre-notification-base-shadow | Die Schattierung für die Benachrichtigungsbasis. |
| .fyre-notification-caption | Der für den Notifizierer angezeigte Text. "Neue Kommentare"standardmäßig. |
| .fyre-notification-close | Eine Schaltfläche, die den Notifizierer schließt. |
| .fyre-notification-container | Der Container für den Notifizierer enthält sowohl das Banner als auch die Basis. |
| .fyre-notification-Zähler | Der Container für die im Notifier angegebene Zahl. |
| .fyre-notification-list | Der Container für das neueste Inhaltselement. |
| .fyre-notification-message | Die ersten ca. 30 Zeichen des Inhalts werden angezeigt. |
| .fyre-notification-message-container | Das Container-div für die Header-Meldung. |
