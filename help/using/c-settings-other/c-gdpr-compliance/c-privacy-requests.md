---
description: Erstellen Sie eine Datenschutzanfrage in Livefyre.
title: Eine Datenschutzanforderung erstellen
exl-id: 117e1edb-becd-45f2-bfe5-12fb19ad01e0
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# Erstellen einer Datenschutzanforderung{#create-a-privacy-request}

Erstellen Sie eine Datenschutzanfrage in Livefyre.

Löschen Sie alle Daten für einen Benutzer, erstellen Sie einen Bericht aller Daten für einen Benutzer und nehmen Sie mithilfe dieses Prozesses Änderungen an der Teilnahme oder dem Ausschluss vor.

So suchen und suchen Sie einen Benutzer und erstellen einen Bericht über dessen Inhalt:

1. Gehen Sie zu **[!UICONTROL Settings > Privacy]** und klicken Sie dann auf **[!UICONTROL Create Request]**.

   ![](assets/privacypage1.png)

1. Füllen Sie die Informationen im Fenster **[!UICONTROL Submit Request]** aus:

   * **[!UICONTROL Reference Id]**. Geben Sie einen Bezeichner ein, der für künftige Referenzzwecke verwendet werden soll. Sie können beispielsweise Text, eine Ticketnummer, eine URL, eine E-Mail-Adresse oder eine andere Zeichenfolge mit bis zu 255 Zeichen hinzufügen.
   * **[!UICONTROL Type]**

      * **Zugriff**. Erfasst alle verfügbaren Daten, die mit dem Konto verknüpft sind. Sensible Details, z. B. Kennwörter oder soziale Berechtigungen, werden verschleiert oder weggelassen.

      * **Löschen**. Löscht oder verschleiert alle mit dem Konto verknüpften Daten. **Wenn Sie diese Option wählen und auf &quot;Senden&quot;klicken, können Sie diese Aktion nicht rückgängig machen oder abbrechen  *oder gelöschte Daten wiederherstellen.*** Wenn das Konto einem Livefyre Studio-Benutzer gehört, werden einige Daten beibehalten, um die Integrität Ihrer Geschäftsberichte zu wahren.

         >[!IMPORTANT]
         >
         >Durch das Löschen von Daten für ein Konto werden mit dem Konto verknüpfte Daten dauerhaft gelöscht oder gelöscht. Sie können diese Aktion nicht rückgängig machen und auch keine Daten wiederherstellen, nachdem Sie sie gelöscht haben.

      * **Ausschluss**. Verhindert, dass Livefyre Daten oder Inhalte aus einem sozialen Konto über Streams oder Social Search passiv erfasst. Anmelde- und Ausschluss-Funktion gelten nicht für registrierte Benutzer
      * **Anmelden**. Ermöglicht Livefyre erneut, Daten oder Inhalte von einem Social-Konto passiv zu erfassen, das zuvor über Streams oder Social Search abgemeldet wurde. Anmelde- und Ausschluss-Funktion gelten nicht für registrierte Benutzer

      ![](assets/privacypage2.png)

   * **[!UICONTROL Identifier Type]** und **[!UICONTROL Identifier]**

      * **[!UICONTROL User Account]**

         * Identifiziert ein Konto eines registrierten Benutzers durch die Benutzerkonto-ID, die von Ihrem User Management-System oder der Studio-Benutzerkennung von Livefyre generiert wurde. Sie können die Benutzerkonto-ID auch in den Benutzerdetails unter **Livefyre** **Benutzereinstellungen** oder in den Inhaltsdetails in der **Asset-Bibliothek** oder **App-Inhalt** suchen.

         * Zulässige Werte: Alphanummerische Zeichenfolge mit bis zu 255 Zeichen. Eine E-Mail-Adresse ist keine gültige Eingabe
      * **[!UICONTROL Facebook User]**

         * Identifiziert ein Konto anhand einer numerischen ID, die von Facebook bereitgestellt wird. Der Antragsteller sollte dies angeben. Anweisungen zum Auffinden der numerischen Facebook-ID [finden Sie hier](https://www.facebook.com/help/1397933243846983?helpref=faq_content)
         * Zulässige Werte: 6-16 Zeichen
      * **[!UICONTROL Instagram User]**

         * Identifiziert das Konto anhand einer numerischen ID, die von Instagram bereitgestellt wird. Der Antragsteller sollte dies angeben. Informieren Sie sich online, wie Sie die numerische Instagram-ID auf einem Instagram-Konto finden, indem Sie die entsprechende-ID finden.
         * Zulässige Werte: 5-16 Zeichen
      * **[!UICONTROL Twitter User]**

         * Identifiziert ein Konto anhand einer numerischen ID, die von Twitter bereitgestellt wird. Die Person, die die Änderung des Datenschutzes beantragt, sollte dies bereitstellen. Sie können Anweisungen zur Suche nach der numerischen Twitter-ID für ein Twitter-Konto finden, indem Sie online suchen
         * Zulässige Werte: 5-16 Zeichen
      * **[!UICONTROL YouTube User]**

         * Identifiziert ein Konto anhand einer numerischen ID, die von YouTube bereitgestellt wird. Die Person, die die Änderung des Datenschutzes beantragt, sollte dies bereitstellen. Anweisungen zum Auffinden der numerischen YouTube-ID bei einem YouTube-Konto [finden Sie hier](https://support.google.com/youtube/answer/3250431?hl=en)
         * Zulässige Werte: 5-16 Zeichen
      * **[!UICONTROL Generic Author]**

         * Identifiziert ein Konto durch eine Livefyre Author ID (JID). Verwenden Sie diese Option für Inhalte, die über RSS, Tumblr oder URLs bezogen werden. Um diese ID zu finden, suchen Sie unter **App-Inhalt** oder **Asset-Bibliothek** nach Inhalten, die dem Autor zugeordnet sind, und wählen Sie dann ein Element aus. Die ID ist unter **App-Inhalt** unter **Info** oder in der **Asset-Bibliothek** unter **Autor** im Abschnitt **Details** verfügbar.

         * Zulässige Werte: Alphanummerische Zeichenfolge mit bis zu 255 Zeichen

         ![](assets/privacypage3.png)








1. Klicken **[!UICONTROL Finish]**.

   ![](assets/privacypage4.png)

1. (Nur für Anforderungen löschen) Vergewissern Sie sich, dass alle Informationen für den Benutzer gelöscht werden sollen.

   >[!IMPORTANT]
   >
   >Durch das Löschen von Daten für ein Konto werden mit dem Konto verknüpfte Daten dauerhaft gelöscht oder gelöscht. Sie können diese Aktion nicht rückgängig machen und auch keine Daten wiederherstellen, nachdem Sie sie gelöscht haben.
