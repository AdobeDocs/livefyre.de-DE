---
description: 'null '
seo-description: 'null '
seo-title: E-Mails für Livefyre-Identität
solution: Experience Manager
title: E-Mails für Livefyre-Identität
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 1%

---


# E-Mails für Livefyre-Identität{#emails-for-livefyre-identity}

Livefyre Identity sendet folgende E-Mails:

* [E-Mail zum Zurücksetzen des Kennworts](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Verifizierungs-E-Mail](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [E-Mail-Bestätigung für Benutzer senden](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Begrüßungs-E-Mail](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Begrüßungs-E-Mail an Benutzer senden](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Sie können das Erscheinungsbild aller Livefyre Identity-E-Mails in **[!UICONTROL Integration Settings > Email Notifications.]** anpassen

## E-Mail zum Zurücksetzen des Kennworts {#section_nd1_whs_p1b}

Livefyre sendet automatisch eine E-Mail zum Zurücksetzen des Kennworts, wenn ein Benutzer versucht, sein Kennwort zurückzusetzen.

Die E-Mail zum Zurücksetzen des Kennworts sieht wie folgt aus:

**Betrifft: Kennwort** zurücksetzen

**Text:**

Hey da *&lt;username>*,

Es wurde eine Anforderung zum Ändern des Kennworts Ihres Profils unter *&lt;Netzwerkname>* gesendet.

Klicken Sie auf den folgenden Link, um ein neues Kennwort auszuwählen, falls Sie dies angefordert haben: *&lt;Kennwort zurücksetzen-URL>*.

*&lt;username>*,  *&lt;network name=&quot;&quot;>* und  *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* werden basierend auf dem Site-Besucher und Ihrem Netzwerk dynamisch generiert.

## Verification Email {#section_ak5_xhs_p1b}

Sie können eine E-Mail zur Bestätigung der E-Mail-Adresse eines Benutzers senden. Um Verifizierungs-E-Mails zu senden, müssen Sie die Option unter **Integrationseinstellungen > Livefyre-Identität** aktivieren.

Die Verifizierungs-E-Mail sieht folgendermaßen aus:

**Betrifft:** E-Mail-Überprüfung

**Text:**

Hallo *&lt;username>*,

Bitte klicken Sie auf den folgenden Link (oder fügen Sie ihn in Ihren Browser ein), um Ihr Konto zu überprüfen: *&lt;Verifizierungs-URL>*.

Dieser Link läuft in 24 Stunden ab.

Vielen Dank

*&lt;Kundenname>* Team

*&lt;username>*,  *&lt;network name=&quot;&quot;>* und  *&lt;verification URL=&quot;&quot;>* werden basierend auf dem Site-Besucher und Ihrem Netzwerk dynamisch generiert.

## Senden einer E-Mail-Bestätigung an Benutzer {#section_vyv_yhs_p1b}

Sie können eine E-Mail an einen Benutzer senden, um die E-Mail-Adresse zu überprüfen, mit der er sich für ein Konto anmeldet. So senden Sie eine Verifizierungs-E-Mail:

1. Klicken Sie in Studio auf das Zahnradsymbol, um die Netzwerkeinstellungen zu ändern.
1. Klicken Sie auf **Integrationseinstellungen > Livefyre-Identität.**

1. Navigieren Sie zu **Anmeldungstypen**.
1. Klicken Sie auf **E-Mail-Bestätigung erforderlich**, um eine E-Mail an Benutzer zu senden, die die für die Anmeldung eines Kontos verwendete E-Mail-Adresse überprüfen.
1. Navigieren Sie zu **Netzwerk-E-Mail**, um das **Logo für E-Mail**, die E-Mail-Adresse, die als &quot;Von&quot;-Adresse (**E-Mail von**) verwendet werden soll, und den Anzeigenamen, der für die E-Mail-Adresse (**E-Mail-Anzeigename**) verwendet werden soll.) verwendet werden soll.

## Begrüßungs-E-Mail {#section_z2v_zhs_p1b}

Sie können eine Begrüßungs-E-Mail an Benutzer senden. Um Begrüßungs-E-Mails zu senden, müssen Sie die Option unter **Integrationseinstellungen** > **Livefyre-Identität** aktivieren.

Die Begrüßungs-E-Mail sieht folgendermaßen aus:

**Betrifft:** Willkommen bei  *&lt;customer name=&quot;&quot;>*

**Text:**

Hallo *&lt;username>*,

Ein Konto wurde für Sie unter *&lt;Kundenname>* erstellt.

Dieses Konto wurde unter *&lt;Verweis-URL>* von IP-Adresse ** erstellt.

Wenn Sie dies tun, können Sie diese E-Mail unbedenklich ignorieren.

Wenn Sie dies nicht getan haben, wenden Sie sich bitte an `support@livefyre.com`

Danke

Das *&quot;Kundenname&quot;* Team

*&quot;Benutzername&quot;, &quot;Kundenname&quot;, &quot;Verweis-URL&quot;* und &quot;IP-Adresse&quot;werden dynamisch auf Basis des Site-Besuchers und Ihres Netzwerks generiert.

## Begrüßungs-E-Mail an einen Benutzer {#section_kjp_c3s_p1b} senden

Sie können eine Begrüßungs-E-Mail an einen Benutzer senden, nachdem dieser sich für ein Konto angemeldet hat. Studio sendet diese E-Mail, nachdem eine Verifizierungs-E-Mail gesendet wurde, wenn Sie eine Verifizierungs-E-Mail eingerichtet haben. So senden Sie eine Begrüßungs-E-Mail:

1. Klicken Sie in Studio auf das Zahnradsymbol, um die Netzwerkeinstellungen zu ändern.
1. Klicken **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Navigieren Sie zu **[!UICONTROL Email Settings]**.

1. Klicken Sie auf **[!UICONTROL Send Welcome Emails To New Users]**, um das Senden von E-Mails zu aktivieren.
1. Navigieren Sie zu **[!UICONTROL Network Email]**, um das *Logo für E-Mail*, die E-Mail-Adresse, die als &quot;Von&quot;-Adresse (**E-Mail von**) verwendet werden soll, und den Anzeigenamen für die E-Mail-Adresse (**E-Mail-Anzeigename**) zu konfigurieren.
