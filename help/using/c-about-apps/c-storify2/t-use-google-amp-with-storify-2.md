---
description: Verwenden Sie Livefyre-APIs, um Ihrer Storify 2-Seite Google AMP-Funktionen hinzuzufügen, damit der Inhalt interaktiv und SEO-freundlich bleibt.
seo-description: Verwenden Sie Livefyre-APIs, um Ihrer Storify 2-Seite Google AMP-Funktionen hinzuzufügen, damit der Inhalt interaktiv und SEO-freundlich bleibt.
seo-title: Google AMP mit Storify 2 verwenden
solution: Experience Manager
title: Google AMP mit Storify 2 verwenden
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 65d931e5bd04964db44f8e3a0e000ecec2652893
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# Google AMP mit Storify 2 verwenden{#use-google-amp-with-storify}

Verwenden Sie Livefyre-APIs, um Ihrer Storify 2-Seite Google AMP-Funktionen hinzuzufügen, damit der Inhalt interaktiv und SEO-freundlich bleibt.

Um Google AMP mit Storify 2 zu verwenden, müssen Sie eine Seite für Ihre Storify 2-App mit Google AMP-Markup erstellen.

Die AMP-Version der App fordert Aktualisierungen von der Originalseite an (verwenden Sie den Parameter **pollInterval** in der API **amp-live-Liste** , um das Intervall für Updateanforderungen festzulegen). Um sicherzustellen, dass Besucher auf Ihrer AMP-Seite schnell die aktuellsten Inhalte erhalten, sollten Sie eine TTL mit niedrigem Cache auf Ihren Storify 2 AMP-Seiten verwenden.

Nicht-Bild-Assets (z. B. Videos), die als Beiträge in einer Storify 2-App enthalten sind, müssen HTTPS gemäß der AMP-Spezifikation verwenden. AMP-URLs, die das Google Cloud Content Versand Network (CDN) verwenden, verwenden HTTPS.

So verwenden Sie Google AMP mit Storify 2:

1. Erstellen Sie eine AMP-validierte Vorlage auf Ihrer Site.
1. Verwenden Sie eine oder mehrere der folgenden Google AMP-APIs, um Ihre Google AMP-Seite anzupassen:
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) zum Anpassen der Storify 2-Anzeige
   1. [amp-live-Liste](https://www.ampproject.org/docs/reference/components/amp-live-list) zum Anpassen des Zeitintervalls für Updates
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) to add a social sharing button
1. Fügen Sie den Inhalt der folgenden Storify 2 AMP-Seite in das CSS für Ihre Storify 2-Seite innerhalb des `<style amp-custom>` -Tags ein: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Schließen Sie den Inhalt der folgenden Storify 2 AMP-Markup-API in Ihre Google AMP-Vorlage ein: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` wobei {{APP_ID}} die App-ID für die Storify 2-App in Livefyre Studio ist.
   1. Der einzige Abfrage-Parameter ist **pollInterval**, d. h. das Intervall, in dem die App nach Updates sucht (in Millisekunden eingestellt).
   1. Die URL enthält Inhalte aus den neuesten Beiträgen (einschließlich Tweets, Videos usw.)
   1. Die Herausgeberseite muss Inhalte aus dieser URL so oft abrufen, wie die Google AMP-Seite aktualisiert werden soll.
