---
description: Ändern Sie Größe, Breite und Interaktionsoptionen der Mosaic-App.
title: Mosaikanpassungen
exl-id: 0223a64c-ec33-4e01-85d7-11845c9b8476
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# Mosaic-Anpassungen{#mosaic-customizations}

Ändern Sie Größe, Breite und Interaktionsoptionen der Mosaic-App.

Alle Apps verwenden die Optionen **[!UICONTROL Style]** und **[!UICONTROL Config]** in **[!UICONTROL App Designer]**. Weitere Informationen zu den Standardoptionen **[!UICONTROL Style]** und **[!UICONTROL Config]** für alle Apps in **[!UICONTROL App Designer.]** finden Sie unter Anpassen von Apps.

Sie können Mosaic mit den folgenden zusätzlichen Optionen im App-Designer anpassen:

* **[!UICONTROL Content interaction]**. Legt den Stil fest, mit dem neue Inhalte auf die Seite geladen werden:

   * **[!UICONTROL Hover Fade]** zum Ausblenden auf der anderen Seite einer Karte, wenn ein Site-Besucher den Mauszeiger über den Inhalt bewegt.
   * **[!UICONTROL Hover Flip]** , um zur anderen Seite einer Karte zu wechseln, wenn ein Site-Besucher den Mauszeiger über den Inhalt bewegt.
   * **[!UICONTROL Click]** , um die andere Seite einer Karte anzuzeigen, wenn ein Site-Besucher mit der Maus auf den Inhalt klickt.

* **[!UICONTROL Number of Tiles to Load]**. Die Anzahl der Kacheln, die in einem Mosaik geladen werden sollen. Dies kann sich auf die Ausgabeanzeige auswirken. Mosaik wird nur dann in einem Raster angezeigt, wenn Sie die richtige Anzahl von Kacheln für die Breite des Containers auswählen. Sie müssen diese ggf. anpassen, damit das Raster korrekt angezeigt wird.
* **[!UICONTROL Hide social branding when rights granted]** Schalten Sie dies ein, um das Logo für das ursprüngliche Social Media-Netzwerk (Twitter oder Instagram) zu entfernen, wenn Rechte für ein Inhaltselement gewährt werden.

* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten, um weitere Maßnahmen zu ergreifen.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Schalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.

   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, um sicherzustellen, dass der Eigentümer des Inhalts Rechte für den Inhalt erteilt hat, bevor eine Aktionsaufruf-Schaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Rechte für den Inhalt gewährt wurden. Die Schaltfläche &quot;Aktionsaufruf&quot;wird jedoch nur dann mit dem Inhalt angezeigt, wenn die Rechte für den Inhalt erteilt wurden.

   * **[!UICONTROL Show call-to-action in tile]**. Wählen Sie aus, ob die Aktionsaufruf-Schaltfläche auf einem Filmstreifen-Kachel angezeigt werden soll, anstatt die Aktionsaufruf-Schaltfläche nur anzuzeigen, wenn der Site-Besucher auf eine Karte klickt und den Inhalt in einem größeren Fenster öffnet.
   * **[!UICONTROL Call-to-action indication text]** Der anzuzeigende Text, der den Benutzer auffordert, auf die Karte zu klicken, um das Aktionsaufrufmodell zu öffnen.

   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile über der Aktionsaufruf-Schaltfläche im Inhaltsmodell angezeigt werden sollen. Die Standardformulierung lautet &quot;Diese Produkte kaufen:&quot;.

   * **[!UICONTROL Call-to-action button text]** Passen Sie den Text auf der Schaltfläche Aktionsaufruf an. Der Standardtext lautet &quot;Jetzt kaufen&quot;.

   * **[!UICONTROL Product display options]** Legen Sie fest, ob die Schaltfläche  **[!UICONTROL Photo]** und die Schaltfläche  **[!UICONTROL Product name]** mit der Aktionsaufruf angezeigt werden sollen.

   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.

   * **[!UICONTROL Referral tracking key-value pairs]** hinzufügen Parameter, um die Verweisverfolgung von Ihrem App-Inhalt auf die zugehörige Produktseite weiter anzugeben.

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC für jede Produktseite in die App. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner auf der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Verwenden Sie STRG/Command + Klick, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um festzulegen, welche Produkte in diesem Ordner in der App auf verschiedenen Seiten angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht, aber mit einer anderen Produkt-ID versehen wurden. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die nicht mit einem Produkt verknüpft sind. Livefyre priorisiert den Inhalt zunächst mit derselben Produkt-ID, dann mit Inhalten, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann mit Inhalten, die ohne Produkt-IDs in der App veröffentlicht wurden.

Weitere Informationen zum Anpassen eines Mosaiks mit Livefyre.js finden Sie unter [Mosaic-Optionen](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md).
