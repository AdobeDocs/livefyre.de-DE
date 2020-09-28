---
description: Ändern Sie Größe, Breite und Interaktionsoptionen der Map-App.
seo-description: Ändern Sie Größe, Breite und Interaktionsoptionen der Map-App.
seo-title: Anpassung der Funktionskarten
solution: Experience Manager
title: Anpassung der Funktionskarten
uuid: dd43c076-027f-42c8-be2e-7d863d4e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# Anpassung der Funktionskarten{#feature-card-customizations}

Ändern Sie Größe, Breite und Interaktionsoptionen der Map-App.

<!-- 
r_feature_card_customization.dita
 -->

Funktionskarten-Apps umfassen nur Standardanpassungen:** [!UICONTROL Theme]**, Markenfarbe, Schriftfamilie und Schriftgröße.

Sie können Funktionskarten mit folgenden Funktionen anpassen:

* **[!UICONTROL Style]** und **[!UICONTROL Config]** Optionen für alle Apps im **[!UICONTROL App Designer]**. Weitere Informationen zu den Standard- **[!UICONTROL Style]** und **[!UICONTROL Config]** -Optionen für alle Apps im Abschnitt Anpassen von Apps finden Sie unter **[!UICONTROL App Designer]**.

* Integrationstools. Weitere Informationen zum Anpassen von Apps mit Integrationstools finden Sie unter App-Integrationen.
* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten, um weitere Maßnahmen zu ergreifen.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Schalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.
   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, um sicherzustellen, dass der Eigentümer des Inhalts Rechte für den Inhalt erteilt hat, bevor eine Aktionsaufruf-Schaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Rechte für den Inhalt gewährt wurden. Die Schaltfläche "Aktionsaufruf"wird jedoch nur dann mit dem Inhalt angezeigt, wenn die Rechte für den Inhalt erteilt wurden.

   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile über der Aktionsaufruf-Schaltfläche im Inhaltsmodell angezeigt werden sollen. Die Standardformulierung lautet "Diese Produkte kaufen:".
   * **[!UICONTROL Call-to-action button text]** Passen Sie den Text auf der Schaltfläche Aktionsaufruf an. Der Standardtext lautet "Jetzt kaufen".
   * **[!UICONTROL Product display options]** Wählen Sie aus, ob Sie die Schaltfläche **[!UICONTROL Photo]** und die **[!UICONTROL Product name]** mit der Aktionsaufruf-Schaltfläche anzeigen möchten.
   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.
   * **[!UICONTROL Referral tracking key-value pairs]** Fügen Sie Parameter hinzu, um die Verweisverfolgung von Ihrem App-Inhalt zur entsprechenden Produktseite weiter anzugeben.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC für jede Produktseite in die App. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner auf der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Verwenden Sie `CTRL/Command + click` zur Auswahl mehrerer Ordner. Livefyre verwendet den Ordner, um festzulegen, welche Produkte in diesem Ordner in der App auf verschiedenen Seiten angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht, aber mit einer anderen Produkt-ID versehen wurden. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die mit keinem Produkt verknüpft sind. Livefyre priorisiert den Inhalt zunächst mit derselben Produkt-ID, dann mit Inhalten, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann mit Inhalten, die ohne Produkt-IDs in der App veröffentlicht wurden.

