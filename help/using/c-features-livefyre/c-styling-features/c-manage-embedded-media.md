---
description: Definieren Sie die Quellen, aus denen Benutzer Medien veröffentlichen können, und die Quellen, aus denen Medienbeiträge verboten werden.
title: Verwalten von eingebetteten Medien
exl-id: f0cc257b-cc82-47bc-9d42-6aef3e0fe8a7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Verwalten von eingebetteten Medien{#manage-embedded-media}

Definieren Sie die Quellen, aus denen Benutzer Medien veröffentlichen können, und die Quellen, aus denen Medienbeiträge verboten werden.

Standardmäßig können alle Medienanlagen in Kommentare eingebettet werden. Eine umfassende Liste der unterstützten Anbieter finden Sie unter embed.ly/providers.

Livefyre verwendet zum Einbetten von Medien in App-Streams die Protokolle Embed.ly und Standard oEmbed und leitet alle von der Quelle bereitgestellten Mediendaten weiter.

Embed.ly leitet alle verfügbaren Informationen, einschließlich Titel, Beschreibung, Miniaturansicht und Einbettungscode des Mediums für eine angegebene URL, weiter. Die Verfügbarkeit dieser Artikel variiert je nach Anbieter. Beispiel: Facebook gibt keine Miniaturansichten für seine Videos zurück und übergibt nur ein eingebettetes Video. Durch Klicken auf &quot;Abspielen&quot;wird das Video Beginn (ähnlich dem Anzeigeformat von YouTube). Twitter gibt nur statische Bilder weiter und sendet keine Videos nach unten. Aus diesem Grund werden native Twitter-Videos möglicherweise nicht aus einem Livefyre-Stream abgespielt.

Beim Einbetten des Kommentarstreams können Sie verhindern, dass bestimmte Anlagen in Kommentare eingebettet werden. Sie können auch alle Embed.ly-Erweiterungen auf Netzwerk-, Site- und Konversationsebene mit Studio ausblenden, wobei nur Links zu den Medien, nicht vollständig eingebettete Medien angezeigt werden.

Apps, die diese Funktion verwenden:

* [Funktionskarte](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Landkarte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Medienwall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
