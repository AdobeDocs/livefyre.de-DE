---
description: Erlauben Sie Benutzern, das Bild anzupassen, das mit ihrem Inhalt angezeigt wird.
seo-description: Erlauben Sie Benutzern, das Bild anzupassen, das mit ihrem Inhalt angezeigt wird.
seo-title: Avatare
title: Avatare
uuid: bf20f3bc-3dcc-4e16-a629-3380d1a7a3f2
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053

---


# Avatare{#avatars}

Erlauben Sie Benutzern, das Bild anzupassen, das mit ihrem Inhalt angezeigt wird.

Benutzeravatare werden (standardmäßig) neben Inhalten in allen Apps angezeigt und aus dem Identitätsprofil-System gezogen, das in Ihrer Implementierung verwendet wird. Diese Avatare variieren je nach App, in der sie angezeigt werden.

(Mit Livefyre können Sie Avatare deaktivieren, wenn Sie sie nicht in Ihren Apps anzeigen möchten.)

>[!NOTE]
>
>Avatare werden für Chat mit 25p x 25p und für die meisten anderen Apps mit 50p x 50p angezeigt.

## Avatar-Speicher {#section_zbh_x1f_wy}

Avatare werden asynchron in Livefyre geladen. Wenn sich ein Benutzer zum ersten Mal bei der App anmeldet oder die zugehörige Avatar-Bilddatei ändert, wird sein Profilbild einer Aufgabenwarteschlange hinzugefügt. (Ein Standardavatar wird vorübergehend angezeigt, während das des Benutzers in den Speicherort des Livefyre-Avatars hochgeladen wird.)

## Gravatar {#section_mqh_p1f_wy}

Livefyre unterstützt die Anwendung von Gravatars. Wenn ein Benutzer keinen benutzerdefinierten Avatar als Teil seines Benutzerprofils hat, sucht Livefyre nach einem Gravatar für diesen Benutzer. Wenn kein Gravatar vorhanden ist, wird der Standardavatar verwendet.


Apps, die diese Funktion verwenden:

* [Karussell](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Funktionskarte](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Landkarte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Medienwall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaik](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

