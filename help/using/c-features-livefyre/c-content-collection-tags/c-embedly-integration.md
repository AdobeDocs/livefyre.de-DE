---
description: Verwenden Sie embed.ly, um mehrere Medienformate direkt in der App anzuzeigen.
title: Embedly-Integration
exl-id: 859fe306-367e-4207-b9f7-c730ba0cd24d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 11%

---

# Embedly-Integration {#embedly-integration}

Verwenden Sie `embed.ly`, um mehrere Medienformate direkt in der App anzuzeigen.

Um eingebettete Medieninhalte aus verschiedenen Quellen, einschließlich Google Maps, YouTube, Flickr, Facebook, Instagram, Spotify und Tumblr, besser zu aktivieren, verwenden Livefyre-Apps Embedly als Drittanbieter für die URL-Erweiterung. Wenn ein Benutzer oder Moderator einen unterstützten Link in einem Beitrag enthält, werden die im Link enthaltenen Medien erweitert, sobald sie in der Sammlung veröffentlicht werden.

Dadurch erhalten Livefyre-Apps Zugriff auf die mehr als 250 verschiedenen eingebetteten Medienoptionen, die Embedly unterstützt.

>[!NOTE]
>
>Livefyre erweitert nur eine Teilmenge der vollständigen Provider-Liste von Embedly. Eingebettete Bilder werden nur dann auf HTTPS-Seiten erweitert, wenn der Anbieter Twitter, YouTube, Imgur, Vine, Wikipedia oder SoundCloud ist. Wenden Sie sich bei weiteren Fragen zur Linkerweiterung oder zu den Quellen bitte an Ihren technischen Kundenbetreuer.

Auf dieser Seite finden Sie Beispiele für beliebte eingebettete Medientypen und deren akzeptable URL-Muster. `Embed.ly` werden ständig neue Quellen hinzugefügt. Eine vollständige Liste der Anbieter finden Sie unter `https://embed.ly/embed/features/providers`.

>[!NOTE]
>
>Für die Formatierung &quot;Einbetten&quot;ist ein vollständiger Permalink erforderlich. Kürzere Links funktionieren nicht.

Nur öffentlich sichtbare Inhalte können eingebettet werden. Wenn Sie versuchen, einen Inhalt einzubetten, der nicht öffentlich ist, wird der Link zum Inhalt im Blog-Beitrag angezeigt und ein Platzhaltersymbol wird ihm beigefügt. Beim Klicken auf den Link erhält der Leser eine Fehlermeldung des Dienstes, in dem der Inhalt gehostet wird, z. B. eine Facebook-Meldung für ein Foto, das nur Freunde enthält. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie bemerken, dass Medien nicht wie erwartet erweitert werden.

## Beispiel für EinbettungsURLs

| Typ | Anbieter | URLs |
|--- |--- |--- |
| Karten | Google Maps | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Hinweis**: URL muss mit beginnen  `http` und nicht  `https.` |
| Soziale Netzwerke | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Video | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Fotos | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Content Upload-Dienst der Suite) | `https://ow.ly/i/*` |
| Umfragen | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Audio | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Apps, die diese Funktion verwenden:

* [Karussell](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Funktionskarte](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Landkarte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Medienwall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaik](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Umfragen](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sir](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Trends](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [Hochladen-Schaltfläche](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
