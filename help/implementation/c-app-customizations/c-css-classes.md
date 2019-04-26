---
description: Verwenden Sie verfügbare CSS-Klassen, um die Anzeige Ihrer Apps anzupassen.
seo-description: Verwenden Sie verfügbare CSS-Klassen, um die Anzeige Ihrer Apps anzupassen.
seo-title: CSS-Klassen
solution: Experience Manager
title: CSS-Klassen
uuid: 8714 e 7 e 5-3858-458 f-a 464-de 87 fd 2 f 0 ff 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CSS-Klassen{#css-classes}

Verwenden Sie verfügbare CSS-Klassen, um die Anzeige Ihrer Apps anzupassen.

Verfügbar für Chat, Kommentare, Live-Blog, Reviews und Autoren.

Verwenden Sie CSS, um Ihre Livefyre-Apps für eine umfassendere Integration auf Ihre Seite anzupassen, indem Sie einfach die Standard-CSS mit Ihrem eigenen Stylesheet überschreiben. In diesem Abschnitt werden die verfügbaren CSS-Anpassungen beschrieben.

* [Editor-CSS](#c_css_classes/section_edx_prh_xz)
* [CSS für Sortieroptionen](#c_css_classes/section_btq_4rh_xz)
* [Kommentar-CSS](#c_css_classes/section_mlv_nrh_xz)
* [CSS für hervorgehobene Kommentare](#c_css_classes/section_m2v_mrh_xz)
* [Archivierte Kommentare (CSS)](#c_css_classes/section_bs5_lrh_xz)
* [Kommentar-Benachrichtigungs-CSS](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS Classes](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Editor-CSS {#section_edx_prh_xz}

Verwenden Sie diese Klassen, um die Benutzeroberfläche des Beitragseditors zu ändern.

| Klasse | Beschreibung |
|---|---|
| . fyre-comment-count | Der Text, der die Anzahl der Kommentare anzeigt. |
| . fyre-login-bar | Der Begrenzungsrahmen, der die Anmeldeleiste und die Optionen enthält. |
| . fyre-live-container | Der Begrenzungsrahmen um die Anzahl der Listening-Listening und deren Avatare. |
| . fyre@-@ editor | Der Begrenzungsrahmen um die. fyre-login-bar. fyre-live-container und den Textbereich, in dem die Benutzer ihre Kommentare schreiben. |
| . fyre-stream-sort | Der Begrenzungsrahmen um die Sortieroptionen. |

Sie können auch Stile in der App-Konfiguration selbst bearbeiten, einschließlich der Hintergrundfarbe des Editors und der Schriftfarbe, -größe und -familie im Editor.

Fügen Sie die editorcss hinzu, um den Kommentareditor anzupassen: {}-Objekt zu fyre. conv. load () und fügen Sie den gewünschten Stil ein. So aktualisieren Sie beispielsweise den Editor mit Ihrem benutzerdefinierten CSS:

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

## CSS für Sortieroptionen {#section_btq_4rh_xz}

| Klasse | Beschreibung |
|---|---|
| . fyre-stream-sort | Die gesamte Sortieroption div. |
| . fyre-stream-sort-neueste | Die Option "Neuestes" . |
| . fyrestream stream-sort-älteste | Die Option "Älteste" . |
| . fyre-stream-sort-bar | Die Trennzeichenleiste zwischen den Optionen. |
| . fyre-stream-sort-selected | Die derzeit ausgewählte Sortieroption. |

HTML-Struktur:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Blenden Sie die|" Trennen der Sortierungsoptionen.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Kommentar-CSS {#section_mlv_nrh_xz}

| Klasse | Beschreibung |
|---|---|
| . fyre-comment-author-tag- *`custom tag name`* | Livefyre erstellt in diesem Format für jedes über Livefyre Studio, [Profil-Synchronisierung hinzugefügte Benutzertag eine CSS-Klasse](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Diese Klasse kann verwendet werden, um den Hintergrund für alle Inhalte zu gestalten, die von Benutzerkonten gepostet werden, einschließlich dieses Tags. |
| . fyre-tag-content-icon- *`tag name`* | Livefyre erstellt in diesem Format für jedes über Livefyre [Studio hinzugefügte Content-Tag eine CSS-Klasse](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Diese Klasse kann verwendet werden, um alle Inhalte zu formatieren, denen Sie das Tag hinzugefügt haben. |
| . fyre-comment-user | Der Begrenzungsrahmen, der das Benutzerprofilbild enthält. |
| . fyre-comment-username | Der Benutzername. |
| . fyre@-@ moderator | Der Begrenzungsrahmen des Moderators. |
| . fyre-comment | Begrenzungsrahmen um den Kommentartext/Link herum. |
| . fyre-comment-article | Der Begrenzungsrahmen für den gesamten Kommentar-Inhalt. |
| . fyre-comment-date | Das Tag, das mit dem Element "Zeit seit Veröffentlichung" verknüpft ist. |
| . fyre-comment-media | Der Begrenzungsrahmen um den Medieninhalt. |
| . fyre-comment-actions | Der Begrenzungsrahmen um die verfügbaren Aktionen, um einen Kommentar zu übernehmen. |
| . fyre-comment-like | Der Begrenzungsrahmen um den "Gefällt mir" -Hyperlink. |
| . fyre-comment-reply | Der Begrenzungsrahmen um den Link "Antwort" . |

## CSS für hervorgehobene Kommentare {#section_m2v_mrh_xz}

>[!NOTE]
>
>Alle CSS-Kommentarklassen können auch auf speziellen Inhalt angewendet werden.

| Klasse | Beschreibung |
|---|---|
| . fyre-featworth-content-wrapper | Der Container-div für den Leser. |
| . fyre-featworth-header | Die führende Titelleiste. |
| . fyre-featworth-header-icon | Das Quellsymbol des Headers. |
| . fyre-featlo@-@ title | Der Kopfzeilentext. |
| . fyre-featlo@-@ body | Der Container-div für speziellen Inhalt im Leser. |
| . fyre-featsonder@-@ bid | Das Anführungszeichen, das jedes Inhaltselement beginnt. |

## Archivierte Kommentare (CSS) {#section_bs5_lrh_xz}

>[!NOTE]
>
>Alle CSS-Klassen des Inhalts können auch auf archivierte Inhalte angewendet werden.

| Klasse | Beschreibung |
|---|---|
| . fyre-archive-stream-title | Der Text "Aus dem Archiv" . |
| . fyre@-@ archive-stream-title-icon | Das Logo für den Header "Archivieren" . |

## Kommentar-Benachrichtigungs-CSS {#section_dy4_krh_xz}

Mit diesen Klassen können Sie den Livefyre-Kommentar-Notifier anpassen.

| Klasse | Beschreibung |
|---|---|
| . fyre-notification | div für das Listenelement (sowohl neu als auch archivieren). |
| . fyre-notifier | Der Wrapper für den Inhalt des Notifier. |
| . fyre-notifier-archive | Der Wrapper für alle neuen Inhalte als der letzte Beitrag. |
| . fyre-notifier-avatar | Das Bild für den Avatar. |
| . fyre-notifier-avatar-container | Der Container-div für den Benutzeravatar. Hiermit können Sie Positionierung definieren. |
| . fyre-notifier-avatar-shading | Die Schattierung für Avatar div. |
| . fyre-notifier-banner | Der Container für die Inhaltsvorschau des angemeldeten Inhalts, der den Benutzeravatar und einen Inhaltsausschnitt für das zuletzt gepostete Element anzeigt. |
| . fyre-notifier-base | Der Container für den Informationsteil des Notifier, der die Anzahl der neuen Kommentare, der Benachrichtigungsbeschriftung und der Schließen-Schaltfläche auflistet. |
| . fyre-notifier-base-close | Der Container-div für die Schließen-Schaltfläche (x) für den Notifier. |
| . fyre-notifier-base-shadow | Die Schattierung für die Basis-Basis. |
| . fyre-notifier-caption | Der für den Benachrichtigungsgrad angezeigte Text. Standardmäßig neue Kommentare (s). |
| . fyre-notifier-close | Eine Schaltfläche, die den Benachrichtigungsvorgang schließt. |
| . fyre-notifier-container | Der Container für den Notifier, enthält sowohl das Banner als auch die Basis. |
| . fyre-notifier-counter | Der Behälter für die im Benachrichtigungsfeld aufgeführte Zahl. |
| . fyre-notifier-list | Der Container für die neueste Inhaltskomponente. |
| . fyre-notifier-message | Die ersten ~ 30 Zeichen des angezeigten Inhalts. |
| . fyre-notifier-message-container | Der Container-div für die Kopfzeilenmeldung. |
