---
description: Ändern Sie die Größe, Breite und Interaktionsoptionen der Karussell-App.
seo-description: Ändern Sie die Größe, Breite und Interaktionsoptionen der Karussell-App.
seo-title: Carousel mit Studio anpassen
solution: Experience Manager
title: Carousel mit Studio anpassen
uuid: 24 f 080 fc -37 bf -40 d 4-8 c 1 a-a 502 ee 8 ac 978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Carousel mit Studio anpassen{#customize-a-carousel-using-studio}

Ändern Sie die Größe, Breite und Interaktionsoptionen der Karussell-App.

Alle Apps verwenden und **[!UICONTROL Style]****[!UICONTROL Config]** Optionen in **[!UICONTROL App Designer]**. Weitere Informationen zum Standard **[!UICONTROL Style]** und den **[!UICONTROL Config]** Optionen für alle Apps im **[!UICONTROL App Designer]**Abschnitt finden Sie unter Anpassen von Apps.

Sie können Karussell mithilfe der folgenden zusätzlichen Optionen im App Designer anpassen:

* **[!UICONTROL Max Number of Items]**

   Legt fest, wie viele Elemente im Karussell angezeigt werden sollen. Der Standardwert ist 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Nur für Computerbildschirme

   * Wenn der Inhalt größer als 600 Pixel ist, wird horizontal angezeigt
   * Wenn der Inhalt kleiner als 600 Pixel ist, wird vertikal angezeigt
   * **Vertikal.** Für Computerbildschirme oder Mobilgeräte. Bei mobilen Geräten passt sich die Karte an die Größe des Bildschirms an.

* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Umschalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.
   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, damit der Inhaltsinhaber die Rechte für den Inhalt erteilt hat, bevor eine Aktionsaktionsschaltfläche für den Inhalt angezeigt wird.
   >[!NOTE]
   >
   >Der Inhalt wird auch dann angezeigt, wenn keine Berechtigungen für den Inhalt erteilt wurden. Die Aktionsaufruf-Schaltfläche wird jedoch mit dem Inhalt nur angezeigt, wenn die Rechte für den Inhalt gewährt werden.

   * **[!UICONTROL Show call-to-action in tile]**. Wählen Sie aus, ob die Aktionsaufruf-Schaltfläche auf einer Kachel angezeigt werden soll, anstatt die Aktionsaufruf-Schaltfläche nur anzuzeigen, wenn der Site-Besucher auf eine Karte klickt und den Inhalt in einem größeren Fenster öffnet.
   * **[!UICONTROL Call-to-action indication text]** Der anzuzeigende Text, um den Benutzer aufzufordern, auf die Karte zu klicken, um den Aktionsaufruf zu öffnen.
   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile oberhalb der Aktionsaufruf-Schaltfläche im Inhalt angezeigt werden sollen. Standardtext lautet: "Shop diese Produkte: ".
   * **[!UICONTROL Call-to-action button text]** Die Wörter, die in der Aktionsaufrufschaltfläche im Inhalt angezeigt werden sollen. Standardtext lautet: "Jetzt kaufen: ".
   * **[!UICONTROL Product display options]** Wählen Sie aus, ob Sie die **[!UICONTROL Photo]** Schaltfläche "Aktionsaufruf **[!UICONTROL Product name]** «und" Aktionsaufruf" anzeigen möchten.
   >[!NOTE]
   >
   >Die Schaltflächen "Foto" und" Produktname" markieren blau, wenn sie aktiviert sind.

   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.
   * **[!UICONTROL Referral tracking key-value pairs]** Fügen Sie Parameter hinzu, um die Verweisverfolgung aus Ihrem App-Inhalt auf die zugehörige Produktseite zu setzen.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC auf die App für jede Produktseite. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Wählen Sie Strg/Befehl + Klicken, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um zu bestimmen, welche Produkte in diesem Ordner auf verschiedenen Seiten in der App angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht wurden, aber mit einer anderen Produkt-ID getaggt sind. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die keinem Produkt zugeordnet sind. Livefyre priorisiert zuerst den Inhalt mit derselben Produkt-ID, dann Inhalte, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann Inhalte, die in der App ohne Produkt-IDs veröffentlicht wurden.
