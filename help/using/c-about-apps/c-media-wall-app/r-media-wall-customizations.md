---
description: Ändern Sie die Größe, Breite und Interaktionsoptionen der Medienwall-App.
seo-description: Ändern Sie die Größe, Breite und Interaktionsoptionen der Medienwall-App.
seo-title: Medienpinnwandanpassungen
solution: Experience Manager
title: Medienpinnwandanpassungen
uuid: 79 aecd 92-3937-4 bb 4-a 1 a 6-b 900 fb 39 afb 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Medienpinnwandanpassungen{#media-wall-customizations}

Ändern Sie die Größe, Breite und Interaktionsoptionen der Medienwall-App.



Medienwände streamen Live-Bilder und andere Inhalte in eine Echtzeit-Social-Wand, wodurch alle Aktivitäten um ein Ereignis visualisiert werden.

Wenn diese Option aktiviert ist, können Benutzer Text, Bilder oder Videos direkt zu dieser App veröffentlichen. Zu den unterstützten Dateitypen gehören:

* Bild: JPEG, GIF, PNG
* Video: Quicktime/MOV, MP 4, MPEG, webm
* Audio: WAV, WAVE, X-MS-WMA, FLAC, OGG, MPEG

* **[!UICONTROL Items to load]**

   Legt die Anfangsanzahl der angezeigten Inhaltselemente fest.

* **[!UICONTROL Load content with animation.]** Aktivieren Sie diese Option, um die Medienpinnwand auf einer Seite mit Animation zu laden. Deaktivieren Sie diese Option, um die Medienpinnwand auf einer Seite ohne Animation zu laden.
* **[!UICONTROL Number of columns.]** Legen Sie die Anzahl der Spalten für die Medienpinnwand fest. Die Anzahl der Spalten bleibt unabhängig von der Größe des Fensters oder Browsers gleich. Wenn Sie "Auto" auswählen, wird die Anzahl der Spalten angepasst, um eine optimierte Spaltenanzahl für die Bildschirmgröße anzuzeigen.
* **[!UICONTROL Fit content to width]**. Wenn diese Option deaktiviert ist, wird der Inhalt auf einem Quadrat abgeschnitten. Aktivieren Sie diese Option, um ein ganzes Bild in der Karte anzuzeigen, unabhängig davon, ob es sich um die gesamte Karte handelt oder nicht.
* **[!UICONTROL Include content modal]**

   Ermöglicht es Benutzern, auf ein Foto im Stream zu klicken, um es in einem überlagerten Popup-Fenster zu öffnen.

* **[!UICONTROL Require rights]**. Aktivieren Sie diese Option, um nur Inhalte mit einem Berechtigungsanforderungsstatus "Gewährt" anzuzeigen.
* **[!UICONTROL Hide social branding when rights granted]** Schalten Sie dies ein, um das Logo für das Social-Media-Netzwerk (Twitter oder Instagram) zu entfernen, wenn die Rechte für ein Inhaltselement gewährt werden.

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. Legen Sie fest, ob Benutzer Text, Foto oder Video mit der Schaltfläche "Hochladen" veröffentlichen können.
   * **[!UICONTROL Require Media]**. Schalten Sie ein, damit Benutzer über die Schaltfläche "Hochladen" nur Foto- oder Videoinhalte hochladen müssen.
   * Sie können den Standardtext für die folgenden Felder zum Hochladen bearbeiten:

      * **[!UICONTROL Upload Button Text]**. Text für die Schaltfläche "Hochladen" . Der Standardtext lautet "Was ist Ihre Meinung? «
      * **[!UICONTROL Comment Modal Title]**. Der Titel der modalen Site-Besucher zum Posten von Inhalten. Der Standardtext lautet "Beitrag posten" .
      * **[!UICONTROL Comment Modal Button]**. Der Text der Schaltflächenbesucher klickt, um Inhalte zu posten. Der Standardtext lautet "Beitrag posten" .

* **[!UICONTROL Call-to-action button]** Sie können die Aktionsaufruf-Schaltfläche mit einem Produktkatalog verwenden, um Benutzer zu einem Produkt oder zu Ihrer Site zu leiten.

   * **[!UICONTROL Call-to-action button]** Schalten Sie den Umschalter ein, um die Aktionsaufruf-Schaltfläche anzuzeigen.
   * **[!UICONTROL Require rights to display products]** Schalten Sie den Umschalter ein, damit der Inhaltsinhaber die Rechte für den Inhalt erteilt hat, bevor eine Aktionsaktionsschaltfläche für den Inhalt angezeigt wird.

      >[!NOTE]
      >
      >Der Inhalt wird auch dann angezeigt, wenn keine Berechtigungen für den Inhalt erteilt wurden. Die Schaltfläche "Aktionsaufruf" wird jedoch nur mit dem Inhalt angezeigt, wenn die Rechte für den Inhalt nicht gewährt werden.

   * **[!UICONTROL Call-to-action header text]** Die Wörter, die in der Kopfzeile oberhalb der Aktionsaufruf-Schaltfläche im Inhalt angezeigt werden sollen. Standardtext lautet: "Shop diese Produkte: ".
   * **[!UICONTROL Call-to-action button text]** Die Wörter, die in der Aktionsaufrufschaltfläche im Inhalt angezeigt werden sollen. Standardtext lautet: "Jetzt kaufen: ".
   * **[!UICONTROL Product display options]** Wählen Sie aus, ob Sie den Foto- und Produktnamen mit der Aktionsaktionsschaltfläche anzeigen möchten.

      >[!NOTE]
      >
      >Die Schaltflächen "Foto" und" Produktname" markieren blau, wenn sie aktiviert sind.

   * **[!UICONTROL Product URL referral tracking]** Schalten Sie den Umschalter ein, um Verweise von dieser App auf die zugehörige Produktseite zu verfolgen.
   * **[!UICONTROL Referral tracking key-value pairs]** Fügen Sie Parameter hinzu, um die Verweisverfolgung aus Ihrem App-Inhalt auf die zugehörige Produktseite zu setzen.

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. Wählen Sie diese Option, um eine App für mehrere Produktseiten zu erstellen. Filtern Sie produktspezifische UGC auf die App für jede Produktseite. Sie können einen oder mehrere Ordner auswählen, um bestimmte Sammlungen der App zuzuordnen.
   * **[!UICONTROL Select Product folders]**. Wählen Sie die Produktordner der obersten Ebene aus, die zum Filtern von UGC verwendet werden sollen. Wählen Sie Strg/Befehl + Klicken, um mehr als einen Ordner auszuwählen. Livefyre verwendet den Ordner, um zu bestimmen, welche Produkte in diesem Ordner auf verschiedenen Seiten in der App angezeigt werden sollen.
   * **[!UICONTROL Show related content]**. Schalten Sie dies ein, um Inhalte anzuzeigen, die in der App veröffentlicht wurden, aber mit einer anderen Produkt-ID getaggt sind. Nachdem der produktspezifische Inhalt für die App angezeigt wurde, zeigt Livefyre Inhalte für andere Produkte und Inhalte an, die keinem Produkt zugeordnet sind. Livefyre priorisiert zuerst den Inhalt mit derselben Produkt-ID, dann Inhalte, die mit anderen Produkt-IDs in der App veröffentlicht wurden, und dann Inhalte, die in der App ohne Produkt-IDs veröffentlicht wurden.

Sie können Medienpinnwände mithilfe von:

* **[!UICONTROL Style]** und **[!UICONTROL Config]** Optionen für alle Apps im **[!UICONTROL App Designer]**. Weitere Informationen zum Standard **[!UICONTROL Style]** und den **[!UICONTROL Config]** Optionen für alle Apps im **[!UICONTROL App Designer]**Abschnitt finden Sie unter Anpassen von Apps.

* Integrationswerkzeuge. Weitere Informationen zum Anpassen einer Medienpinnwand mithilfe von Integrationstools finden Sie unter [Media Wall Integration](/help/implementation/c-app-integrations/c-media-wall-integration.md) .

