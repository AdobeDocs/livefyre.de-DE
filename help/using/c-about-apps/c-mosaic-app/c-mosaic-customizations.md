---
description: Ändern Sie die Größe, Breite und Interaktionsoptionen der Mosaic-App.
seo-description: Ändern Sie die Größe, Breite und Interaktionsoptionen der Mosaic-App.
seo-title: Mosaikanpassungen
solution: Experience Manager
title: Mosaikanpassungen
uuid: 4 e 226 d 68-f 517-4922-bc 25-655 d 524 d 7 d 52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mosaikanpassungen{#mosaic-customizations}

Ändern Sie die Größe, Breite und Interaktionsoptionen der Mosaic-App.

Alle Apps verwenden und **[!UICONTROL Style]****[!UICONTROL Config]** Optionen in **[!UICONTROL App Designer]**. Weitere Informationen zum Standard **[!UICONTROL Style]** und den **[!UICONTROL Config]** Optionen für alle Apps im Abschnitt **[!UICONTROL App Designer.]**

Sie können Mosaic mithilfe der folgenden zusätzlichen Optionen im App Designer anpassen:

* **[!UICONTROL Content interaction]**. Legt den Stil fest, mit dem neue Inhalte auf die Seite geladen werden:

   * **[!UICONTROL Hover Fade]** zum Ausblenden auf die andere Seite einer Karte, wenn der Besucher den Mauszeiger über den Inhalt bewegt.
   * **[!UICONTROL Hover Flip]** , um auf der anderen Seite einer Karte zu spiegeln, wenn der Besucher den Mauszeiger über den Inhalt bewegt.
   * **[!UICONTROL Click]** , um die andere Seite einer Karte anzuzeigen, wenn ein Site-Besucher auf den Mauszeiger auf den Inhalt klickt.

* **[!UICONTROL Number of Tiles to Load]**. Die Anzahl der in Mosaic zu ladenden Elemente. Dies kann sich auf die Anzeige auswirken. Mosaiken werden nur dann in einem Raster angezeigt, wenn Sie die richtige Anzahl an Kacheln zur Containerbreite auswählen. Möglicherweise müssen Sie diese anpassen, damit das Raster korrekt angezeigt wird.
* **[!UICONTROL Hide social branding when rights granted]** Schalten Sie dies ein, um das Logo für das Social-Media-Netzwerk (Twitter oder Instagram) zu entfernen, wenn die Rechte für ein Inhaltselement gewährt werden.

* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Umschalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.

   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, damit der Inhaltsinhaber die Rechte für den Inhalt erteilt hat, bevor eine Aktionsaktionsschaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Berechtigungen für den Inhalt erteilt wurden. Die Schaltfläche &quot;Aktionsaufruf&quot; wird jedoch nur mit dem Inhalt angezeigt, wenn die Rechte für den Inhalt nicht gewährt werden.

   * **[!UICONTROL Show call-to-action in tile]**. Wählen Sie aus, ob die Aktionsaufruf-Schaltfläche in einer Filmstreifen-Kachel angezeigt werden soll, anstatt die Aktionsaufruf-Schaltfläche nur anzuzeigen, wenn der Site-Besucher auf eine Karte klickt und den Inhalt in einem größeren Fenster öffnet.
   * **[!UICONTROL Call-to-action indication text]** Der anzuzeigende Text, um den Benutzer aufzufordern, auf die Karte zu klicken, um den Aktionsaufruf zu öffnen.

   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile oberhalb der Aktionsaufruf-Schaltfläche im Inhalt angezeigt werden sollen. Standardtext lautet: &quot;Shop diese Produkte: &quot;.

   * **[!UICONTROL Call-to-action button text]** Passen Sie den Text auf der Aktionsaktionsschaltfläche an. Standardtext ist &quot;Jetzt kaufen&quot; .

   * **[!UICONTROL Product display options]** Wählen Sie aus, ob Sie die **[!UICONTROL Photo]** Schaltfläche &quot;Aktionsaufruf **[!UICONTROL Product name]** «und&quot; Aktionsaufruf&quot; anzeigen möchten.

   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.

   * **[!UICONTROL Referral tracking key-value pairs]** Fügen Sie Parameter hinzu, um die Verweisverfolgung aus Ihrem App-Inhalt auf die zugehörige Produktseite zu setzen.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC auf die App für jede Produktseite. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Wählen Sie Strg/Befehl + Klicken, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um zu bestimmen, welche Produkte in diesem Ordner auf verschiedenen Seiten in der App angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht wurden, aber mit einer anderen Produkt-ID getaggt sind. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die keinem Produkt zugeordnet sind. Livefyre priorisiert zuerst den Inhalt mit derselben Produkt-ID, dann Inhalte, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann Inhalte, die in der App ohne Produkt-IDs veröffentlicht wurden.

Weitere Informationen zum Anpassen von Mosaic mit Livefyre. js finden Sie unter [Mosaic-Optionen](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) .
