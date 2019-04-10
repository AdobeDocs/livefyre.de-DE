---
description: null
seo-description: null
seo-title: Anpassungen des Filmstreifens
solution: Experience Manager
title: Anpassungen des Filmstreifens
uuid: 99 f 8 b 697-4 aa 3-4813-bcac-d 0 e 0 bdee 252 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Anpassungen des Filmstreifens{#filmstrip-customizations}

Alle Apps verwenden und **[!UICONTROL Style]****[!UICONTROL Config]** Optionen in **[!UICONTROL App Designer]**. Weitere Informationen zum Standard **[!UICONTROL Style]** und den **[!UICONTROL Config]** Optionen für alle Apps im Abschnitt **[!UICONTROL App Designer.]**

Sie können Filmstreifen mithilfe der folgenden zusätzlichen Optionen im App Designer anpassen:

* **[!UICONTROL Content fit]**. Wählen Sie den **[!UICONTROL crop]** Inhalt aus, um die Karte auszufüllen oder ein **[!UICONTROL Aspect Ratio]** ganzes Bild in der Karte anzuzeigen, unabhängig davon, ob es sich um die gesamte Karte handelt oder nicht.
* **[!UICONTROL Tile Size]**. Geben Sie die Größe der Kacheln in Pixel ein.
* **[!UICONTROL Show Notifications]**. Wählen Sie aus, ob Sie beim Streamen in die Filmstreifen-App eine Benachrichtigung für neue Inhalte anzeigen möchten.
* **[!UICONTROL Require rights]**. Aktivieren Sie diese Option, um nur Inhalte mit einem Berechtigungsanforderungsstatus "Gewährt" anzuzeigen.
* **[!UICONTROL Hide social branding when rights granted]** Schalten Sie dies ein, um das Logo für das Social-Media-Netzwerk (Twitter oder Instagram) zu entfernen, wenn die Rechte für ein Inhaltselement gewährt werden.
* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer für weitere Aktionen zu einem Produkt oder zu Ihrer Site zu leiten.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Umschalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.
   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, damit der Inhaltsinhaber die Rechte für den Inhalt erteilt hat, bevor eine Aktionsaktionsschaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Berechtigungen für den Inhalt erteilt wurden. Die Aktionsaufruf-Schaltfläche wird jedoch mit dem Inhalt nur angezeigt, wenn die Rechte für den Inhalt gewährt werden.

   * **[!UICONTROL Show call-to-action in tile]**. Wählen Sie aus, ob die Aktionsaufruf-Schaltfläche in einer Filmstreifen-Kachel angezeigt werden soll, anstatt die Aktionsaufruf-Schaltfläche nur anzuzeigen, wenn der Site-Besucher auf eine Karte klickt und den Inhalt in einem größeren Fenster öffnet.
   * **[!UICONTROL Call-to-action indication text]** Der anzuzeigende Text, um den Benutzer aufzufordern, auf die Karte zu klicken, um den Aktionsaufruf zu öffnen.
   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile oberhalb der Aktionsaufruf-Schaltfläche im Inhalt angezeigt werden sollen. Standardtext lautet: "Shop diese Produkte: ".
   * **[!UICONTROL Call-to-action button text]** Die Wörter, die in der Aktionsaufruf-Schaltfläche im Inhalt angezeigt werden sollen. Standardtext lautet: "Jetzt kaufen: ".
   * **[!UICONTROL Product display options]** Wählen Sie aus, ob die **[!UICONTROL Photo]** Aktionsaufruf-Schaltfläche **[!UICONTROL Product name]** angezeigt werden soll.

      >[!NOTE]
      >
      >Die Schaltflächen "Foto" und" Produktname" markieren blau, wenn sie aktiviert sind.

   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.
   * **[!UICONTROL Referral tracking key-value pairs]** Fügen Sie Parameter hinzu, um die Verweisverfolgung aus Ihrem App-Inhalt auf die zugehörige Produktseite zu setzen.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC auf die App für jede Produktseite. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select product folders]**. Wählen Sie die Produktordner der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Wählen Sie Strg/Befehl + Klicken, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um zu bestimmen, welche Produkte in diesem Ordner auf verschiedenen Seiten in der App angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht wurden, aber mit einer anderen Produkt-ID getaggt sind. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die keinem Produkt zugeordnet sind. Livefyre priorisiert zuerst den Inhalt mit derselben Produkt-ID, dann Inhalte, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann Inhalte, die in der App ohne Produkt-IDs veröffentlicht wurden.

Weitere Informationen zum Anpassen eines Filmstreifens mit Livefyre. js finden Sie unter [Filmstreifen-Optionen](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) .

