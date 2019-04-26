---
description: Verwenden Sie embed.ly, um mehrere Medienformate direkt in der App anzuzeigen.
seo-description: Verwenden Sie embed.ly, um mehrere Medienformate direkt in der App
  anzuzeigen.
seo-title: Embedly-Integration
solution: Experience Manager
title: Embedly-Integration
uuid: 1 f 27 e 32 c-c 2 c 3-4 f 7 c -93 de-c 9 c 7 bf 783 d 6 a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Embedly-Integration{#embedly-integration}

Verwenden `embed.ly` Sie diese Option, um mehrere Medienformate direkt in der App anzuzeigen.

Um eingebettete Medieninhalte aus verschiedenen Quellen wie Google Maps, youtube, Flickr, Facebook, Instagram, Spotify und Tumblr besser zu aktivieren, verwenden Livefyre Apps Embedly als Drittanbieter-Provider für die URL-Erweiterung. Wenn ein Benutzer oder Moderator einen unterstützten Link in einem Beitrag enthält, werden die im Link enthaltenen Medien bei der Veröffentlichung in der Sammlung erweitert.

Damit erhalten Livefyre-Apps Zugriff auf mehr als 250 verschiedene eingebettete Medienoptionen, die von Embedly unterstützt werden.

>[!NOTE]
>
>Livefyre erweitert nur eine Untergruppe der vollständigen Anbieterliste von Embedly. Eingebettete Bilder werden nur auf HTTPS-Seiten erweitert, wenn der Anbieter Twitter, youtube, Imgur, Revine, Wikipedia oder soundcloud ist. Weitere Fragen zur Link-Erweiterung oder zu den Quellen erhalten Sie von Ihrem technischen Kundenbetreuer.

Diese Seite listet Beispiele für einige beliebte eingebettete Medientypen und ihre zulässigen URL-Muster auf. `Embed.ly` laufend neue Quellen hinzufügen. Eine vollständige Liste der Anbieter `https://embed.ly/embed/features/providers`finden Sie unter.

>[!NOTE]
>
>Die Formatierung "Einbetten" erfordert einen vollständigen Permalink. Verkürzte Links funktionieren nicht.

Nur öffentlich sichtbare Inhalte können eingebettet werden. Wenn Sie versuchen, einen Inhalt einzubetten, der nicht öffentlich ist, wird der Link zum Inhalt im Blog-Beitrag angezeigt und ein Platzhaltersymbol wird angefügt. Wenn Sie auf klicken, wird der Leser zu einer Fehlermeldung vom Dienst weitergeleitet, in dem der Inhalt gehostet wird, z. B. eine Facebook-Nachricht für ein Nur-Freunde-Foto. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie bemerken, dass die Medien nicht wie erwartet erweitert werden.

## Beispiel-urls

| Typ | Anbieter | Urls |
|--- |--- |--- |
| Maps | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Hinweis**: URL muss `http` mit `https.` |
| Soziale Netzwerke | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Video | Youtube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Fotos | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | Twitpic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Hootsuite Content Uploading Service) | `https://ow.ly/i/*` |
| Umfragen | Gopollgo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Audio | Soundcloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Apps, die diese Funktion verwenden:

* [Karussell](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Map](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Medienpinnwand](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaik](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Umfragen](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Zielgruppen](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Trends](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Hochladen-Schaltfläche](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

