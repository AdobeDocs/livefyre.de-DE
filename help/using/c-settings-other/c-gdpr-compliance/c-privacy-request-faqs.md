---
description: Antworten auf häufig gestellte Fragen zu GDPR-Ready Datenschutzanforderungen.
seo-description: Antworten auf häufig gestellte Fragen zu GDPR-Ready Datenschutzanforderungen.
seo-title: Häufig gestellte Fragen zu Datenschutzanfragen
solution: Experience Manager
title: Häufig gestellte Fragen zu Datenschutzanfragen
uuid: 0 cd 6 f 0 d 2-504 d -46 e 9-ac 46-070536 cda 86
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Häufig gestellte Fragen zu Datenschutzanfragen{#privacy-request-faqs}

Antworten auf häufig gestellte Fragen zu GDPR-Ready Datenschutzanforderungen.

* **Wie können Site-Besucher sich von der Verfolgung auf einer Site ausschließen, die Livefyre-Apps verwendet?** Wenn ein Site-Besucher sich abmeldet, muss die Kundenimplementierung Livefyre darauf hinweisen, dass der Benutzer sich vor der Instanziierung einer App abgemeldet hat. Livefyre has created a way to do this with the JavaScript option, `userPrivacyOptOut`. Weitere Informationen dazu finden Sie `userPrivacyOptOut`unter [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   Wenn das `userPrivacyOptOut` Flag auf "true" gesetzt ist, übertragen alle Apps auf der Seite keine Daten mithilfe von Cookies oder einer anderen Methode an Livefyre-Server. Livefyre aktualisiert dann keine lokalen Speicherung mit Daten, die zur Verfolgung von Site-Besuchern verwendet werden könnten. Wenn eine Quelle einen Proxy nicht unterstützt, zeigt Livefyre eine Maske auf dem Inhalt an, es sei denn, ein Benutzer klickt auf das Video und genehmigt die potenzielle Verfolgung aus dieser Quelle.

   Wenn Sie die Livefyre-Identität verwenden, können Benutzer ihr Profil löschen oder einen Bericht mit Daten erstellen, die für ihr Benutzerkonto verfolgt werden.

* **Wie kann ich verhindern, dass zukünftige Inhalte von einem Site-Besucher erfasst werden, der sich abgemeldet hat?** Verwenden `userPrivacyOptOut` Sie die Verwendung auf `livefyre.js` einer Webseite, die Livefyre-Apps verwendet. Weitere `userPrivacyOptOut`Informationen finden Sie unter [userprivacyoptout](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Wie erstelle ich einen Bericht und löschen Sie die Daten für App-Benutzer oder Inhaber von Social-Konten?**[Datenschutzanfragen](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) , um einen Bericht zu erstellen und Benutzerdaten aus Apps zu löschen.

* **Wie entferne ich den gesamten Inhalt für einen Besucher?** Livefyre unterhält keine persistenten Informationen über Site-Besucher, außer in Form von Cookies, um sie eindeutig für Livecount-Funktionen zu identifizieren. Livecount ist eine transiente und Echtzeitanzahl der Besucher auf der Site. Es wird kein Verlauf beibehalten, nachdem der Besucher Cookies verlässt oder löscht.

   Erstellen Sie eine [Datenschutzanforderung](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) , um das Konto zu löschen. Livefyre löscht oder macht das Benutzerprofil und alle zugehörigen Datensätze anonym.

* **Wie entferne ich Inhalte für einen registrierten Benutzer?** Erstellen Sie eine [Datenschutzanforderung](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) , um das Konto zu löschen. Das Benutzerprofil und alle zugehörigen Aufzeichnungen werden vollständig zerstört.

   >[!NOTE]
   >
   >Diese Aktion kann nicht rückgängig gemacht werden.

* **Wie erstelle ich einen Bericht mit Daten, die von einem aktuellen oder früheren Mitarbeiter verfolgt werden?**[Zeigen Sie einen Datenschutzbericht](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) an, um einen Bericht mit Daten zu erstellen, die für ein Benutzerkonto verfolgt werden.

* **Ist der Livefyre-Social-Stream kompatibel?** Wenn ein Benutzer einen Beitrag oder Tweet aus ihrem sozialen Netzwerk löscht, wird innerhalb von 24 Stunden der Inhalt aus allen Quellen in Livefyre gelöscht. Dies gilt für Twitter und Facebook.

