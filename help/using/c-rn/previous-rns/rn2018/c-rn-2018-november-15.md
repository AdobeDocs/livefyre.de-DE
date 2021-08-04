---
description: Versionshinweise für die Version vom 15. November 2018.
title: Versionshinweise
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
source-git-commit: beb224fdccf68c98fc3eff62b0867f22fa52902b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 6%

---

# Versionshinweise{#release-notes}

Versionshinweise für die Version vom 15. November 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden neuen Funktionen wurden in der Produktionsversion dieser Version veröffentlicht:

* **Aktualisierungen der Instagram-Suche und -Streams.** Sie können ein  *Instagram-* Geschäftskonto wie folgt verwenden:

   * Führen Sie eine Instagram-Social-Suche nach Benutzer durch (der Benutzer muss auch ein Instagram-Geschäftskonto sein).

   * Erstellen Sie Instagram-Streams von einem bestimmten Instagram-Benutzerkonto aus (das Konto muss auch ein Geschäftskonto sein), einschließlich Ihres eigenen.

   * Fordern Sie mithilfe eines teilweise automatisierten Workflows Rechte für Assets von Instagram an.

   * Informationen dazu, welche Art von Instagram-Konten Sie einrichten und von Instagram anfordern müssen, finden Sie unter [Über Instagram-Konten](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Die automatische Überwachung von Antworten auf Anfragen zu Nutzungsrechten für kontenbasierte Suchen.** Nur für datenbankbasierte Suchen - die Möglichkeit, Antworten auf Rechteanfragen automatisch zu überwachen und den Aktivitätsverlauf in Livefyre zu aktualisieren, ist verfügbar.

Weitere Informationen zum Anfordern von Berechtigungen für Instagram-Konten finden Sie unter [Instagram-Rechteanforderung manuell senden](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) und [Teilautomatisierte Instagram-Rechteanforderung senden](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Adobe Target-Integration.** Die Integration mit Adobe Target wurde hinzugefügt, sodass Sie Livefyre-Apps direkt in Ihrer Adobe Target-Angebotsbibliothek freigeben können. Weitere Informationen zur Verwendung von Livefyre mit Adobe Target finden Sie in der [Target-Dokumentation](https://experienceleague.adobe.com/docs/livefyre/using/library/livefyre-target.html).

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

### Produktionsversion

| Art des Problems | Komponente | Versionshinweise |
|--- |--- |--- |
| Fehler | AppService: Livefyre-Identität | Es wurde ein Problem behoben, durch das durch Klicken auf [!UICONTROL Reset to Default] das Logo unter Anmeldemodul in Studio > Integrationseinstellungen > Livefyre-Identität nicht auf das Standardbild zurückgesetzt wurde. |
| Fehler | Bibliothek | Es wurde ein Problem behoben, bei dem ein Video, das in die Bibliothek hochgeladen und dann in Asset-Details angezeigt wurde, nicht korrekt angezeigt wurde. |
| Fehler | Streams | Es wurde ein Fehler behoben, der verhinderte, dass Produkte in einer Stream-Regel angezeigt wurden. |
| Fehler | Streams | Es wurde ein Problem behoben, bei dem Produkt-Tags für eine Stream-Regel nicht verfügbar waren. |
| Verbesserung | Studio | Es wurde ein Problem behoben, bei dem die Produkt-ID nicht in Livefyre Studio angezeigt wurde. |
| Fehler | Studio: ModQ | Es wurde ein Problem behoben, bei dem gelöschte Inhalte nach dem Löschen weiterhin in ModQ angezeigt wurden. |

### UAT-Version

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Social-Komponente: Karussell | Es wurde ein Problem behoben, bei dem der Freigabe-Link nicht reagierte und die URL wie erwartet in IE11 und Mozilla Firefox kopierte. |
