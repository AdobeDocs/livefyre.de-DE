---
description: Um eine Social-Anmeldung zu aktivieren, verwenden Sie Studio, um Ihrer Livefyre-Integration die Anmeldedaten Ihrer Social-Apps hinzuzufügen, und passen Sie das Anmeldemodul an.
title: Verwenden von Studio zum Verbinden Ihrer Social-Apps mit Ihrer Livefyre-Implementierung
exl-id: 2ccb9737-8c59-4c1d-93d3-61f913b3cdd6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 1%

---

# Verwenden von Studio zum Verbinden Ihrer Social-Apps mit Ihrer Livefyre-Implementierung{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

Um eine Social-Anmeldung zu aktivieren, verwenden Sie Studio, um Ihrer Livefyre-Integration die Anmeldedaten Ihrer Social-Apps hinzuzufügen, und passen Sie das Anmeldemodul an.

## Anpassen des Anmeldemodells {#section_v4c_hv2_3z}

Mit dem Anmeldemodell können Sie die Informationen anpassen, die Ihre Benutzer bei der Anmeldung bei Ihren Apps sehen. Sie können das modale Fenster anpassen.

* **Logo:** Laden Sie ein Logo hoch, das Sie in Ihren Anmeldemodellen verwenden können.
* **Schriftfamilie:** Wählen Sie eine Schriftart aus, die Ihrem Branding entspricht.
* **Markenfarbe:** Geben Sie eine hexadezimale Farbe für den spezifischen Text im Modal ein.
* **Geschäftsbedingungen-URL:** Geben Sie die URL für die Seite &quot;Geschäftsbedingungen&quot;Ihrer Firma ein. Dieses Feld ist für die Verwendung mit Livefyre Identity erforderlich.

## Übersetzen der Livefyre-Identität {#section_xxt_z52_3z}

Sie können Übersetzungssätze für Textzeichenfolgen in Livefyre Identity erstellen und ändern.

Weitere Informationen zur Verwendung von Übersetzungssätzen mit Livefyre Identity finden Sie unter Übersetzungssätze.

Weitere Informationen zu den spezifischen Zeichenfolgen, die Sie für Livefyre Identity anpassen können, finden Sie unter Livefyre Identity.

## Aktivieren Sie die Anmeldung mit E-Mail {#section_dlv_wzt_bbb}

Erlauben Sie Benutzern, sich mit ihren E-Mail-Adressen anzumelden und mit Apps auf Ihrer Site zu interagieren.

So aktivieren Sie die Anmeldung mit einem nativen Livefyre-Konto:

1. Navigieren Sie in Livefyre Studio zu **[!UICONTROL Integration Settings]**.
1. Schalten Sie den Umschalter **[!UICONTROL Enable Login with Email]** in **[!UICONTROL On]** um.

## Aktivieren Sie die Anmeldung mit einem Facebook-Konto {#section_ph3_515_bbb}

Schließen Sie Ihr Facebook-Konto an Livefyre an, damit Benutzer ihre Facebook-Anmeldungen zur Interaktion mit Apps auf Ihrer Site verwenden können.

So aktivieren Sie die Anmeldung über ein Facebook-Konto:

1. Schalten Sie den Umschalter **[!UICONTROL Enable Login with Facebook]** in **[!UICONTROL ON]** um.

1. hinzufügen Sie **[!UICONTROL App ID]** und **[!UICONTROL App Secret]** Ihrer Facebook-App.

   Diese Werte sind im Facebook Developers Dashboard für die App aufgeführt, verfügbar unter [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/).

## Anmeldung mit Google aktivieren {#section_fq3_kb5_bbb}

Verbinden Sie Ihr Google+-Konto mit Livefyre, damit Benutzer ihre Google+-Anmeldungen zur Interaktion mit Apps auf Ihrer Site verwenden können.

So aktivieren Sie die Anmeldung über ein Google+-Konto:

1. Schalten Sie den Umschalter **[!UICONTROL Enable Login with Google]** in **[!UICONTROL ON]** um.

1. hinzufügen Sie **[!UICONTROL Client ID]** und **[!UICONTROL Client secret]** Ihrer Google-App.

   Diese Werte werden in Ihrer Benutzeroberfläche des Google Cloud-Plattform-Projekts aufgelistet, die unter [https://console.cloud.google.com/](https://console.cloud.google.com/apis/library) verfügbar ist. Um diese Informationen abzurufen, gehen Sie zu **[!UICONTROL API Manager > Credentials]** und klicken Sie auf den Projektnamen.

## Aktivieren einer Anmeldung mit einem Twitter-Konto {#section_iyz_wb5_bbb}

Schließen Sie Ihr Twitter-Konto an Livefyre an, damit Benutzer ihre Twitter-Anmeldungen zur Interaktion mit Apps auf Ihrer Site verwenden können.

So aktivieren Sie die Anmeldung über ein Twitter-Konto:

1. Schalten Sie den Umschalter **[!UICONTROL Enable Login with Twitter]** in **[!UICONTROL ON]** um.

1. hinzufügen Sie **[!UICONTROL Consumer Key (API Key)]** und **[!UICONTROL Consumer Secret (API Secret)]** Ihrer Twitter-App.

   Diese Werte sind auf der Seite **[!UICONTROL Keys and Access Tokens]** Ihrer Twitter-App aufgeführt, die unter [https://apps.twitter.com/](https://apps.twitter.com/) verfügbar ist.

## Aktivieren Sie die Anmeldung mit einem Yahoo! Konto {#section_s1q_3c5_bbb}

Schließen Sie Ihre Yahoo! Konto bei Livefyre, um Benutzern die Verwendung ihrer Yahoo! sich anmelden, um mit Apps auf Ihrer Site zu interagieren.

So aktivieren Sie die Anmeldung mit einem Yahoo! account:

1. Schalten Sie den Umschalter **[!UICONTROL Enable Login with Yahoo!]** in **[!UICONTROL ON]** um.

1. hinzufügen Sie Ihre Yahoo! die Werte **[!UICONTROL Client ID]** und **[!UICONTROL Client Secret]**.

   Diese Werte werden in Yahoo! App-Detailseite, verfügbar unter [developer.yahoo.com/apps](https://developer.yahoo.com/apps).

## Aktivieren Sie die Anmeldung mit einem Microsoft Live-Konto {#section_z42_4c5_bbb}

Verbinden Sie Ihr Microsoft Live-ID-Konto mit Livefyre, damit Benutzer ihre Microsoft Live-ID-Anmeldungen verwenden können, um mit Apps auf Ihrer Site zu interagieren.

So aktivieren Sie die Anmeldung mit einem Microsoft Live ID-Konto:

1. Wechseln Sie in **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]** den Umschalter **[!UICONTROL Enable Microsoft Live Login]** zu **[!UICONTROL On]**.

1. Geben Sie **[!UICONTROL Microsoft Live Client ID (Private Key)]** und **[!UICONTROL Microsoft Live Client Secret (Password)]** ein.

1. Klicken **[!UICONTROL Save Settings]**.

   Die Werte **[!UICONTROL Microsoft Live Client ID (Private Key)]** und **[!UICONTROL Microsoft Live Client Secret (Password)]** werden auf der Detailseite der Microsoft Live-ID-App aufgeführt.

## Verbinden Sie Ihre Social-Apps mit Ihrer Livefyre-Identität {#section_on2_vc5_bbb}

Ermöglichen Sie Ihren Benutzern, Ihre Livefyre-Identitätsimplementierung für Apps auf Ihrer Site zu verwenden.

1. Eine App erstellen.
1. Navigieren Sie zu **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]** **[!UICONTROL Livefyre Identity]**.

1. Geben Sie die erforderlichen App-Anmeldeinformationen für die erstellte App ein.
