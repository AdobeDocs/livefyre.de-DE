---
description: Verwenden Sie verfügbare CSS-Klassen, um die Anzeige Ihrer Apps anzupassen.
seo-description: Verwenden Sie verfügbare CSS-Klassen, um die Anzeige Ihrer Apps anzupassen.
seo-title: CSS-Klassen
solution: Experience Manager
title: CSS-Klassen
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 1%

---


# CSS-Klassen{#css-classes}

Verwenden Sie verfügbare CSS-Klassen, um die Anzeige Ihrer Apps anzupassen.

Verfügbar für Chat, Kommentare, Live-Blog, Reviews und Siegels.

Verwenden Sie CSS, um Ihre Livefyre-Apps für eine umfassendere Integration mit Ihrer Seite anzupassen, indem Sie einfach die Standard-App-CSS mit Ihrem eigenen Stylesheet außer Kraft setzen. In diesem Abschnitt werden verfügbare CSS-Anpassungen beschrieben.

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
| .fyre-comment-count | Der Text, der die Anzahl der Kommentare anzeigt. |
| .fyre-login-bar | Der Begrenzungsrahmen, der die Anmeldeleiste und die Optionen enthält. |
| .fyre-live-Container | Der Begrenzungsrahmen um die Anzahl der zuhörenden Personen und ihre Avatare. |
| .fyre-editor | Der Begrenzungsrahmen um die .fyre-login-bar, .fyre-live-Container und den Textbereich, in dem die Benutzer ihre Kommentare schreiben. |
| .fyre-stream-sort | Der Begrenzungsrahmen um die Sortieroptionen. |

Sie können auch die Stile in der App-Konfiguration selbst bearbeiten, einschließlich der Hintergrundfarbe des Editors und der Schriftfarbe, -größe und -familie des Textes, der im Editor angezeigt wird.

Fügen Sie zum Anpassen des Kommentareditors das Objekt editorCss:{} zu fyre.conv.load() hinzu und fügen Sie den gewünschten Stil hinzu. So aktualisieren Sie beispielsweise den Editor mit Ihrer benutzerdefinierten CSS:

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

## Sortieroptionen CSS {#section_btq_4rh_xz}

| Class | Beschreibung |
|---|---|
| .fyre-stream-sort | Die gesamten Sortieroptionen div. |
| .fyre-stream-sort-neueste | Die Option &quot;Neueste&quot;. |
| .fyre-stream-sort-oldest | Die Option &quot;Älteste&quot;. |
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

Blenden Sie das &quot;|&quot;aus, indem Sie die Sortieroptionen trennen.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Kommentar-CSS {#section_mlv_nrh_xz}

| Class | Beschreibung |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre erstellt eine CSS-Klasse in diesem Format für jeden Benutzer-Tag, der über Livefyre Studio hinzugefügt wird: [Profil Sync](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Diese Klasse kann verwendet werden, um den Hintergrund für alle Inhalte zu gestalten, die von Benutzerkonten veröffentlicht werden, einschließlich dieses Tags. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre erstellt eine CSS-Klasse in diesem Format für jedes Content-Tag, das über Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md) hinzugefügt wird. Diese Klasse kann verwendet werden, um alle Inhalte zu gestalten, denen Sie das Tag hinzugefügt haben. |
| .fyre-comment-user | Der Begrenzungsrahmen mit dem Profil des Benutzers. |
| .fyre-comment-username | Der Benutzername. |
| .fyre-Moderator | Der Begrenzungsrahmen des Moderators. |
| .fyre-comment | Begrenzungsrahmen um den Kommentartext/Link. |
| .fyre-comment-article | Der Begrenzungsrahmen für den gesamten Kommentarinhalt. |
| .fyre-comment-date | Das Tag, das an das Element &quot;time since published&quot;angehängt ist. |
| .fyre-comment-media | Der Begrenzungsrahmen um den Medieninhalt. |
| .fyre-comment-actions | Der Begrenzungsrahmen um die verfügbaren Aktionen, die für einen Kommentar ausgeführt werden sollen. |
| .fyre-comment-like | Der Begrenzungsrahmen um den Link &quot;Gefällt mir&quot;. |
| .fyre-comment-response | Der Begrenzungsrahmen um den Link &quot;Antworten&quot;. |

## CSS für hervorgehobene Kommentare {#section_m2v_mrh_xz}

>[!NOTE]
>
>Alle CSS-Klassen für Kommentare können auch auf spezielle Inhalte angewendet werden.

| Class | Beschreibung |
|---|---|
| .fyre-featured-content-wrapper | Der Container div für den Leser. |
| .fyre-featured-header | Die führende Titelleiste. |
| .fyre-featured-header-icon | Das Quill-Symbol der Kopfzeile. |
| .fyre-featured-title | Der Kopfzeilentext. |
| .fyre-special-body | Der Container div für speziellen Inhalt im Reader. |
| .fyre-featured-quote | Das Anführungszeichen, das jedes Inhaltselement beginnt. |

## Archivierte Kommentare CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>Alle CSS-Klassen für Inhalte können auch auf archivierte Inhalte angewendet werden.

| Class | Beschreibung |
|---|---|
| .fyre-archive-stream-title | Der Text &quot;Aus dem Archiv&quot;. |
| .fyre-archive-stream-title-icon | Das Logo für die Kopfzeile &quot;From the Archive&quot;. |

## Kommentar-Benachrichtigungs-CSS {#section_dy4_krh_xz}

Mit diesen Klassen können Sie den Livefyre-Kommentar-Notifier anpassen.

| Class | Beschreibung |
|---|---|
| .fyre-Benachrichtigung | Das div für das Element &quot;Liste&quot;(sowohl neuer als auch archivierter Inhalt). |
| .fyre-notifier | Der Wrapper für den Inhalt des Notifizierers. |
| .fyre-notification-archive | Der Wrapper für alle neuen Inhalte außer dem letzten Beitrag. |
| .fyre-notification-avatar | Das Bild für den Avatar. |
| .fyre-notification-avatar-Container | Der Container div für den Benutzeravatar. Ermöglicht die Definition der Positionierung. |
| .fyre-notification-avatar-shading | Die Schattierung für den Avatar-Div. |
| .fyre-notification-banner | Der Container für den Inhalt der Vorschau des Benachrichtigers, in dem der Benutzeravatar und ein Inhaltsausschnitt für das zuletzt gepostete Element angezeigt werden. |
| .fyre-notification-base | Der Container für den Informationsteil des Notifizierenden, in dem die Anzahl der neuen Kommentare, die Beschriftung des Notifizierenden und die Schaltfläche zum Schließen Liste werden. |
| .fyre-notification-base-close | Der Container div für die Schließen-Schaltfläche (x) für den Notifizierer. |
| .fyre-notification-base-shadow | Die Schattierung für die Benachrichtigungsbasis. |
| .fyre-notification-caption | Der für den Notifizierer angezeigte Text. &quot;Neue Kommentare&quot;standardmäßig. |
| .fyre-notification-close | Eine Schaltfläche, die den Notifizierer schließt. |
| .fyre-notification-Container | Der Container für den Notifizierer enthält sowohl das Banner als auch die Basis. |
| .fyre-notification-Zähler | Der Container für die im Notifizierer angegebene Nummer. |
| .fyre-notification-Liste | Der Container für das neueste Inhaltselement. |
| .fyre-notification-message | Die ersten ca. 30 Zeichen des Inhalts werden angezeigt. |
| .fyre-notification-message-Container | Der Container div für die Kopfzeilenmeldung. |
