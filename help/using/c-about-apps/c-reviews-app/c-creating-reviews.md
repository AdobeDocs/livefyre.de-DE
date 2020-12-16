---
description: Hier finden Sie eine umfassende Auswahl an Anpassungen, mit denen Sie eine Review-App erstellen können, die Ihren Anforderungen und Ihrem Branding entspricht.
seo-description: Hier finden Sie eine umfassende Auswahl an Anpassungen, mit denen Sie eine Review-App erstellen können, die Ihren Anforderungen und Ihrem Branding entspricht.
seo-title: Erstellen einer Reviews-App
solution: Experience Manager
title: Erstellen einer Reviews-App
uuid: 6caeafe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---


# Erstellen einer Reviews-App{#creating-a-reviews-app}

Hier finden Sie eine umfassende Auswahl an Anpassungen, mit denen Sie eine Review-App erstellen können, die Ihren Anforderungen und Ihrem Branding entspricht.

Verwenden Sie die Reviews-App, indem Sie sie als JS-Anwendung benutzerdefiniert in Ihre Site einbetten. Sie können keine Reviews-App in Livefyre Studio erstellen. Informationen zum Erstellen einer Reviews-App auf Ihrer Site finden Sie unter [Reviews Integration](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Ratings {#section_hs5_c4h_21b}

Bewertungen sind der numerische Wert, den Ihre Benutzer der Überprüfung zuweisen. Jeder Review muss eine Bewertung enthalten, die standardmäßig als 5-Sterne-System angezeigt wird. (Während die Bewertungen in der App als 0,5 - 5 angezeigt werden, speichert Livefyre ein Verhältnis von X/100 im Backend, d. h., dass 1 Stern 20/100 und 2 Sterne 40/100 ist. Dieses Verhältnis wird angezeigt, wenn Sie die Reviews in Studio anzeigen.)

Die Bewertungsskala von 0,5 bis 5 kann bis zu einem Rating von 100 konfiguriert werden, wobei auch Halbwertsbewertungen verfügbar sind.

Weitere Informationen finden Sie im Feld maxRating für das Reviews convConfig-Objekt.

## Bewertungssymbol {#section_cqn_c4h_21b}

Die Bewertungssymbole können an Ihr Branding und Ihren Stil angepasst werden.

Weitere Informationen finden Sie unter **[!UICONTROL Configure Star Ratings]** unter Reviews Customization.

## Ratingstufen-Dimensionen {#section_cnx_snh_21b}

Bewertungsdimensionen sind die Kategorien, zu denen Ihre Prüfer Ihr Produkt oder Ihre Dienstleistung bewerten. Beispiele für Bewertungsdimensionen sind &quot;Leistung&quot;, &quot;Design&quot;, &quot;Kosten&quot;, &quot;Gesamt&quot;oder eine andere Kategorie, die Sie auswählen.

Standardmäßig wird eine &quot;Gesamt&quot;-Bewertungsdimension angezeigt, Sie können jedoch mehrere Ratingdimensionen definieren und implementieren, wie im Beispiel unten dargestellt.

Weitere Informationen finden Sie im Feld ratingDimensions unter Sammlungsmetadaten überprüfen.

## Textfelder {#section_xcm_4nh_21b} überprüfen

Sie können auch zusätzliche Textfelder in das Produkt oder Erlebnis einschließen, das geprüft wird. (Textfelder können z. B. &quot;Vor&quot;und &quot;Nachteile&quot;oder &quot;Nicht versäumen&quot;sein.) Die Zahl, der Titel und der Standardtext für das Feld können angepasst werden. Die Benutzer müssen alle Textfelder sowie den Titel, den Text und die Bewertung der Überprüfung ausfüllen, um ihre Überprüfung zu veröffentlichen. Es ist nicht möglich, optionale Textfelder einzuschließen.

Weitere Informationen finden Sie im Feld ratingDimensions für die Metadaten zur Überprüfung der Sammlung.

## Zusammenfassung {#section_ysz_lnh_21b}

Standardmäßig wird ein Übersichtsabschnitt oben in der Reviews-App angezeigt. Dieser Abschnitt enthält eine Visualisierung der durchschnittlichen Benutzerbewertung und der Bewertungsaufschlüsselung für die Reviews-Sammlung, wobei nur ganze Zahlen angezeigt werden. Dieser Abschnitt ist schreibgeschützt und kann bei Bedarf ausgeblendet werden.

Weitere Informationen finden Sie im Feld ratingSummaryEnabled für das Reviews convConfig-Objekt.

## Spam- und Wohlfühlfilter {#section_hcm_jnh_21b}

Der Text des Titels und des Body eines Reviews wird durch unseren Spam-Filter und Wohlfühlfilter weitergeleitet, sobald der Review veröffentlicht wird.

## Textanpassung {#section_tjf_hnh_21b}

Textzeichenfolgen, einschließlich QuickInfos und Etiketten, können für Ihre Sprache oder Marke angepasst werden.

## Antworten auf eine Überprüfung {#section_yng_fnh_21b}

Benutzer können in jeder Reviews-Sammlung auf die Review ihrer eigenen oder anderen reagieren. Nur angemeldete Benutzer können eine Antwort an eine Überprüfung posten.

Die Option, mit der Benutzer auf eine Überprüfung antworten können, ist in Studio aktiviert. Inhaber können diese Einstellung für die Netzwerk-, Site- oder Sammlungsebene umschalten. Moderatoren können diese Einstellung nur für ihre Sammlungen aktivieren.

## SocialSync und Kuratieren {#section_llh_2nh_21b}

Da Reviews darauf ausgelegt sind, jedem gesendeten Inhalt einen numerischen Wert hinzuzufügen, werden SocialSync und Kuratieren nicht von den Reviews unterstützt.

## Reviews APIs {#section_xrh_wmh_21b}

Reviews-APIs stehen zur Verfügung, damit Sie Informationen zu durchschnittlichen Benutzerbewertungen und Bewertungen sowie Aktivitäten zu Benutzerbewertungen in anderen Bereichen Ihrer Site anzeigen können.

[Bewertungen und Reviews](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Der Bootstrap-API-Endpunkt ermöglicht es Suchmaschinen wie Google, Ihre Rezension zu lesen, damit die Inhalte und Suchbegriffe Ihre Suchmaschinenoptimierung verbessern können.

* **[!UICONTROL Average User Ratings]** Die API für durchschnittliche Benutzerbewertungen ruft die durchschnittliche Benutzerbewertung für eine oder mehrere Reviews-Sammlungen ab, sodass Sie eine Visualisierung dieser Informationen auf einer Indexseite erstellen oder einer Suchindex-Seite hinzufügen können.

* **[!UICONTROL Ratings Breakdown]** Die API für die Aufschlüsselung von Bewertungen ruft eine Aufschlüsselung aller Bewertungen für eine bestimmte Reviews-Sammlung ab und ermöglicht Ihnen die Erstellung einer Visualisierung, die die Anzahl der Reviews anzeigt, die mit den einzelnen Bewertungen verknüpft sind.

* **[!UICONTROL User Reviews]** Die User Reviews API ruft die neuesten Reviews für einen bestimmten Benutzer ab. Diese Aktivität kann verwendet werden, um die Rezensionen eines Benutzers auf seiner Seite mit öffentlichem Profil anzuzeigen.
