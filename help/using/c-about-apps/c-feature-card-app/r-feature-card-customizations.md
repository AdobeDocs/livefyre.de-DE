---
description: Ändern Sie die Größe, Breite und Interaktionsoptionen der Map-App.
seo-description: Ändern Sie die Größe, Breite und Interaktionsoptionen der Map-App.
seo-title: Anpassung von Funktionskarten
solution: Experience Manager
title: Anpassung von Funktionskarten
uuid: dd 43 c 076-027 f -42 c 8-be 2 e -7 d 663 d 4 e 3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# Anpassung von Funktionskarten{#feature-card-customizations}

Ändern Sie die Größe, Breite und Interaktionsoptionen der Map-App.

<!-- 
r_feature_card_customization.dita
 -->

Feature Card-Apps enthalten nur standardanpassungen: ** [!UICONTROL Theme]**, Markenfarbe, Schriftfamilie und Schriftgröße.

Sie können Feature Cards mithilfe von:

* **[!UICONTROL Style]** und **[!UICONTROL Config]** Optionen für alle Apps im **[!UICONTROL App Designer]**. Weitere Informationen zum Standard **[!UICONTROL Style]** und den **[!UICONTROL Config]** Optionen für alle Apps im **[!UICONTROL App Designer]** Abschnitt finden Sie unter Anpassen von Apps.

* Integrationswerkzeuge. Weitere Informationen zum Anpassen von Apps mit Integrationswerkzeugen finden Sie unter App-Integrationen.
* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Umschalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.
   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, damit der Inhaltsinhaber die Rechte für den Inhalt erteilt hat, bevor eine Aktionsaktionsschaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Berechtigungen für den Inhalt erteilt wurden. Die Schaltfläche &quot;Aktionsaufruf&quot; wird jedoch nur mit dem Inhalt angezeigt, wenn die Rechte für den Inhalt nicht gewährt werden.

   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile oberhalb der Aktionsaufruf-Schaltfläche im Inhalt angezeigt werden sollen. Standardtext lautet: &quot;Shop diese Produkte: &quot;.
   * **[!UICONTROL Call-to-action button text]** Passen Sie den Text auf der Aktionsaktionsschaltfläche an. Standardtext ist &quot;Jetzt kaufen&quot; .
   * **[!UICONTROL Product display options]** Wählen Sie aus, ob Sie die **[!UICONTROL Photo]** Schaltfläche &quot;Aktionsaufruf **[!UICONTROL Product name]** «und&quot; Aktionsaufruf&quot; anzeigen möchten.
   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.
   * **[!UICONTROL Referral tracking key-value pairs]** Fügen Sie Parameter hinzu, um die Verweisverfolgung aus Ihrem App-Inhalt auf die zugehörige Produktseite zu setzen.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC auf die App für jede Produktseite. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Verwenden `CTRL/Command + click` Sie diese Option, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um zu bestimmen, welche Produkte in diesem Ordner auf verschiedenen Seiten in der App angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht wurden, aber mit einer anderen Produkt-ID getaggt sind. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die keinem Produkt zugeordnet sind. Livefyre priorisiert zuerst den Inhalt mit derselben Produkt-ID, dann Inhalte, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann Inhalte, die in der App ohne Produkt-IDs veröffentlicht wurden.

