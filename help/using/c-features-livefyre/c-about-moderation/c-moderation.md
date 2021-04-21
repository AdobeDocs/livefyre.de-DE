---
description: Die Livefyre Spam and Missuse Filtering Engine (SAFE) ist ein Hintergrundprozess, der alle eingehenden Inhalte analysiert und für alle Livefyre-Kunden aktiviert ist.
title: SAFE-Regeln
exl-id: 13cd8df0-c4b7-436e-ba07-64ec67321d6b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# SAFE-Regeln{#safe-rules}

Die Livefyre Spam and Missuse Filtering Engine (SAFE) ist ein Hintergrundprozess, der alle eingehenden Inhalte analysiert und für alle Livefyre-Kunden aktiviert ist.



SAFE verwendet Musterregeln sowie statistische Modelle, um Spam, Missbrauch, Ernsthaftigkeit und (wiederholte) Massenbeiträge zu erkennen. Es wird von Zeit zu Zeit in anderen Livefyre-Produkten, insbesondere in den Content-Moderationstools und ModQ, referenziert.

>[!NOTE]
>
>SAFE ist nur auf Englisch verfügbar, mit Ausnahme der Bulk Mailing Classification. Wenn Sie Unterstützung für andere Sprachen benötigen, wenden Sie sich bitte an Ihren Strategischen Kundenbetreuer.

## Studio-Komponenten mit SAFE {#section_k34_4tx_vy}

Flags, die von SAFE angewendet werden, können mit den folgenden Studio-Komponenten verwendet werden:

* Regeln

   Sie können SAFE-Regeln definieren, um Inhalte automatisch zu kennzeichnen und zu definieren, wie gekennzeichnete Inhalte im **[!UICONTROL Network Settings]** behandelt werden sollen.

   Beispielsweise kann eine Site eine sehr niedrige Toleranz für Profitabilität festlegen und SAFE-Regeln definieren, die alle als Profane gekennzeichneten Inhalte als Bozo’d festlegen. Andere Sites können Regeln definieren, mit denen Profane-Inhalte vormoderiert werden, bevor sie in den Stream gelangen.

* ModQ

   Sie können Inhalte, die mit SAFE-Regeln und anderen Vormoderationsregeln gekennzeichnet sind (z. B. SPAM, Ernsthaftigkeit usw.), im ModQ moderieren.

* App-Inhalt in der Bibliothek

   Die von SAFE gekennzeichneten Inhalte werden auf der Registerkarte &quot;**[!UICONTROL Library]**&quot;im App-Inhalt aufgelistet. Sie können Inhalte nach Flags filtern, um Inhalte zu moderieren.

## SAFE-Filteroptionen {#section_pg5_ttx_vy}

SAFE wendet die folgenden Flags auf gefilterten Inhalt an und kann verwendet werden, um Regeln und moderaten Inhalt aus Livefyre Studio zu erstellen.

* **[!UICONTROL Profanity List]**: Profane Inhalte, wie durch eine Liste von englischen Suchbegriffen definiert, basierend auf der allgemeinen Verwendung.

   Der Profanity-Filter sucht auf der Grundlage einer getesteten Wortsprache nach professioneller Liste. Wenn der Inhalt erkannt wird, wird er als Profane gekennzeichnet.

   >[!NOTE]
   >
   >Livefyre bietet auch einen zweiten Profanity-Liste-Filter, den Sie sowohl auf Site- als auch auf Netzwerkebene anpassen können. Mit der Profanity-Liste erstellte Regeln haben Vorrang vor automatisierten Regeln, die aus dem SAFE-Profanity-Filter stammen. Weitere Informationen finden Sie im Abschnitt zur Profanity-Liste in der Einstellungsdokumentation.

* **[!UICONTROL Mild Profanity]**: Wörter und Ausdrücke sind in der Regel nicht akzeptabel in höflichen Unterhaltungen, sondern in der Regel akzeptabel in Gelegenheitsgesprächen. Im Allgemeinen sind diese Wörter und Ausdrücke im Netzwerk-Fernsehen zulässig.
* **[!UICONTROL Strong Profanity]**: Sehr starke Sprache, wie zum Beispiel Ausdrucke und Phrasen, die nicht im Netzwerk-Fernsehen erlaubt und sparsam in R-bewerteten Filmen und reife Kabel-TV-Shows verwendet werden. Im Allgemeinen werden diese Wörter nicht in höflichen oder zufälligen Gesprächen verwendet und in einem unhöflichen Gespräch mit der Absicht, dem Zuhörer zu schaden, gesagt.
* **[!UICONTROL SPAM]**: Unerbetene, meist kommerzielle Inhalte. Es verwendet ein statistisches Modell, das auf einer Vielzahl von Funktionen (einschließlich Kommentarinhalt und URLs) basiert, um einen Inhalt als SPAM zu kennzeichnen. Sie können Spam-Schwellenwerte anpassen, um die SPAM-Tagging-Raten für Ihr Netzwerk oder Ihre Site auf Anfrage anzupassen.
* **[!UICONTROL Mild Insult]**: Insulting content, wie durch eine Liste von Suchbegriffen und Wortmustern definiert.
* **[!UICONTROL Strong Insult]**: Insulting content, wie durch eine Liste von Suchbegriffen und Wortmustern definiert.
* **[!UICONTROL Hate Speech]**: Eine Beleidigung, die auf ethnischer oder religiöser Zugehörigkeit beruht, insbesondere wenn die Zugehörigkeit zur Zielpopulation in einer Minderheit oder einem Schutzgebiet liegt.
* **[!UICONTROL ALL CAPS]**: Text in Großbuchstaben (geleert).
* **[!UICONTROL Mild Threat]**: Eine Drohung oder Beleidigung, die normalerweise eine Art milde Abstammung gegen eine andere Person beinhaltet. Diese Option markiert mögliche Bedrohungen häufiger, weist aber auch eine höhere Falsch-Positiv-Rate auf als **[!UICONTROL Strong Threat]**.

* **[!UICONTROL Strong Threat]**: Eine ernsthafte Bedrohung oder Beleidigung, die einen oder mehrere Menschen, oft mit starker Ernsthaftigkeit, mit einem umsetzbaren Körper schädigen. Diese Option markiert mögliche Bedrohungen weniger häufig, weist aber auch eine niedrigere Falsch-Positiv-Rate auf als **[!UICONTROL Mild Threat]**.

* **[!UICONTROL Probable Nudity]**: Ein Bild, in dem es möglicherweise Nuancen aufweist. Diese Option markiert die Nacktheit weniger häufig, hat aber auch eine niedrigere Falsch-Positiv-Rate als **[!UICONTROL Possible Nudity]**.

* **[!UICONTROL Possible Nudity]**: Ein Bild, in dem es möglicherweise Nuancen aufweist. Diese Option markiert die Nacktheit häufiger, weist aber auch eine höhere Falsch-Positiv-Rate auf als **[!UICONTROL Probable Nudity]**.

* **[!UICONTROL PII]** (Persönlich identifizierbare Informationen): Informationen, die den Benutzer identifizieren können. Dazu können eine E-Mail-Adresse, eine physische Adresse, eine Sozialversicherungsnummer (für US-Kunden), eine Kreditkartennummer, ein Passwort oder alles andere gehören, das in Betrug verwendet werden kann oder um eine Identität zu erhalten.
* **[!UICONTROL Livefyre Recommends Trash]**. Legen Sie die Aktion fest, die das System ausführt, wenn die automatische Moderationsempfehlung Inhalte zur Ablehnung identifiziert.  ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >Um Moderation Recommendations zu aktivieren, wenden Sie sich an Ihre Adobe Livefyre Support Professional.

## Umgang mit Inhalten, die nicht von SAFE {#section_pjy_5tx_vy} erfasst werden

Es gibt mehrere Möglichkeiten, um Inhalte effektiv zu behandeln, die von diesem Filter nicht erfasst werden. Die unten aufgeführten Optionen sind in der empfohlenen Reihenfolge aufgeführt.

1. Entfernen Sie als Moderator den Inhalt aus dem Stream.
1. Erstellen Sie eine Flag-Regel, die besagt, wenn ein Inhaltselement von fünf Benutzern als Spam oder Offensiv gekennzeichnet wird, setzen Sie sie auf Bozo.
1. Verbieten Sie den Benutzer, der unerwünschte Inhalte veröffentlicht, damit alle Inhalte direkt in den Bozo-Status gelangen.
1. hinzufügen spezielle Wörter, die immer nach Ihrer profanen Liste gefiltert werden sollten.

>[!NOTE]
>
>Wenn ein Moderator Inhalte postet, die von unserem Spam-Filter erfasst werden, wird sie weiterhin als Spam gekennzeichnet, aber automatisch genehmigt und nicht auf Bozo eingestellt.

Wenn Sie Trends oder Muster von Inhalten feststellen, die nicht von SAFE erfasst werden, senden Sie eine E-Mail mit den Kommentar-IDs und dem Text an Ihre CSMs.



Apps, die diese Funktion verwenden:

* [Karussell](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Funktionskarte](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Landkarte](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Medienwall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaik](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sir](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Hochladen-Schaltfläche](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
