---
description: Ändern Sie Größe, Breite und Interaktionsoptionen der Mosaic-App.
seo-description: Ändern Sie Größe, Breite und Interaktionsoptionen der Mosaic-App.
seo-title: Mosaikanpassungen
solution: Experience Manager
title: Mosaikanpassungen
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mosaikanpassungen{#mosaic-customizations}

Ändern Sie Größe, Breite und Interaktionsoptionen der Mosaic-App.

Alle Apps verwenden **[!UICONTROL Style]** und **[!UICONTROL Config]** Optionen im **[!UICONTROL App Designer]**. Weitere Informationen zu den Standard- **[!UICONTROL Style]** und **[!UICONTROL Config]** Optionen für alle Apps finden Sie unter Anpassen von Apps im Abschnitt **[!UICONTROL App Designer.]**

Sie können Mosaic mit den folgenden zusätzlichen Optionen im App-Designer anpassen:

* **[!UICONTROL Content interaction]**. Legt den Stil fest, mit dem neue Inhalte auf die Seite geladen werden:

   * **[!UICONTROL Hover Fade]** zum Ausblenden auf die andere Seite einer Karte, wenn ein Besucher der Site den Mauszeiger über den Inhalt bewegt.
   * **[!UICONTROL Hover Flip]** , um zur anderen Seite einer Karte zu wechseln, wenn ein Besucher der Site den Mauszeiger über den Inhalt bewegt.
   * **[!UICONTROL Click]** , um die andere Seite einer Karte anzuzeigen, wenn ein Besucher der Site auf den Inhalt klickt.

* **[!UICONTROL Number of Tiles to Load]**. Die Anzahl der Kacheln, die in einem Mosaik geladen werden sollen. Dies kann sich auf die Ausgabeanzeige auswirken. Mosaik wird nur dann in einem Raster angezeigt, wenn Sie die richtige Anzahl von Kacheln für die Behälterbreite auswählen. Sie müssen diese ggf. anpassen, damit das Raster korrekt angezeigt wird.
* **[!UICONTROL Hide social branding when rights granted]** Schalten Sie dies ein, um das Logo für das ursprüngliche Social Media-Netzwerk (Twitter oder Instagram) zu entfernen, wenn Rechte für ein Inhaltselement gewährt werden.

* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten, um weitere Maßnahmen zu ergreifen.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Schalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.

   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, um sicherzustellen, dass der Eigentümer des Inhalts Rechte für den Inhalt erteilt hat, bevor eine Aktionsaufruf-Schaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Rechte für den Inhalt gewährt wurden. Die Schaltfläche "Aktionsaufruf"wird jedoch nur dann mit dem Inhalt angezeigt, wenn die Rechte für den Inhalt erteilt wurden.

   * **[!UICONTROL Show call-to-action in tile]**. Wählen Sie aus, ob die Aktionsaufruf-Schaltfläche auf einem Filmstreifen-Kachel angezeigt werden soll, anstatt die Aktionsaufruf-Schaltfläche nur anzuzeigen, wenn der Besucher der Site auf eine Karte klickt und den Inhalt in einem größeren Fenster öffnet.
   * **[!UICONTROL Call-to-action indication text]** Der anzuzeigende Text, der den Benutzer auffordert, auf die Karte zu klicken, um das Aktionsaufrufmodell zu öffnen.

   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile über der Aktionsaufruf-Schaltfläche im Inhaltsmodell angezeigt werden sollen. Die Standardformulierung lautet "Diese Produkte kaufen:".

   * **[!UICONTROL Call-to-action button text]** Passen Sie den Text auf der Schaltfläche Aktionsaufruf an. Der Standardtext lautet "Jetzt kaufen".

   * **[!UICONTROL Product display options]** Wählen Sie aus, ob Sie die Schaltfläche **[!UICONTROL Photo]** und die **[!UICONTROL Product name]** mit der Aktionsaufruf-Schaltfläche anzeigen möchten.

   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.

   * **[!UICONTROL Referral tracking key-value pairs]** Fügen Sie Parameter hinzu, um die Verweisverfolgung von Ihrem App-Inhalt zur entsprechenden Produktseite weiter anzugeben.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC für jede Produktseite in die App. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner auf der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Verwenden Sie STRG/Command + Klick, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um festzulegen, welche Produkte in diesem Ordner in der App auf verschiedenen Seiten angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht, aber mit einer anderen Produkt-ID versehen wurden. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die mit keinem Produkt verknüpft sind. Livefyre priorisiert den Inhalt zunächst mit derselben Produkt-ID, dann mit Inhalten, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann mit Inhalten, die ohne Produkt-IDs in der App veröffentlicht wurden.

Weitere Informationen zum Anpassen eines Mosaiks mithilfe von Livefyre.js finden Sie unter [Mosaic-Optionen](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) .
