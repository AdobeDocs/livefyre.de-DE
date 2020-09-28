---
description: Ändern Sie Größe, Breite und Interaktionsoptionen der Media Wall-App.
seo-description: Ändern Sie Größe, Breite und Interaktionsoptionen der Media Wall-App.
seo-title: Anpassung der Medienmauer
solution: Experience Manager
title: Anpassung der Medienmauer
uuid: 79aecd92-3937-4bb4-a1a6-b090fb39afb0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Anpassung der Medienmauer{#media-wall-customizations}

Ändern Sie Größe, Breite und Interaktionsoptionen der Media Wall-App.



Media Walls streamen Live-Bilder und andere Inhalte in eine Echtzeit-Social-Wand, um alle Aktivitäten rund um ein Ereignis zu visualisieren.

Wenn diese Option aktiviert ist, können Benutzer Text, Bilder oder Videos direkt in diese App posten. Zu den unterstützten Dateitypen zählen:

* Bild: JPEG, GIF, PNG
* Video: Quicktime/MOV, MP4, MPEG, WebM
* Audio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Legt die anfängliche Anzahl der angezeigten Inhaltselemente fest.

* **[!UICONTROL Load content with animation.]** Schalten Sie diese Option ein, um die Media Pinnwand auf einer Seite mit Animation zu laden. Schalten Sie diese Option aus, um die Medienwall auf eine Seite ohne Animation zu laden.
* **[!UICONTROL Number of columns.]** Legen Sie die Anzahl der Spalten für die Medienwall fest. Die Anzahl der Spalten bleibt gleich, unabhängig von der Größe des Fensters oder Browsers. Wenn Sie "Auto"auswählen, wird die Anzahl der Spalten angepasst, um eine optimierte Anzahl von Spalten für die Bildschirmgröße anzuzeigen.
* **[!UICONTROL Fit content to width]**. Wenn diese Option deaktiviert ist, wird der Inhalt auf ein Quadrat zugeschnitten. Schalten Sie diese Option ein, um ein ganzes Bild auf der Karte anzuzeigen, unabhängig davon, ob die gesamte Karte gefüllt ist oder nicht.
* **[!UICONTROL Include content modal]**

   Ermöglicht Benutzern, auf ein Foto im Stream zu klicken, um es in einem überlagerten Popup-Fenster zu öffnen.

* **[!UICONTROL Require rights]**. Aktivieren Sie diese Option, um nur Inhalte mit dem Berechtigungsanforderungsstatus "Genehmigt"anzuzeigen.
* **[!UICONTROL Hide social branding when rights granted]** Schalten Sie dies ein, um das Logo für das ursprüngliche Social Media-Netzwerk (Twitter oder Instagram) zu entfernen, wenn Rechte für ein Inhaltselement gewährt werden.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Wählen Sie aus, ob Benutzer mit der Schaltfläche "Hochladen"Text, Fotos oder Videos veröffentlichen dürfen.
   * **[!UICONTROL Require Media]**. Schalten Sie ein/aus, damit Benutzer nur Foto- oder Videoinhalte mit der Schaltfläche "Hochladen"hochladen müssen.
   * Sie können den Standardtext für die folgenden Felder der Schaltfläche "Schaltfläche hochladen"bearbeiten:

      * **[!UICONTROL Upload Button Text]**. Text für die Schaltfläche "Hochladen". Der Standardtext lautet "Was ist im Kopf?"
      * **[!UICONTROL Comment Modal Title]**. Der Titel für die modale Site, die Besucher zum Posten von Inhalten verwenden. Der Standardtext lautet "Kommentar posten".
      * **[!UICONTROL Comment Modal Button]**. Der Text der Schaltfläche, auf die Besucher der Site klicken, um Inhalte zu posten. Der Standardtext lautet "Kommentar posten".

* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten, um weitere Maßnahmen zu ergreifen.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Schalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.
   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, um sicherzustellen, dass der Eigentümer des Inhalts Rechte für den Inhalt erteilt hat, bevor eine Aktionsaufruf-Schaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Rechte für den Inhalt gewährt wurden. Die Schaltfläche "Aktionsaufruf"wird jedoch nur dann mit dem Inhalt angezeigt, wenn die Rechte für den Inhalt erteilt wurden.

   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile über der Aktionsaufruf-Schaltfläche im Inhaltsmodell angezeigt werden sollen. Die Standardformulierung lautet "Diese Produkte kaufen:".
   * **[!UICONTROL Call-to-action button text]** Die Wörter, die im Inhalts-Modal in der Schaltfläche Aktionsaufruf angezeigt werden sollen. Der Standardtext lautet "Jetzt kaufen:".
   * **[!UICONTROL Product display options]** Wählen Sie aus, ob das Foto und der Produktname mit der Schaltfläche Aktionsaufruf angezeigt werden sollen.

      >[!NOTE]
      >
      >Sowohl die Schaltflächen "Foto"als auch "Produktname"markieren Blau, wenn sie aktiviert sind.

   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.
   * **[!UICONTROL Referral tracking key-value pairs]** Fügen Sie Parameter hinzu, um die Verweisverfolgung von Ihrem App-Inhalt zur entsprechenden Produktseite weiter anzugeben.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC für jede Produktseite in die App. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner auf der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Verwenden Sie STRG/Command + Klick, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um festzulegen, welche Produkte in diesem Ordner in der App auf verschiedenen Seiten angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht, aber mit einer anderen Produkt-ID versehen wurden. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die mit keinem Produkt verknüpft sind. Livefyre priorisiert den Inhalt zunächst mit derselben Produkt-ID, dann mit Inhalten, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann mit Inhalten, die ohne Produkt-IDs in der App veröffentlicht wurden.

Sie können Media Wall wie folgt anpassen:

* **[!UICONTROL Style]** und **[!UICONTROL Config]** Optionen für alle Apps im **[!UICONTROL App Designer]**. Weitere Informationen zu den Standard- **[!UICONTROL Style]** und **[!UICONTROL Config]** -Optionen für alle Apps im Abschnitt Anpassen von Apps finden Sie unter **[!UICONTROL App Designer]**.

* Integrationstools. Weitere Informationen zum Anpassen einer Medienwall mithilfe von Integrationstools finden Sie unter [Media Wall-Integration](/help/implementation/c-app-integrations/c-media-wall-integration.md) .

