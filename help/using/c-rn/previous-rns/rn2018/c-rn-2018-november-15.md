---
description: Versionshinweise für die Version vom 15. November 2018.
seo-description: Versionshinweise für die Version vom 15. November 2018.
seo-title: Versionshinweise
solution: Experience Manager
title: Versionshinweise
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: efb031b58f01ec69c8297a808998d25a0015f102
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 7%

---


# Versionshinweise{#release-notes}

Versionshinweise für die Version vom 15. November 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden neuen Funktionen wurden in der Produktionsversion dieser Version veröffentlicht:

* **Aktualisierungen der Instagram-Suche und des Streams.** Sie können ein *Instagram-Geschäftskonto* verwenden, um:

   * Führen Sie eine Instagram Social-Suche nach dem Benutzer durch (Benutzer muss auch ein Instagram-Geschäftskonto sein).

   * Erstellen Sie Instagram-Streams von einem bestimmten Instagram-Benutzerkonto (das Konto muss auch ein Geschäftskonto sein), einschließlich Ihres eigenen.

   * Fordern Sie Rechte für Assets von Instagram mithilfe eines teilweise automatisierten Workflows an.

   * Weitere Informationen zu Instagram-Konten, die Sie einrichten und über Instagram anfordern müssen, finden Sie unter [Info zu Instagram-Konten](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Die automatische Überwachung von Verwendungsrechten fordert Antworten für kontenbasierte Suchen an.** Nur für datenbankbasierte Suchvorgänge - die Möglichkeit, Antworten auf Berechtigungsanfragen automatisch zu überwachen und den Verlauf der Aktivität in Livefyre zu aktualisieren, ist verfügbar.

Weitere Informationen zum Anfordern von Rechten für Instagram-Konten finden Sie unter [Senden von Instagram-Rights-Anfragen manuell](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) und [Senden einer teilweise automatisierten Instagram-Rights-Anforderung](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Adobe Target-Integration.** Die Integration mit Adobe Target wurde hinzugefügt, sodass Sie Livefyre-Apps direkt in Ihrer Adobe Target Angebots Library freigeben können. Weitere Informationen zur Verwendung von Livefyre mit Adobe Target finden Sie in der Dokumentation zur [Zielgruppe](hhttps://docs.adobe.com/content/help/en/livefyre/using/library/livefyre-target.html).

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

### Produktionsversion

| Art des Problems | Komponente | Versionshinweise |
|--- |--- |--- |
| Fehler | AppService: Livefyre-Identität | Es wurde ein Problem behoben, bei dem das Logo unter &quot;Login Modal in Studio > Integrationseinstellungen > Livefyre-Identität&quot;nicht auf das Standardbild zurückgesetzt [!UICONTROL Reset to Default] wurde. |
| Fehler | Bibliothek | Es wurde ein Problem behoben, bei dem ein Video, das in die Bibliothek hochgeladen und dann im Detail angezeigt wurde, nicht korrekt angezeigt wurde. |
| Fehler | Streams | Es wurde ein Fehler behoben, der verhinderte, dass Produkte in einer Stream-Regel angezeigt wurden. |
| Fehler | Streams | Es wurde ein Problem behoben, bei dem Produkt-Tags für eine Stream-Regel nicht verfügbar waren. |
| Verbesserung | Studio | Es wurde ein Problem behoben, bei dem die Produkt-ID nicht in Livefyre Studio angezeigt wurde. |
| Fehler | Studio: ModQ | Es wurde ein Problem behoben, bei dem gelöschte Inhalte nach dem Löschen weiterhin in ModQ angezeigt wurden. |

### UAT-Version

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Soziale Komponente: Karussell | Es wurde ein Problem behoben, bei dem der Link Freigeben nicht geantwortet und die URL wie erwartet in IE11 und Mozilla Firefox kopiert wurde. |