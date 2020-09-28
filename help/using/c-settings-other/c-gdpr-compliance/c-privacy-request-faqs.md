---
description: Antworten auf häufig gestellte Fragen (FAQs) zu GDPR-Ready-Datenschutzanforderungen.
seo-description: Antworten auf häufig gestellte Fragen (FAQs) zu GDPR-Ready-Datenschutzanforderungen.
seo-title: Häufig gestellte Fragen zur Datenschutzanforderung
solution: Experience Manager
title: Häufig gestellte Fragen zur Datenschutzanforderung
uuid: 0cd6f0d2-504d-46e9-ac46-070536cda086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Häufig gestellte Fragen zur Datenschutzanforderung{#privacy-request-faqs}

Antworten auf häufig gestellte Fragen (FAQs) zu GDPR-Ready-Datenschutzanforderungen.

* **Wie können Site-Besucher sich von der Verfolgung auf einer Site ausschließen, die Livefyre-Apps verwendet?** Wenn sich ein Besucher der Site abmeldet, muss die Kundenimplementierung Livefyre mitteilen, dass der Benutzer sich vor der Instanziierung einer App abgemeldet hat. Livefyre hat eine Möglichkeit geschaffen, dies mit der JavaScript-Option zu tun, `userPrivacyOptOut`. Weitere Informationen zur Verwendung `userPrivacyOptOut`finden Sie unter [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Wenn das `userPrivacyOptOut` Flag auf "true"gesetzt ist, senden Apps auf der Seite keine Daten mithilfe von Cookies oder einer anderen Methode an Livefyre-Server. Livefyre aktualisiert dann nicht den lokalen Speicher mit Daten, die zur Verfolgung von Site-Besuchern verwendet werden könnten. Wenn eine Quelle keinen Proxy unterstützt, zeigt Livefyre eine Maske für den Inhalt an, es sei denn, ein Benutzer klickt auf das Video und genehmigt die potenzielle Verfolgung aus dieser Quelle.

   Wenn Sie Livefyre Identity verwenden, können Benutzer entweder ihr Profil löschen oder einen Bericht mit den für ihr Benutzerkonto verfolgten Daten erstellen.

* **Wie kann ich verhindern, dass zukünftiger Inhalt von einem Site-Besucher erfasst wird, der sich abgemeldet hat?** Verwendung `userPrivacyOptOut` mit `livefyre.js` auf einer Webseite, die Livefyre-Apps verwendet. Weitere Informationen `userPrivacyOptOut`finden Sie unter [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Wie erstelle ich einen Bericht und lösche die Daten für App-Benutzer oder Inhaber sozialer Konten?** [Datenschutzanforderungen](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) , um einen Bericht zu erstellen und Benutzerdaten aus Apps zu löschen.

* **Wie entferne ich den gesamten Inhalt eines Besuchers?** Livefyre pflegt keine beständigen Informationen über Site-Besucher, außer in Form von Cookies, um sie eindeutig für Livecount-Funktionen zu identifizieren. Livecount ist eine vorübergehende und Echtzeitanzahl der Besucher auf der Site. Nach dem Verlassen oder Löschen von Cookies wird kein Verlauf beibehalten.

   Erstellen Sie eine [Datenschutzanforderung](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) , um das Konto zu löschen. Livefyre löscht oder macht das Benutzerprofil und damit verbundene Datensätze anonym.

* **Wie entferne ich Inhalte für einen registrierten Benutzer?** Erstellen Sie eine [Datenschutzanforderung](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) , um das Konto zu löschen. Das Benutzerprofil und alle damit verbundenen Datensätze werden vollständig zerstört.

   >[!NOTE]
   >
   >Diese Aktion kann nicht rückgängig gemacht werden.

* **Wie erstelle ich einen Bericht über Daten, die von einem aktuellen oder ehemaligen Mitarbeiter verfolgt werden?** [Zeigen Sie einen Datenschutzbericht](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) an, um einen Bericht mit den für ein Benutzerkonto verfolgten Daten zu erstellen.

* **Ist Livefyre Social Stream kompatibel?** Wenn ein Benutzer einen Beitrag oder Tweet aus seinem sozialen Netzwerk löscht, wird der Inhalt innerhalb von 24 Stunden auch aus allen Quellen in Livefyre gelöscht. Dies gilt für Twitter und Facebook.

