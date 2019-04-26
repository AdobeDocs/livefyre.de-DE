---
description: Erlauben Sie Benutzern, das mit ihrem Inhalt angezeigte Bild anzupassen.
seo-description: Erlauben Sie Benutzern, das mit ihrem Inhalt angezeigte Bild anzupassen.
seo-title: Avatare
title: Avatare
uuid: bf 20 f 3 bc -3 dcc -4 e 16-a 629-3380 d 1 a 7 a 3 f 2
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Avatare{#avatars}

Erlauben Sie Benutzern, das mit ihrem Inhalt angezeigte Bild anzupassen.

Benutzeravatare werden (standardmäßig) neben den Inhalten in allen Apps angezeigt und aus dem in Ihrer Implementierung verwendeten Identitätsprofilsystem abgerufen. Die Größe dieser Avatare hängt von der App ab, in der sie angezeigt werden.

(In Livefyre können Sie Avatare deaktivieren, wenn Sie sie nicht in Ihren Apps anzeigen möchten.)

>[!NOTE]
>
>Avatare werden mit 25 p x 25 p für Chat und 50 p x 50 p in den meisten anderen Apps angezeigt.

## Avatar Storage {#section_zbh_x1f_wy}

Avatare werden asynchron in Livefyre geladen. Wenn ein Benutzer sich zuerst bei der App anmeldet oder die zugehörige Avatar-Bilddatei ändert, wird ihr Profilbild einer Aufgabenwarteschlange hinzugefügt. (Temporärer Avatar wird vorübergehend angezeigt, während der Benutzer auf den Livefyre-Avatar-Speicherort hochgeladen wird.)

## Gravatare {#section_mqh_p1f_wy}

Livefyre unterstützt die Verwendung von Gravatars. Wenn ein Benutzer über keinen benutzerdefinierten Avatar als Teil ihres Benutzerprofils verfügt, prüft Livefyre, ob dieser Benutzer ein Gravatar enthält. Wenn kein Gravatar vorhanden ist, wird der Standardavatar verwendet.

Wenn Kommentare mithilfe des Livefyre wordpress-Plugins eingebettet wurden, wird der Graphatar des Benutzers verwendet, wenn die folgenden Bedingungen erfüllt sind:

* Der Gravatar wurde im wordpress-Administratorbedienfeld aktiviert und
* der Benutzer über ein Gravatar-Konto verfügt und
* ein benutzerdefinierter Avatar nicht angegeben wird.

Weitere Informationen finden Sie in der wordpress-Grafik-Dokumentation.



Apps, die diese Funktion verwenden:

* [Karussell](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Map](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Medienpinnwand](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaik](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

