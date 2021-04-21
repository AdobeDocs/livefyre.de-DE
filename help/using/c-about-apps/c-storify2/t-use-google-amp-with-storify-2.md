---
description: Verwenden Sie Livefyre-APIs, um Ihrer Storify 2-Seite Google AMP-Funktionen hinzuzufügen, damit der Inhalt interaktiv und SEO-freundlich bleibt.
title: Google AMP mit Storify 2 verwenden
exl-id: 2fee8655-ac9f-484e-a042-9b7ac7151fcc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Google AMP mit Storify 2{#use-google-amp-with-storify} verwenden

Verwenden Sie Livefyre-APIs, um Ihrer Storify 2-Seite Google AMP-Funktionen hinzuzufügen, damit der Inhalt interaktiv und SEO-freundlich bleibt.

Um Google AMP mit Storify 2 zu verwenden, müssen Sie eine Seite für Ihre Storify 2-App mit Google AMP-Markup erstellen.

Die AMP-Version der App-Anforderung wird von der Originalseite aktualisiert (verwenden Sie den Parameter **pollInterval** in der **amp-live-Liste**-API, um das Intervall für Updateanforderungen festzulegen). Um sicherzustellen, dass Besucher auf Ihrer AMP-Seite schnell die aktuellsten Inhalte erhalten, sollten Sie eine TTL mit niedrigem Cache auf Ihren Storify 2 AMP-Seiten verwenden.

Nicht-Bild-Assets (z. B. Videos), die als Beiträge in einer Storify 2-App enthalten sind, müssen HTTPS gemäß der AMP-Spezifikation verwenden. AMP-URLs, die das Google Cloud Content Versand Network (CDN) verwenden, verwenden HTTPS.

So verwenden Sie Google AMP mit Storify 2:

1. Erstellen Sie eine AMP-validierte Vorlage auf Ihrer Site.
1. Verwenden Sie eine oder mehrere der folgenden Google AMP-APIs, um Ihre Google AMP-Seite anzupassen:
   1. [amp-](https://www.ampproject.org/docs/reference/components/amp-iframe) iframe zum Anpassen der Storify 2-Anzeige
   1. [amp-live-](https://www.ampproject.org/docs/reference/components/amp-live-list) list zum Anpassen des Zeitintervalls für Updates
   1. [amp-social-](https://www.ampproject.org/docs/reference/components/amp-social-share) shareto add an social sharing button
1. Fügen Sie den Inhalt der folgenden Storify 2 AMP-Seite in das CSS für Ihre Storify 2-Seite im `<style amp-custom>`-Tag ein: [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. Schließen Sie den Inhalt der folgenden Storify 2 AMP-Markup-API in Ihre Google AMP-Vorlage ein: `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` wobei {{APP_ID}} die App-ID für die Storify 2-App in Livefyre Studio ist.
   1. Der einzige Parameter für die Abfrage ist **pollInterval**. Dies ist das Intervall, in dem die App nach Updates sucht (in Millisekunden eingestellt).
   1. Die URL enthält Inhalte aus den neuesten Beiträgen (einschließlich Tweets, Videos usw.)
   1. Die Herausgeberseite muss Inhalte aus dieser URL so oft abrufen, wie die Google AMP-Seite aktualisiert werden soll.
