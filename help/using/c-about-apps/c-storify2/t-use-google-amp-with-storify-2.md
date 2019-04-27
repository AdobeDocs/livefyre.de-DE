---
description: Verwenden Sie Livefyre-apis, um Ihrer Storify 2-Seite Google AMP-Funktionen hinzuzufügen, um den Inhalt interaktiv und SEO-freundlich zu halten.
seo-description: Verwenden Sie Livefyre-apis, um Ihrer Storify 2-Seite Google AMP-Funktionen hinzuzufügen, um den Inhalt interaktiv und SEO-freundlich zu halten.
seo-title: Google AMP mit Storify 2 verwenden
solution: Experience Manager
title: Google AMP mit Storify 2 verwenden
uuid: 40 c 9 f 083-7284-43 ba-ae 27-53 b 1 ff 9 e 3954
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Google AMP mit Storify 2 verwenden{#use-google-amp-with-storify}

Verwenden Sie Livefyre-apis, um Ihrer Storify 2-Seite Google AMP-Funktionen hinzuzufügen, um den Inhalt interaktiv und SEO-freundlich zu halten.

Um Google AMP mit Storify 2 zu verwenden, müssen Sie eine Seite für Ihre Storify 2 App mit Google AMP markup erstellen.

Die AMP-Version der App fordert Updates von der Originalseite an (verwenden Sie den **pollinterval** -Parameter in der **amp-live-list** -API, um das Intervall für Updateanforderungen festzulegen). Um sicherzustellen, dass Besucher auf Ihrer AMP-Seite den aktuellsten Inhalt schnell erhalten, sollten Sie einen niedrigen Cache-TTL auf Ihren Storify 2 AMP-Seiten verwenden.

Nicht Bild-Assets (z. B. Videos), die als Beiträge in einer Storify 2-App enthalten sind, müssen HTTPS verwenden, wie in der AMP-Spezifikation angegeben. AMP-urls, die CDN (Google Cloud Content Delivery Network) verwenden, verwenden HTTPS.

So verwenden Sie Google AMP mit Storify 2:

1. Erstellen Sie eine AMP-validierte Vorlage auf Ihrer Site.
1. Verwenden Sie eines oder mehrere der folgenden Google AMP-apis, um Ihre Google AMP-Seite anzupassen:
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) zur Anpassung der Storify 2-Anzeige
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) zur Anpassung des Zeitintervalls für Updates
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) zum Hinzufügen einer Schaltfläche Social Sharing
1. Fügen Sie den Inhalt der folgenden Storify 2 AMP-Seite in die CSS für Ihre Storify 2-Seite im <style amp-custom> -tag: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Fügen Sie den Inhalt der folgenden Storify 2 AMP-Markup-API in Ihre Google AMP-Vorlage ein: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` wobei {{APP_ ID}} die App-ID für die Storify 2-App in Livefyre Studio ist.
   1. Der einzige Abfrageparameter ist **pollinterval**, d. h. das Intervall, in dem die App nach Aktualisierungen sucht (in Millisekunden festgelegt).
   1. Die URL enthält Inhalte aus den letzten Beiträgen (einschließlich Tweets, Videos usw.)
   1. Die Herausgeberseite muss Inhalte aus dieser URL abrufen, so oft Sie die Google AMP-Seite aktualisieren möchten.
