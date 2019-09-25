---
description: Versionshinweise für die Version vom 15. Februar 2018.
seo-description: Versionshinweise für die Version vom 15. Februar 2018.
seo-title: 15. Februar 2018
solution: Experience Manager
title: 15. Februar 2018
uuid: ee46f088-9fb7-49e2-a42c-e0d4b2f24a32
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# February 15, 2018{#february}

Versionshinweise für die Version vom 15. Februar 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden Funktionen sind in der Produktionsversion dieser Version neu:

* **Smart-Tags.**

   Livefyre verwendet die Adobe Sensei-Bilderkennungstechnologie, um Bilder, die Sie in der Bibliothek speichern, automatisch mit Tags zu versehen.
Mit intelligenten Tags sparen Sie Zeit beim Suchen und Moderieren von Inhalten. Mit intelligenten Tags können Sie:

   * Gespeicherte Bilder nach genauem Inhalt basierend auf dem Bildinhalt statt nur nach Text suchen
   * Erfassen von Inhalten in Streams basierend auf genauen Suchbegriffen, die das Bild analysieren, statt nur Text
   Weitere Informationen zu intelligenten Tags finden Sie unter [intelligente Tags](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags).

* **In-Produkt-Nachrichten.** Wenn Sie sich jetzt bei Livefyre Studio anmelden, wird ein Fenster mit Hinweisen angezeigt, in dem Updates zu neuen Funktionen angezeigt werden.
* **UGC für Karussell.** Sie können jetzt alle Funktionen von UGC Commerce in der Livefyre Carousel App verwenden. Sie können eine Aktionsaufruf-Schaltfläche erstellen und Ihren Produktkatalog mit der App verbinden, um ein Einkaufserlebnis aus Carousel zu erstellen.

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

## Produktionsversion

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | ModQ | Es wurde ein Problem behoben, bei dem Instagram-Beiträge, die als genehmigt oder als abgestürzt markiert markiert wurden, erneut in die Warteschlange eingereiht wurden. |
| Verbesserung | Rights Management | Es wurde eine Verbesserung hinzugefügt, um eine Warnung anzuzeigen, wenn versucht wird, abgelaufene Instagram-Konten bei der Anforderung von Rechten zu verwenden. |
| Fehler | Trends | Es wurde ein Problem behoben, bei dem die Trends-App manchmal HTTP und nicht HTTPS zulässt. |

## UAT-Version

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Verbesserung | Apps | Es wurde die Möglichkeit hinzugefügt, Apps aus Livefyre zu löschen. |
| Fehler | Umfragen | Umfragen wurden geändert, um ausschließlich HTTPS zu verwenden. Bisher waren Umfragen weiterhin für HTTP zulässig. |
| Fehler | UGC | Es wurde ein Problem behoben, bei dem UGC in einer Visualisierungs-App nicht wie erwartet nach Produkt-ID gefiltert hat. |

