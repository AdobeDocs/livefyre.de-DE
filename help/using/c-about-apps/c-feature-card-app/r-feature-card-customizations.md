---
description: Ändern Sie Größe, Breite und Interaktionsoptionen der Map-App.
title: Anpassung der Funktionskarten
exl-id: b907885a-211d-4628-9955-5f1a5ec577cf
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Anpassung der Funktionskarten{#feature-card-customizations}

Ändern Sie Größe, Breite und Interaktionsoptionen der Map-App.

<!-- 
r_feature_card_customization.dita
 -->

Funktionskarten-Apps enthalten nur Standardanpassungen:** [!UICONTROL Theme]**, Markenfarbe, Schriftfamilie und Schriftgröße.

Sie können Funktionskarten mit folgenden Funktionen anpassen:

* **[!UICONTROL Style]** und  **[!UICONTROL Config]** Optionen für alle Apps im  **[!UICONTROL App Designer]**. Weitere Informationen zu den Standardoptionen **[!UICONTROL Style]** und **[!UICONTROL Config]** für alle Apps in **[!UICONTROL App Designer]** finden Sie unter Anpassen von Apps.

* Integrationstools. Weitere Informationen zum Anpassen von Apps mit Integrationstools finden Sie unter App-Integrationen.
* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten, um weitere Maßnahmen zu ergreifen.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Schalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.
   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, um sicherzustellen, dass der Eigentümer des Inhalts Rechte für den Inhalt erteilt hat, bevor eine Aktionsaufruf-Schaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Rechte für den Inhalt gewährt wurden. Die Schaltfläche &quot;Aktionsaufruf&quot;wird jedoch nur dann mit dem Inhalt angezeigt, wenn die Rechte für den Inhalt erteilt wurden.

   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile über der Aktionsaufruf-Schaltfläche im Inhaltsmodell angezeigt werden sollen. Die Standardformulierung lautet &quot;Diese Produkte kaufen:&quot;.
   * **[!UICONTROL Call-to-action button text]** Passen Sie den Text auf der Schaltfläche Aktionsaufruf an. Der Standardtext lautet &quot;Jetzt kaufen&quot;.
   * **[!UICONTROL Product display options]** Legen Sie fest, ob die Schaltfläche  **[!UICONTROL Photo]** und die Schaltfläche  **[!UICONTROL Product name]** mit der Aktionsaufruf angezeigt werden sollen.
   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.
   * **[!UICONTROL Referral tracking key-value pairs]** hinzufügen Parameter, um die Verweisverfolgung von Ihrem App-Inhalt auf die zugehörige Produktseite weiter anzugeben.

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC für jede Produktseite in die App. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner auf der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Verwenden Sie `CTRL/Command + click`, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um festzulegen, welche Produkte in diesem Ordner in der App auf verschiedenen Seiten angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht, aber mit einer anderen Produkt-ID versehen wurden. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die nicht mit einem Produkt verknüpft sind. Livefyre priorisiert den Inhalt zunächst mit derselben Produkt-ID, dann mit Inhalten, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann mit Inhalten, die ohne Produkt-IDs in der App veröffentlicht wurden.
