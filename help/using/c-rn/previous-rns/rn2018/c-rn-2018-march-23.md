---
description: Versionshinweise für die Version vom 23. März 2018.
title: 23. März 2018
exl-id: 85fd6f79-7fa8-425e-b4c7-2e1635d6ef17
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 7%

---

# 23. März 2018{#march}

Versionshinweise für die Version vom 23. März 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden Funktionen sind in der Produktionsversion dieser Version neu:

* **Neu in Produktion:** Facebook hat ein Sicherheitsupdate für Facebook Login erstellt, das dazu führt, dass die Facebook-Anmeldung eines Kunden nicht ordnungsgemäß funktioniert. Um dieses Problem zu beheben, müssen Sie:

   1. hinzufügen Sie die folgende URL in das Feld **[!UICONTROL Valid OAuth redirect URIs]** in den Client-OAuth-Einstellungen. Ersetzen Sie `<networkname>` durch Ihren richtigen Netzwerknamen:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Wechseln Sie **[!UICONTROL Use Strict Mode for Redirect URI]** zu **[!UICONTROL Yes]**.

* **Neu in UAT:** Sie können jetzt den Vertrauensschwellenwert für Smart-Tags in Streams wählen. Wenn Sie den Präzisionswert (0-100) für Tags festlegen, können Sie die Genauigkeit der von uns abgerufenen Assets steuern.

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

## Produktionsversion

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Fehler | Medienwall | Es wurde ein Problem in Media Pinnwand behoben, bei dem Tags nicht angeklickt werden konnten, wenn ein Instagram-Beitrag aus einer Stream-Regel hinzugefügt wurde. |
| Fehler | ModQ | Es wurde ein Problem behoben, durch das ModQ nicht ordnungsgemäß geladen wurde. |
| Fehler | ModQ | Es wurde ein Problem behoben, bei dem das Einbetten von Audio dazu führte, dass ModQ nicht mehr funktionierte. |

## UAT-Version

| **Art des Problems** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Verbesserung | Filmstreifen | Einige Probleme wurden behoben, um den Zugriff auf den Filmstreifen zu erleichtern. |
| Verbesserung | Studio | Sie können sich jetzt mit einem IMS-Login bei Livefyre anmelden. |
