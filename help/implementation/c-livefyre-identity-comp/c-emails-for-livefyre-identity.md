---
description: null
seo-description: null
seo-title: E-Mails für Livefyre-Identität
solution: Experience Manager
title: E-Mails für Livefyre-Identität
uuid: 4 e 807803-687 e -4 df 0-94 d 1-b 18 a 48 d 024 e 8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# E-Mails für Livefyre-Identität{#emails-for-livefyre-identity}

Livefyre-Identität sendet die folgenden E-Emails:

* [E-Mail zum Zurücksetzen des Kennworts](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Verifizierungs-E-Mail](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [E-Mail-Überprüfung für Benutzer senden](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Begrüßungs-E-Mail](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Begrüßungs-E-Mail an Benutzer senden](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Sie können das Erscheinungsbild aller Livefyre-Identitätse-Emails in **[!UICONTROL Integration Settings > Email Notifications.]**

## E-Mail zum Zurücksetzen des Kennworts {#section_nd1_whs_p1b}

Livefyre sendet automatisch eine E-Email zum Zurücksetzen des Kennworts, wenn ein Benutzer versucht, sein Kennwort zurückzusetzen.

Die E-Mail zum Zurücksetzen des Kennworts sieht wie folgt aus:

**Betreff:** Kennwort zurücksetzen

**Haupttext:**

Hey there *< username >*,

Es gab eine Anforderung zum Ändern des Kennworts Ihres Profils unter *< Netzname >*.

Wenn Sie dies angefordert haben, klicken Sie auf den folgenden Link, um ein neues Kennwort auszuwählen: *< Kennwort zurücksetzen >*.

*< Benutzername >*, *< network name >*und *< password reset url >* werden alle dynamisch basierend auf dem Site-Besucher und Ihrem Netzwerk generiert.

## Verifizierungs-E-Mail {#section_ak5_xhs_p1b}

Sie können eine E-Mail an die E-Mail-Adresse eines Benutzers senden. Um Verifizierungs-E-Emails zu senden, müssen Sie die Option unter **Integrationseinstellungen > Livefyre-Identität aktivieren**.

Die Verifizierungs-E-Mail sieht wie folgt aus:

**Betreff:** E-Mail-Bestätigung

**Haupttext:**

Hallo *< Benutzername >*,

Klicken Sie auf den folgenden Link (oder fügen Sie ihn in Ihren Browser ein), um Ihr Konto zu bestätigen: *< verification URL >*.

Dieser Link läuft in 24 Stunden ab.

Danke,

Der < *Kundenname >* Team

*< Benutzername >*, *< network name >*und *< verification URL >* werden alle dynamisch basierend auf dem Site-Besucher und Ihrem Netzwerk generiert.

## E-Mail-Überprüfung an Benutzer senden {#section_vyv_yhs_p1b}

Sie können eine E-Mail an einen Benutzer senden, um die E-Mail-Adresse zu bestätigen, die für die Anmeldung bei einem Konto verwendet wird. So senden Sie eine Überprüfungs-E-Mail

1. Klicken Sie in Studio auf das Zahnradsymbol, um die Netzwerkeinstellungen zu ändern.
1. Klicken **Sie auf Integrationseinstellungen > Livefyre-Identität.**

1. Navigieren Sie zu **Anmeldetypen**.
1. Klicken **Sie auf E-Mail-Überprüfung** erforderlich, um eine E-Email an Benutzer zu senden, die die E-Email-Adresse bestätigen, die sie für die Anmeldung bei einem Konto verwenden.
1. Navigieren Sie zur **Netzwerk-E-Mail** , um das **Logo für E-Mail**zu konfigurieren, die E-Email-Adresse für die Verwendung als Adresse (**E-Mail von**) und den Anzeigenamen für die E-Email-Adresse (**E-Mail-Anzeigename**).

## Begrüßungs-E-Mail {#section_z2v_zhs_p1b}

Sie können eine Begrüßungs-E-Mail an Benutzer senden. Um Begrüßungs-E-Emails zu senden, müssen Sie die Option unter **Integrationseinstellungen** > **Livefyre-Identität aktivieren**.

Die Begrüßungs-E-Mail sieht wie folgt aus:

**Betreff:** Willkommen bei *< Kundenname >*

**Haupttext:**

Hallo *< Benutzername >*,

Ein Konto wurde für Sie unter *< Kundenname > erstellt*.

Dieses Konto wurde unter *< Referrer-URL >* von IP-Adresse *> IP-Adresse > erstellt*.

Wenn Sie dies getan haben, können Sie diese E-Mail sicher ignorieren.

Wenn Sie dies nicht getan haben, wenden Sie sich bitte an `support@livefyre.com`

Danke

The *"customer name"* Team

*" Benutzername" , "Kundenname" ," Verweisende URL"* und "IP-Adresse" werden alle dynamisch basierend auf dem Site-Besucher und Ihrem Netzwerk generiert.

## Begrüßungs-E-Mail an einen Benutzer senden {#section_kjp_c3s_p1b}

Sie können eine Begrüßungs-E-Mail an einen Benutzer senden, nachdem sie sich für ein Konto registriert haben. Studio sendet diese E-Mail nach dem Senden einer Verifizierungs-E-Mail, wenn Sie eine Verifizierungs-E-Mail einrichten. So senden Sie eine Begrüßungs-E-Mail

1. Klicken Sie in Studio auf das Zahnradsymbol, um die Netzwerkeinstellungen zu ändern.
1. Klicken Sie auf **[!UICONTROL Integration Settings > Livefyre Identity]**

1. **[!UICONTROL Email Settings]**Navigieren Sie zu.

1. Klicken **[!UICONTROL Send Welcome Emails To New Users]** Sie auf, um das Senden von E-Emails zu aktivieren.
1. Navigieren Sie zum **[!UICONTROL Network Email]** Konfigurieren des *Logos für E-Mail*, die E-Email-Adresse für die Verwendung als Adresse (**E-Mail von**) und den Anzeigenamen für die E-Email-Adresse (**E-Mail-Anzeigename**).
