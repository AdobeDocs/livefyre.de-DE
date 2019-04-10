---
description: Reviews bieten eine umfassende Palette an Anpassungen, mit deren Hilfe
  Sie eine Review-App erstellen können, die Ihren Anforderungen und Branding entspricht.
seo-description: Reviews bieten eine umfassende Palette an Anpassungen, mit deren
  Hilfe Sie eine Review-App erstellen können, die Ihren Anforderungen und Branding
  entspricht.
seo-title: Erstellen einer Review-App
solution: Experience Manager
title: Erstellen einer Review-App
uuid: 6 cachte 7-c 04 e -484 e-b 02 f -98 dc 6 d 9 b 3184
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Erstellen einer Review-App{#creating-a-reviews-app}

Reviews bieten eine umfassende Palette an Anpassungen, mit deren Hilfe Sie eine Review-App erstellen können, die Ihren Anforderungen und Branding entspricht.

Verwenden Sie die Review-App, indem Sie sie benutzerspezifisch auf Ihrer Site als JS-Anwendung einbetten. In Livefyre Studio können Sie keine Review-App erstellen. Informationen zum Erstellen einer Review-App auf Ihrer Site finden Sie unter [Review-Integration](/help/implementation/c-app-integrations/c-reviews-integration.md).


## Bewertungen {#section_hs5_c4h_21b}

Ratings sind der numerische Wert, den Ihre Benutzer dem Review zuweisen. Jede Überprüfung muss eine Bewertung enthalten, die standardmäßig als 5 Sternchensystem angezeigt wird. (Während Bewertungen in der App als 0,5 - 5 angezeigt werden, speichert Livefyre ein Verhältnis von X/100 im Backend, sodass 1 Stern 20/100 und 2 Sterne 40/100 betragen. Dieses Verhältnis wird angezeigt, wenn die Reviews in Studio angezeigt werden.)

Die Bewertungsskala von 0,5 bis 5 kann bis zu einer Bewertung von 100 konfiguriert werden, mit halber Bewertung ebenfalls verfügbar.

Weitere Informationen finden Sie im Feld maxrating für das Reviewconfig-Objekt.

## Bewertungssymbolstil {#section_cqn_c4h_21b}

Bewertungssymbole können angepasst werden, um Ihr Branding und Stil anzupassen.

Weitere Informationen finden Sie **[!UICONTROL Configure Star Ratings]** unter Reviews Customization.

## Bewertungsdimensionen {#section_cnx_snh_21b}

Bewertungsdimensionen sind die Kategorien, in denen Ihre Überprüfer Ihr Produkt oder Ihren Dienst bewerten. Beispiele für Bewertungsdimensionen sind "Leistung" ," Entwurf" , "Kosten" ," Gesamt" oder eine andere Kategorie, die Sie auswählen.

Der Standardwert ist die Anzeige einer "Gesamt" -Bewertungsdimension, Sie können jedoch mehrere Bewertungsdimensionen definieren und implementieren, wie im Beispiel unten dargestellt.

Weitere Informationen finden Sie im Feld variabdimensions unter "Review Collection Metadata" .

## Textfelder überprüfen {#section_xcm_4nh_21b}

Sie können auch zusätzliche Textfelder in das betreffende Produkt oder Erlebnis einfügen. (Textfelder können beispielsweise "Pros" und" Cons" oder "Nicht Miss" lauten.) Die Anzahl, der Titel und der Standardtext für das Feld sind anpassbar. Benutzer müssen alle Textfelder sowie den Prüfungstitel, den Haupttext und die Bewertung abschließen, um ihre Überprüfung zu veröffentlichen. Optionale Textfelder sind nicht möglich.

Weitere Informationen finden Sie im Feld variabdimensions für die Überprüfungssammlung-Metadaten.

## Zusammenfassung überprüfen {#section_ysz_lnh_21b}

Standardmäßig wird oben in der Review-App ein Übersichtsabschnitt angezeigt. In diesem Abschnitt finden Sie eine Visualisierung der durchschnittlichen Benutzerbewertung und die Bewertung der Bewertung für die Sammlungssammlung, die nur ganze Zahlen anzeigt. Dieser Abschnitt ist schreibgeschützt und kann bei Bedarf ausgeblendet werden.

Weitere Informationen finden Sie im Feld ratingsummaryenabled für das Reviewconfig-Objekt.

## Spam und Gewinn-Filter {#section_hcm_jnh_21b}

Der Text einer Überprüfung und des Hauptteils der Überprüfung wird über unseren Spam Filter- und Gewinn-Filter weitergeleitet, sobald der Review gepostet wird.

## Textanpassung {#section_tjf_hnh_21b}

Textzeichenfolgen, einschließlich quickinfos und Bezeichnungen, können für die Sprache oder für Ihre Marke angepasst werden.

## Antworten auf eine Überprüfung {#section_yng_fnh_21b}

Benutzer können in jeder Reviews-Sammlung auf eigene oder andere Überprüfungen antworten. Nur Benutzer, die angemeldet sind, können eine Antwort auf einen Review posten.

Die Option für Benutzer, auf eine Überprüfung zu antworten, ist in Studio aktiviert. Inhaber können diese Einstellung für das Netzwerk, die Site oder die Sammlungsebene umschalten. Moderatoren können diese Einstellung nur für ihre Sammlungen aktivieren.

## Socialsync und Kuratieren {#section_llh_2nh_21b}

Da Reviews für jeden Teil des gesendeten Inhalts einen numerischen Wert hinzufügen sollen, werden socialsync und Kurate mit den Reviews nicht unterstützt.

## Prüft apis {#section_xrh_wmh_21b}

Überprüfungs-apis sind verfügbar, damit Sie durchschnittliche Angaben zur Benutzerbewertung und zur Bewertung von Bewertungswerten anzeigen können, und Benutzer Aktivitäten auf anderen Abschnitten Ihrer Site überprüfen können.

[Bewertungen und Überprüfungen](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Der Bootstrap-API-Endpunkt ermöglicht es Ihnen, Ihre Überprüfung von Suchmaschinen wie Google zu lesen, damit der Inhalt und die Suchbegriffe Ihre Suchmaschinenoptimierung verbessern können.

* **[!UICONTROL Average User Ratings]** Die durchschnittliche Benutzerbewertung API ruft die durchschnittliche Benutzerbewertung für eine oder mehrere Review-Sammlungen ab, sodass Sie eine Visualisierung dieser Informationen auf einer Indexseite erstellen oder einer Suchindex-Seite hinzufügen können.

* **[!UICONTROL Ratings Breakdown]** Die Analytics-Aufschlüsselungs-API ruft eine Aufschlüsselung aller Bewertungen für eine spezifische Überprüfungssammlung ab und ermöglicht es Ihnen, eine Visualisierung zu erstellen, die die Anzahl der mit den einzelnen Bewertungsstern verbundenen Reviews anzeigt.

* **[!UICONTROL User Reviews]** Die Benutzerüberprüfungs-API ruft die neuesten Überprüfungen für einen bestimmten Benutzer ab. Mit dieser Aktivität können Sie die Überprüfungen eines Benutzers auf ihrer öffentlichen Profilseite anzeigen.
