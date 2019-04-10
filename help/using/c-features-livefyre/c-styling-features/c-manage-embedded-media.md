---
description: Definieren Sie die Quellen, aus denen Benutzer Medien veröffentlichen
  können, und diejenigen, aus denen Medienbeiträge verboten werden.
seo-description: Definieren Sie die Quellen, aus denen Benutzer Medien veröffentlichen
  können, und diejenigen, aus denen Medienbeiträge verboten werden.
seo-title: Eingebettete Medien verwalten
title: Eingebettete Medien verwalten
uuid: d 8621 be 1-dcfb -429 f -954 e-b 21 fdcf 2715
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Eingebettete Medien verwalten{#manage-embedded-media}

Definieren Sie die Quellen, aus denen Benutzer Medien veröffentlichen können, und diejenigen, aus denen Medienbeiträge verboten werden.

Standardmäßig können alle Medienanlagen in Kommentare eingebettet werden. Eine umfassende Liste der unterstützten Anbieter finden Sie unter embed.ly/providers.

Livefyre verwendet eingebettete. ly- und standardmäßige oembed-Protokolle, um Medien in App-Streams einzubetten, und übergeben alle Mediendaten, die von der Quelle bereitgestellt werden.

" Eingebettet. ly" durchläuft alle verfügbaren Informationen, einschließlich Titel, Beschreibung, Miniaturansicht und Einbettungscode des Mediums für jede beliebige URL. Die Verfügbarkeit dieser Elemente variiert je nach Anbieter. Beispiel: Facebook gibt keine Miniaturansichten für seine Videos zurück und übergibt nur ein einbettbares Video. Durch Klicken auf "Abspielen" wird das Video gestartet (ähnlich wie das Anzeigeformat von youtube). Twitter übergibt nur statische Bilder und sendet keine Videos. Aus diesem Grund werden native Twitter-Videos in einem Livefyre-Stream möglicherweise nicht wiedergegeben.

Sie können verhindern, dass bestimmte Anhänge in Kommentare eingebettet werden, wenn Sie den Kommentarstream einbetten. Sie können auch alle ausgeblendeten. ly-Erweiterungen im Netzwerk, auf der Site- und Unterhaltungsebene mit Studio ausblenden und nur Links zu den Medien, nicht vollständig eingebettete Medien anzeigen.

Apps, die diese Funktion verwenden:

* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Map](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Medienpinnwand](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)

