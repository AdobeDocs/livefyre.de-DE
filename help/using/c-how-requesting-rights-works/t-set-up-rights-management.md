---
description: Legen Sie die Einstellungen für das Anfordern von Rechten für Instagram- und Twitter-Beiträge fest.
seo-description: Legen Sie die Einstellungen für das Anfordern von Rechten für Instagram- und Twitter-Beiträge fest.
seo-title: Rights Management einrichten
solution: Experience Manager
title: Rights Management einrichten
uuid: 3ffcbc95-484f-4eba-b817-658c1d658bf8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Rights Management einrichten{#set-up-rights-management}

Legen Sie die Einstellungen für das Anfordern von Rechten für Instagram- und Twitter-Beiträge fest.

Bevor Sie die Einstellungen für Rights Request definieren können, müssen Sie ein oder mehrere Social-Konten für Instagram oder Twitter konfigurieren. Weitere Informationen zum Konfigurieren eines Social-Kontos finden Sie unter Social-Konto [hinzufügen](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Sie können die Rechteverwaltung nur auf Netzwerkebene konfigurieren. Sie können die Verwaltung der Site-spezifischen Rechte nicht konfigurieren.

1. Navigieren Sie in Livefyre Studio zu **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**.

   >[!NOTE]
   >
   >Sie benötigen Berechtigungen auf Moderator- oder Administrator-Netzwerkebene, um Rights Management-Konten einzurichten.

1. Wählen Sie diese Option, **[!UICONTROL +Add New Account]** wenn keine Rights Management-Konten eingerichtet wurden.
1. Klicken Sie **[!UICONTROL Create New Setting]** unter dem sozialen Netzwerk, das Sie für Rights Management verwenden möchten.

   >[!NOTE]
   >
   >Bei Instagram-Konten müssen Sie über ein Instagram-Geschäftskonto verfügen, um Rechte mit Teilautomatisierung anzufordern. Weitere Informationen zu den verschiedenen Instagram-Konten und deren Verwendung finden Sie unter [Info zu Instagram-Konten](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

1. Füllen Sie die angezeigten Felder aus. Alle Felder müssen ausgefüllt werden.

   * **[!UICONTROL Display name:]** Geben Sie einen Anzeigenamen ein, um das Twitter- oder Instagram-Konto für Ihr Rights Request-Konto zu identifizieren. Dieser Name ist nur intern.
   * **[!UICONTROL Enabled:]**Standardmäßig auf "on"setzen. Aktiviert die Rights Management für das Konto.
   * **[!UICONTROL Approval hashtag:]** Das Hashtag, mit dem der Inhaltseigentümer angibt, dass er der Nutzung seines Inhalts zustimmt.
   * **[!UICONTROL Terms and conditions:]** Ein Link zu den Nutzungsbedingungen Ihres Netzwerks für die Wiederverwendung von Inhalten. Bei diesem Feld ist die Groß-/Kleinschreibung zu beachten.
   * **[!UICONTROL Network and sites:]** Das Netzwerk oder die Site, für das bzw. die dieses Konto Wiederverwendungsrechte für Inhalte anfordern kann. Um dieses Konto für das gesamte Netzwerk verfügbar zu machen, wählen Sie das erste Element in der Liste aus oder beschränken Sie mithilfe des Befehls-/STRG-Schlüssels auf bestimmte Websites.
   * **[!UICONTROL Default message:]** Eine Meldung, die zusammen mit Ihrer Rights Request angezeigt wird. Sie können diese Meldung überschreiben, wenn Sie Rechte anfordern.

      * Livefyre zeigt eine der Standardmeldungen an Moderatoren, wenn ein Moderator eine Anforderung an einen Inhaltsersteller sendet. Moderatoren können vor dem Senden eine weitere Standardnachricht erstellen oder die Nachricht bearbeiten. Die Nachrichten müssen den Twitter- oder Instagram-Handle des Autors ({handle}), Ihr Genehmigungs-Hashtag ({grantTag}) und einen Link zu Ihren Geschäftsbedingungen ({termsLink}) enthalten.

         **[!UICONTROL Note:]** Bei {handle}, {grantTag} und {termsLink} wird die Groß-/Kleinschreibung beachtet.

         **[!UICONTROL Note:]** Um eine böswillige Verwendung zu verhindern, umschließt Twitter alle enthaltenen URLs mit [t.co](https://t.co/) -Formatierung. Damit Ihre Standardnachricht nicht länger als 140 Zeichen ist, empfiehlt Livefyre, keine URLs in die Standardnachricht aufzunehmen.

      * Empfohlene Vorgehensweisen zum Schreiben von Rechten fordern Meldungen an:

         * Erstellen Sie mehrere Standardmeldungen, damit Sie nicht wie ein Roboter klingen. Speichern Sie alle Standardmeldungen, bevor Sie die nächste Standardnachricht erstellen.
         * Ermutigen Sie Ihre Moderatoren, diese Notiz zu personalisieren, bevor Sie sie senden, damit die Anfragen Ihres Netzwerks nicht mit Spam getaggt werden.

1. Klicken Sie auf **[!UICONTROL Save Settings]** , um Ihr Rights Request-Konto hinzuzufügen.
Senden Sie eine Berechtigungsanfrage aus der Asset-Bibliothek. Weitere Informationen zum Senden einer Berechtigungsanfrage aus der Asset-Bibliothek finden Sie unter [Eine Berechtigungsanfrage](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) senden.