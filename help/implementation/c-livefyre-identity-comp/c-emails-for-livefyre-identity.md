---
description: 'null '
seo-description: 'null '
seo-title: E-Mails für Livefyre-Identität
solution: Experience Manager
title: E-Mails für Livefyre-Identität
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# E-Mails für Livefyre-Identität{#emails-for-livefyre-identity}

Livefyre Identity sendet folgende E-Mails:

* [E-Mail zum Zurücksetzen des Kennworts](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Verifizierungs-E-Mail](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [E-Mail-Bestätigung für Benutzer senden](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Begrüßungs-E-Mail](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Begrüßungs-E-Mail an Benutzer senden](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Sie können das Erscheinungsbild aller Livefyre-Identity-E-Mails in **[!UICONTROL Integration Settings > Email Notifications.]**

## E-Mail zum Zurücksetzen des Kennworts {#section_nd1_whs_p1b}

Livefyre sendet automatisch eine E-Mail zum Zurücksetzen des Kennworts, wenn ein Benutzer versucht, sein Kennwort zurückzusetzen.

Die E-Mail zum Zurücksetzen des Kennworts sieht wie folgt aus:

**** Betrifft: Kennwort zurücksetzen

**Text:**

Hey *&lt;Benutzername&gt;*,

Es wurde eine Anforderung zum Ändern des Kennworts Ihres Profils unter *&lt;Netzwerkname&gt;* gesendet.

Klicken Sie auf den folgenden Link, um ein neues Kennwort auszuwählen, falls Sie dies wünschen: *&lt;URL zum Zurücksetzen des Kennworts&gt;*.

*&lt;Benutzername&gt;*, *&lt;Netzwerkname&gt;* und *&lt;URL zum Zurücksetzen des Kennworts&gt;* werden dynamisch basierend auf dem Site-Besucher und Ihrem Netzwerk generiert.

## Verifizierungs-E-Mail {#section_ak5_xhs_p1b}

Sie können eine E-Mail zur Bestätigung der E-Mail-Adresse eines Benutzers senden. Um Verifizierungs-E-Mails zu senden, müssen Sie die Option unter **Integrationseinstellungen &gt; Livefyre-Identität** aktivieren.

Die Verifizierungs-E-Mail sieht folgendermaßen aus:

**** Betrifft: E-Mail-Bestätigung

**Text:**

Hallo *&lt;Benutzername&gt;*,

Bitte klicken Sie auf den folgenden Link (oder fügen Sie ihn in Ihren Browser ein), um Ihr Konto zu überprüfen: *&lt;Verifizierungs-URL&gt;*.

Dieser Link läuft in 24 Stunden ab.

Vielen Dank

Das *&lt;Kundenname&gt;* -Team

*&lt;Benutzername&gt;*, *&lt;Netzwerkname&gt;* und *&lt;Verifizierungs-URL&gt;* werden dynamisch basierend auf dem Site-Besucher und Ihrem Netzwerk generiert.

## E-Mail-Bestätigung an Benutzer senden {#section_vyv_yhs_p1b}

Sie können eine E-Mail an einen Benutzer senden, um die E-Mail-Adresse zu überprüfen, mit der er sich für ein Konto anmeldet. So senden Sie eine Verifizierungs-E-Mail:

1. Klicken Sie in Studio auf das Zahnradsymbol, um die Netzwerkeinstellungen zu ändern.
1. Klicken Sie auf **Integrationseinstellungen &gt; Livefyre-Identität.**

1. Navigieren Sie zu **Anmeldetypen**.
1. Klicken Sie auf **"E-Mail-Bestätigung** erforderlich", um eine E-Mail an Benutzer zu senden, die die für die Kontoanmeldung verwendete E-Mail-Adresse bestätigen.
1. Navigieren Sie zu **Netzwerk-E-Mail** , um das **Logo für E-Mail**, die E-Mail-Adresse, die als Ausgangsadresse verwendet werden soll (**E-Mail-Adresse**) und den Anzeigenamen für die E-Mail-Adresse (**E-Mail-Anzeigename**) zu konfigurieren.

## Begrüßungs-E-Mail {#section_z2v_zhs_p1b}

Sie können eine Begrüßungs-E-Mail an Benutzer senden. Um Begrüßungs-E-Mails zu senden, müssen Sie die Option unter **Integrationseinstellungen** &gt; **Livefyre-Identität** aktivieren.

Die Begrüßungs-E-Mail sieht folgendermaßen aus:

**** Betrifft: Willkommen bei *&lt;Kundenname&gt;*

**Text:**

Hallo *&lt;Benutzername&gt;*,

Unter *&lt;Kundenname&gt;* wurde ein Konto für Sie erstellt.

Dieses Konto wurde unter *&lt;Verweis-URL&gt;* aus IP-Adresse *&lt;IP-Adresse&gt;* erstellt.

Wenn Sie dies tun, können Sie diese E-Mail sicher ignorieren.

Wenn Sie dies nicht getan haben, wenden Sie sich bitte an `support@livefyre.com`

Danke

Das *"Kundenname"* -Team

*"Benutzername", "Kundenname",* "Verweisadresse"und "IP-Adresse"werden dynamisch basierend auf dem Site-Besucher und Ihrem Netzwerk generiert.

## Begrüßungs-E-Mail an einen Benutzer senden {#section_kjp_c3s_p1b}

Sie können eine Begrüßungs-E-Mail an einen Benutzer senden, nachdem er sich für ein Konto angemeldet hat. Studio sendet diese E-Mail, nachdem eine Bestätigungs-E-Mail gesendet wurde, wenn Sie eine Bestätigungs-E-Mail einrichten. So senden Sie eine Begrüßungs-E-Mail:

1. Klicken Sie in Studio auf das Zahnradsymbol, um die Netzwerkeinstellungen zu ändern.
1. Klicken Sie auf **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Navigieren Sie zu **[!UICONTROL Email Settings]**.

1. Klicken Sie auf **[!UICONTROL Send Welcome Emails To New Users]** , um das Senden von E-Mails zu aktivieren.
1. Navigieren Sie **[!UICONTROL Network Email]** zum Konfigurieren des *Logos für E-Mail*, der E-Mail-Adresse, die als "Von"-Adresse verwendet werden soll (**E-Mail-Adresse von**), und des Anzeigennamens, der für die E-Mail-Adresse verwendet werden soll (**E-Mail-Anzeigename**).
