---
description: 'null '
seo-description: 'null '
seo-title: Filmstreifen-Anpassungen
solution: Experience Manager
title: Filmstreifen-Anpassungen
uuid: 99f8b697-4aa3-4813-bcac-d0e0bdee252d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Filmstreifen-Anpassungen{#filmstrip-customizations}

Alle Apps verwenden **[!UICONTROL Style]** und **[!UICONTROL Config]** Optionen im **[!UICONTROL App Designer]**. Weitere Informationen zu den Standard- **[!UICONTROL Style]** und **[!UICONTROL Config]** Optionen für alle Apps finden Sie unter Anpassen von Apps im Abschnitt **[!UICONTROL App Designer.]**

Sie können den Filmstreifen mit den folgenden zusätzlichen Optionen im App-Designer anpassen:

* **[!UICONTROL Content fit]**. Wählen Sie **[!UICONTROL crop]** den Inhalt zum Ausfüllen der Karte aus oder **[!UICONTROL Aspect Ratio]** zum Anzeigen eines ganzen Bildes auf der Karte, unabhängig davon, ob die gesamte Karte gefüllt ist oder nicht.
* **[!UICONTROL Tile Size]**. Geben Sie die Größe der Kacheln in Pixel ein.
* **[!UICONTROL Show Notifications]**. Legen Sie fest, ob eine Benachrichtigung für neue Inhalte angezeigt werden soll, wenn diese in die Filmstreifen-App gestreamt werden.
* **[!UICONTROL Require rights]**. Aktivieren Sie diese Option, um nur Inhalte mit dem Berechtigungsanforderungsstatus "Genehmigt"anzuzeigen.
* **[!UICONTROL Hide social branding when rights granted]** Schalten Sie dies ein, um das Logo für das ursprüngliche Social Media-Netzwerk (Twitter oder Instagram) zu entfernen, wenn Rechte für ein Inhaltselement gewährt werden.
* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten, um weitere Maßnahmen zu ergreifen.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Schalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.
   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, um sicherzustellen, dass der Eigentümer des Inhalts Rechte für den Inhalt erteilt hat, bevor eine Aktionsaufruf-Schaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Rechte für den Inhalt gewährt wurden, die Aktionsaufruf-Schaltfläche jedoch nicht zusammen mit dem Inhalt angezeigt wird, wenn keine Rechte für den Inhalt gewährt wurden.

   * **[!UICONTROL Show call-to-action in tile]**. Wählen Sie aus, ob die Aktionsaufruf-Schaltfläche auf einem Filmstreifen-Kachel angezeigt werden soll, anstatt die Aktionsaufruf-Schaltfläche nur anzuzeigen, wenn der Besucher der Site auf eine Karte klickt und den Inhalt in einem größeren Fenster öffnet.
   * **[!UICONTROL Call-to-action indication text]** Der anzuzeigende Text, der den Benutzer auffordert, auf die Karte zu klicken, um das Aktionsaufrufmodell zu öffnen.
   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile über der Aktionsaufruf-Schaltfläche im Inhaltsmodell angezeigt werden sollen. Der Standardtext lautet "Shop these products:".
   * **[!UICONTROL Call-to-action button text]** Die Wörter, die im Inhalts-Modal in der Aktionsaufruf-Schaltfläche angezeigt werden sollen. Der Standardtext lautet "Jetzt kaufen:".
   * **[!UICONTROL Product display options]** Wählen Sie aus, ob Sie die Schaltfläche **[!UICONTROL Photo]** und die Schaltfläche **[!UICONTROL Product name]** mit dem Aktionsaufruf anzeigen möchten.

      >[!NOTE]
      >
      >Sowohl die Schaltflächen "Foto"als auch "Produktname"markieren Blau, wenn sie aktiviert sind.

   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.
   * **[!UICONTROL Referral tracking key-value pairs]** Fügen Sie Parameter hinzu, um die Verweisverfolgung von Ihrem App-Inhalt zur entsprechenden Produktseite weiter anzugeben.

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC für jede Produktseite in die App. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select product folders]**. Wählen Sie die Produktordner auf der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Verwenden Sie STRG/Command + Klick, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um festzulegen, welche Produkte in diesem Ordner in der App auf verschiedenen Seiten angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht, aber mit einer anderen Produkt-ID versehen wurden. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die mit keinem Produkt verknüpft sind. Livefyre priorisiert den Inhalt zunächst mit derselben Produkt-ID, dann mit Inhalten, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann mit Inhalten, die ohne Produkt-IDs in der App veröffentlicht wurden.

Weitere Informationen zum Anpassen eines Filmstreifens mit Livefyre.js finden Sie unter [Filmstreifenoptionen](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) .

