---
description: Fügen Sie mit einer Mosaic-App eine dynamische, dynamische Pinnwand,
  Fotos und Videos zu Ihrer Site hinzu.
seo-description: Fügen Sie mit einer Mosaic-App eine dynamische, dynamische Pinnwand,
  Fotos und Videos zu Ihrer Site hinzu.
seo-title: Mosaik
solution: Experience Manager
title: Mosaik
uuid: 331 c 5 f 80-7440-4 b 91-8 ac 6-4 f 56 a 8 a 5 befe
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mosaik{#mosaic}

Fügen Sie mit einer Mosaic-App eine dynamische, dynamische Pinnwand, Fotos und Videos zu Ihrer Site hinzu.

Mosaic wandelt benutzergenerierte Inhalte in eine dynamische Pinnwand und Fotos um, indem der neueste hochgeladene und soziale Medieninhalt in einem einheitlichen Rasterformat angezeigt wird.

Site-Besucher können den Mauszeiger über eine Mosaic-Karte bewegen, um Text und andere Inhaltsinformationen anzuzeigen. Mobile und nicht mobile Benutzer können eine Karte erweitern, um ein größeres Bild zu sehen, Inhalte freizugeben und Video abzuspielen. Wenn neue Elemente verfügbar werden, werden alte Elemente entfernt und in die Warteschlange versetzt, um das perfekte Raster zu bilden.

## Info zu Mosaic {#section_tng_slj_yy}

Mosaic zeigt die neuesten Livefyre- und Stream-Inhalte in einer einheitlichen Rasteranzeige an. Um ein nahtloses visuelles Erlebnis zu erstellen, werden Inhaltsinformationen nur bei der Maus angezeigt. Wenn neue Elemente verfügbar werden, werden alte Elemente entfernt und in die Warteschlange zurückgesetzt.

## Welche Art von Inhalt kann ich in Mosaic veröffentlichen? {#section_b5h_qlj_yy}

Unterstützte Inhalte, die Folgendes enthalten:

* Fotos
* Videos
* Audio

Unterstützte Inhaltsquellen:

* Twitter
* Instagram
* Facebook
* Youtube
* RSS
* Tumblr
* Livefyre
* Weibo

Inhalte, die Text enthalten, können nur in Mosaiken veröffentlicht werden, wenn sie Teil eines Foto- oder Videobeitrags sind.

## Wie sieht ein Site-Besucher Inhalte in einem Mosaik aus? {#section_w5c_plj_yy}

Ein Site-Besucher sieht Inhalte, die in einer Mosaic von Studio aus einem Studio-Stream oder Social Search gefüllt wurden. Wenn neue Inhalte in der App veröffentlicht werden, während sich ein Site-Besucher auf der Seite befindet, wird der neue Inhalt sofort angezeigt und der alte Inhalt wird in Echtzeit nach unten verschoben, ohne dass der Benutzer seine Seite aktualisieren muss.

## Was passiert, wenn ein Site-Besucher auf ein Element in einem Mosaik klickt? {#section_cvz_nlj_yy}

* Auf einem Desktop können Sie den Mauszeiger über die Karte bewegen, um ihn zu spiegeln und ein Erweiterungssymbol anzuzeigen. Klicken Sie auf das Symbol Erweitern, um ein größeres Bild anzuzeigen, ein Video anzusehen oder mehrere Medienelemente im Inhalt anzuzeigen.
* Auf einem Mobilgerät können Sie auf eine Karte klicken, um ein größeres Bild anzuzeigen, ein Video anzusehen oder mehrere Medienelemente im Inhalt anzuzeigen.

## Kann ein Site-Besucher Inhalte aus einem Mosaik freigeben? {#section_zzz_mlj_yy}

Ja. Ein Site-Besucher kann alle Inhaltstypen auf einem Mosaik freigeben:

* Auf einem Desktop bewegen Sie den Mauszeiger über die Karte und klicken Sie dann auf das Freigabesymbol.
* Klicken Sie auf einem Mobilgerät auf eine Karte, um sie zu öffnen, und klicken Sie auf das Freigabesymbol.

## Wie oft werden die Teile durch die Karten gedreht? {#section_hpx_llj_yy}

Alle 10 Sekunden wird ein neues Inhaltselement hinzugefügt.

## Wie werden neue Inhalte zu einem Mosaik hinzugefügt? {#section_f4w_klj_yy}

Inhalt zu Mosaic hinzufügen durch:

* Manuelles Veröffentlichen aus der Bibliothek.
* Einrichten eines Streams, der automatisch veröffentlicht werden soll.
* Verwenden der Schaltfläche "Hochladen" , falls aktiviert.

## Wie werden nur Text in der App angezeigt? {#section_h31_klj_yy}

Mosaic zeigt keine Nur-Text-Inhalte an. Mosaic zeigt nur Bilder und Videos an.

## Warum sehe ich in einer Mosaik manchmal graue Felder? {#section_i5c_jlj_yy}

Mosaic funktioniert am besten mit einer Sammlung, die ständig neue Inhalte enthält. Wenn Ihre App weniger als 25 Inhaltselemente aufweist, werden graustufen graue Felder angezeigt. Füllen Sie den Mosaik mit weiteren Inhalten aus, um die Anzeige grauer Felder zu verhindern. Planen Sie, mindestens 32 Inhaltselemente in der App bereitzustellen, damit sie wie vorgesehen angezeigt werden.

## Warum werden einige meiner Inhalte auf meiner Site nicht angezeigt, obwohl der Inhalt in Studio angezeigt wird? {#section_upr_hlj_yy}

Mosaic zeigt Inhalte in einem perfekten Raster an. Wenn Sie 25 Inhaltselemente haben, muss die Containerbreite fünf Inhaltselemente für alle 25 Inhaltselemente enthalten, damit sie angezeigt werden: fünf und fünf unten.

Wenn die Containerbreite nur vier zum perfekten Raster passt, aber 25 Inhaltselemente, klassifiziert Mosaic die zusätzliche Inhaltseinheit als Ausreißer und zeigt sie nicht in der App an. Der ausreißende Inhalt wird nicht gedreht, da er technisch gesehen in der App ist, aber nicht angezeigt wird. Wenn die Containerbreite sieben beträgt, wird nur 21 angezeigt, da vier Ausreißer sind und nicht das perfekte Raster bilden.

Manchmal wird Inhalt nicht angezeigt, da Sie sich eingeschaltet **[!UICONTROL Require rights]**haben. Wenn Sie dies aktivieren, müssen Sie über Rechte für alle Inhalte in der App verfügen. Wenn der Rechte-Status für ein Inhaltselement nicht "gewährt" wird, wird es nicht in der App angezeigt.

## Mosaic mit Studio erstellen {#section_dwb_glj_yy}

Sie können alle Apps in Livefyre Studio auf die gleiche Weise erstellen. Weitere Informationen zum Erstellen einer Mosaic-App in Studio mithilfe des Standardprozesses finden Sie unter Erstellen von Apps.

## Mosaik lokalisieren {#section_lnv_clj_yy}

Lokalisierung ist für Mosaic verfügbar. Sie können:

* Ändern der für Mosaic verfügbaren Zeichenfolgen
* Erstellen und Ändern einer Übersetzung für Mosaic
* Einen Übersetzungssatz auf eine Site anwenden
* Einen Übersetzungssatz auf ein Netzwerk anwenden

