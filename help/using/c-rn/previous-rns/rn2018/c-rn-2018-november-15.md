---
description: Versionshinweise für die Version vom 15. November 2018.
seo-description: Versionshinweise für die Version vom 15. November 2018.
seo-title: Versionshinweise
solution: Experience Manager
title: Versionshinweise
uuid: 34 e 64943-dea 6-46 ac -9 fcc -8 febeab 6 aa 42
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Versionshinweise{#release-notes}

Versionshinweise für die Version vom 15. November 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden neuen Funktionen wurden in der Produktionsversion dieser Version veröffentlicht:

* **Updates für Instagram-Suche und -stream.** Sie können ein *Instagram-Geschäftskonto* für Folgendes verwenden:

   * Führen Sie eine Instagram-Social-Suche nach dem Benutzer durch (Benutzer müssen ein Instagram-Geschäftskonto sein).

   * Erstellen Sie Instagram-Streams aus einem bestimmten Instagram-Benutzerkonto (das Konto muss auch ein Geschäftskonto sein), einschließlich Ihrer eigenen.

   * Anfordern von Rechten für Assets von Instagram mit einem teilweise automatisierten Arbeitsablauf.

   * Informationen zu den Instagram-Konten, die Sie über Instagram einrichten und anfordern müssen, finden Sie unter [Instagram-Konten](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Automatische Überwachung der Anforderungsrechte für Verwendungsrechte für geschäftskontobasierte Suchen.** Nur für geschäftsbasierte Suchen—die Möglichkeit, Antworten automatisch auf Rechte von Rechten zu überwachen und den Aktivitätsverlauf in Livefyre zu aktualisieren.

Weitere Informationen zum Anfordern von Rechten für Instagram-Konten finden Sie unter [Instagram Rights Request manuell](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) senden und [teilweise automatisierte Instagram-Rechte senden](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Adobe Target-Integration.** Integration mit Adobe Target ermöglicht, sodass Sie Livefyre-Apps direkt an Ihre Adobe Target-Angebotsbibliothek freigeben können. Weitere Informationen zur Verwendung von Livefyre mit Adobe Target finden Sie in der [Target-Dokumentation](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html).

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

### Produktionsversion

| Ausgabentyp | Komponente | Versionshinweise |
|--- |--- |--- |
| Ausgabe | Appservice: Livefyre-Identität | Es wurde ein Problem behoben, durch das Klicks [auf! UICONTROL Zurücksetzen auf Standard] wurde das Logo unter "Login Modal" unter Studio > Integrationseinstellungen > Livefyre Identity to the default image nicht zurückgesetzt. |
| Ausgabe | Bibliothek | Es wurde ein Problem behoben, durch das ein in die Bibliothek hochgeladenes Video, das dann in der Asset-Details angezeigt wurde, nicht richtig angezeigt wurde. |
| Ausgabe | Streams | Es wurde ein Fehler behoben, der verhinderte, dass Produkte in einer Stream-Regel angezeigt wurden. |
| Ausgabe | Streams | Es wurde ein Problem behoben, durch das Produkt-Tags für eine Stream-Regel nicht verfügbar waren. |
| Verbesserung | Studio | Es wurde ein Problem behoben, durch das Produkt-Ids in Livefyre Studio nicht angezeigt wurden. |
| Ausgabe | Studio: Modq | Ein Problem wurde behoben, bei dem gelöschte Inhalte nach dem Löschen weiterhin in modq angezeigt wurden. |

### UAT-Version

| **Ausgabentyp** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Ausgabe | Social-Komponente: Karussell | Es wurde ein Problem behoben, durch das der Link "Freigeben" nicht in IE 11 und Mozilla Firefox angezeigt und die URL wie erwartet kopiert wurde. |