---
description: Ändern Sie Größe, Breite und Interaktionsoptionen der Karussell-App.
seo-description: Ändern Sie Größe, Breite und Interaktionsoptionen der Karussell-App.
seo-title: Karussell mit Studio anpassen
solution: Experience Manager
title: Karussell mit Studio anpassen
uuid: 24f080fc-37bf-40d4-8c1a-a502ee8ac978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---


# Karussell mit Studio{#customize-a-carousel-using-studio} anpassen

Ändern Sie Größe, Breite und Interaktionsoptionen der Karussell-App.

Alle Apps verwenden die Optionen **[!UICONTROL Style]** und **[!UICONTROL Config]** in **[!UICONTROL App Designer]**. Weitere Informationen zu den Standardoptionen **[!UICONTROL Style]** und **[!UICONTROL Config]** für alle Apps in **[!UICONTROL App Designer]** finden Sie unter Anpassen von Apps.

Sie können ein Karussell mit den folgenden zusätzlichen Optionen im App-Designer anpassen:

* **[!UICONTROL Max Number of Items]**

   Legt die Anzahl der Elemente fest, die im Karussell angezeigt werden sollen. Standardwert ist 50.

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. Nur für Computerbildschirme

   * Wenn der Inhalt größer als 600 Pixel ist, wird horizontal angezeigt
   * Wenn der Inhalt kleiner als 600 Pixel ist, wird vertikal angezeigt
   * **Vertikal.** Für Computerbildschirme oder Mobilgeräte. Bei Mobilgeräten schrumpft die Karte, um sie an die Bildschirmgröße anzupassen.

* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten, um weitere Maßnahmen zu ergreifen.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Schalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.
   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, um sicherzustellen, dass der Eigentümer des Inhalts Rechte für den Inhalt erteilt hat, bevor eine Aktionsaufruf-Schaltfläche für den Inhalt angezeigt wird.

   >[!NOTE]
   >
   >Der Inhalt wird auch dann angezeigt, wenn keine Rechte für den Inhalt gewährt wurden, die Aktionsaufruf-Schaltfläche jedoch nicht zusammen mit dem Inhalt angezeigt wird, wenn keine Rechte für den Inhalt gewährt wurden.

   * **[!UICONTROL Show call-to-action in tile]**. Wählen Sie aus, ob die Aktionsaufruf-Schaltfläche auf einer Kachel angezeigt werden soll, anstatt die Aktionsaufruf-Schaltfläche nur anzuzeigen, wenn der Site-Besucher auf eine Karte klickt und den Inhalt in einem größeren Fenster öffnet.
   * **[!UICONTROL Call-to-action indication text]** Der anzuzeigende Text, der den Benutzer auffordert, auf die Karte zu klicken, um das Aktionsaufrufmodell zu öffnen.
   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile über der Aktionsaufruf-Schaltfläche im Inhaltsmodell angezeigt werden sollen. Der Standardtext lautet &quot;Shop these products:&quot;.
   * **[!UICONTROL Call-to-action button text]** Die Wörter, die im Inhalts-Modal in der Schaltfläche Aktionsaufruf angezeigt werden sollen. Der Standardtext lautet &quot;Jetzt kaufen:&quot;.
   * **[!UICONTROL Product display options]** Legen Sie fest, ob die Schaltfläche  **[!UICONTROL Photo]** und die Schaltfläche  **[!UICONTROL Product name]** mit der Aktionsaufruf angezeigt werden sollen.

   >[!NOTE]
   >
   >Sowohl die Schaltflächen &quot;Foto&quot;als auch &quot;Produktname&quot;markieren Blau, wenn sie aktiviert sind.

   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.
   * **[!UICONTROL Referral tracking key-value pairs]** hinzufügen Parameter, um die Verweisverfolgung von Ihrem App-Inhalt auf die zugehörige Produktseite weiter anzugeben.



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC für jede Produktseite in die App. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner auf der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Verwenden Sie STRG/Command + Klick, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um festzulegen, welche Produkte in diesem Ordner in der App auf verschiedenen Seiten angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht, aber mit einer anderen Produkt-ID versehen wurden. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die nicht mit einem Produkt verknüpft sind. Livefyre priorisiert den Inhalt zunächst mit derselben Produkt-ID, dann mit Inhalten, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann mit Inhalten, die ohne Produkt-IDs in der App veröffentlicht wurden.
