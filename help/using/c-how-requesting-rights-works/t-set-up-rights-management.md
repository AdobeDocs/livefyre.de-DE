---
description: Legen Sie die Einstellungen für das Anfordern von Rechten für Instagram- und Twitter-Beiträge fest.
seo-description: Legen Sie die Einstellungen für das Anfordern von Rechten für Instagram- und Twitter-Beiträge fest.
seo-title: Rights Management einrichten
solution: Experience Manager
title: Rights Management einrichten
uuid: 3 ffcbc 95-484 f -4 eba-b 817-658 c 1 d 658 bf 8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Rights Management einrichten{#set-up-rights-management}

Legen Sie die Einstellungen für das Anfordern von Rechten für Instagram- und Twitter-Beiträge fest.

Bevor Sie Rights Request Settings definieren können, müssen Sie ein oder mehrere Social-Konten für Instagram oder Twitter konfigurieren. Weitere Informationen zum Konfigurieren eines Social-Kontos finden Sie unter [Social-Konto hinzufügen](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram).

>[!NOTE]
>
>Sie können Rights Management nur auf Netzwerkebene konfigurieren. Sie können die Site-spezifische Rechteverwaltung nicht konfigurieren.

1. Navigieren Sie in Livefyre Studio zu **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**.

   >[!NOTE]
   >
   >Zum Einrichten von Rights Management-Konten benötigen Sie Berechtigungen für Moderatoren oder Administratoren.

1. Wählen **[!UICONTROL +Add New Account]** Sie diese Option aus, wenn Sie keine Rights Management-Konten eingerichtet haben.
1. Klicken **[!UICONTROL Create New Setting]** Sie im sozialen Netzwerk, das Sie für Rights Management verwenden möchten.

   >[!NOTE]
   >
   >Für Instagram-Konten müssen Sie über ein Instagram-Geschäftskonto verfügen, um Rechte mit partieller Automatisierung anzufordern. Weitere Informationen zu den verschiedenen Arten von Instagram-Konten und deren Verwendung finden Sie unter [Instagram-Konten](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts).

1. Füllen Sie die angezeigten Felder aus. Alle Felder sind erforderlich.

   * **[!UICONTROL Display name:]** Geben Sie einen Anzeigenamen ein, um das Twitter- oder Instagram-Konto zu identifizieren, das für Ihr Rights Request-Konto verwendet werden soll. Dieser Name ist nur intern.
   * ****[!UICONTROL Enabled:]Standardmäßig aktiviert. Aktiviert Rights Management für das Konto.
   * **[!UICONTROL Approval hashtag:]** Das Hashtag, mit dem der Eigentümer des Inhalts anzeigt, dass er die Verwendung ihres Inhalts akzeptiert.
   * **[!UICONTROL Terms and conditions:]** Ein Link zu den Geschäftsbedingungen Ihres Netzwerks für die Wiederverwendung von Inhalten. Bei diesem Feld wird zwischen Groß- und Kleinschreibung unterschieden.
   * **[!UICONTROL Network and sites:]** Das Netzwerk oder die Site, für die dieses Konto die Wiederverwendungsrechte für Inhalte anfordern kann. Um dieses Konto für das gesamte Netzwerk verfügbar zu machen, wählen Sie das erste Element in der Liste aus oder beschränken Sie auf bestimmte Sites mit dem Befehl Befehl/STRG.
   * **[!UICONTROL Default message:]** Eine Meldung, die mit Ihrer Rights Request angezeigt wird. Sie können diese Meldung überschreiben, wenn Sie Rechte anfordern.

      * Livefyre stellt eine der Standardmeldungen für Moderatoren dar, wenn ein Moderator eine Anforderung an einen Inhaltsautor sendet. Moderatoren können eine weitere Standardnachricht erstellen oder die Nachricht vor dem Senden bearbeiten. Nachrichten müssen den Twitter- oder Instagram-Handle des Autors ({handle}), Ihr Genehmigungshashtag ({granttag}) und einen Link zu Ihren Geschäftsbedingungen ({termslink}) enthalten.

         **[!UICONTROL Note:]** Bei {handle}, {granttag} und {termslink} wird zwischen Groß- und Kleinschreibung unterschieden.

         **[!UICONTROL Note:]** Um böswillige Verwendung zu verhindern, bricht Twitter alle enthaltenen urls mit [t. co](https://t.co/) -Formatierung ein. Um zu verhindern, dass Ihre Standardnachricht 140 Zeichen überschreitet, empfiehlt Livefyre, urls in Ihrer Standardnachricht einzubinden.

      * Bewährte Verfahren zum Schreiben von Rechtschreibanforderungsmeldungen:

         * Erstellen Sie mehrere Standardmeldungen, damit Sie nicht wie ein Robot klingen. Speichern Sie die Standardnachricht vor der Erstellung der nächsten Standardnachricht.
         * Empfehlen Sie Ihren Moderatoren, diese Notiz vor dem Senden zu personalisieren, um zu verhindern, dass die Anforderungen Ihres Netzwerks Spam mit Tags versehen.

1. Klicken **[!UICONTROL Save Settings]** Sie auf, um Ihr Rights Request-Konto hinzuzufügen.
Senden Sie eine Rechteanforderung aus der Asset-Bibliothek. Weitere Informationen zum Senden einer Rechteanforderung aus der Asset-Bibliothek finden Sie unter [Rights Request](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) senden.