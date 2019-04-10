---
description: Versionshinweise für die Version vom 23. März 2018.
seo-description: Versionshinweise für die Version vom 23. März 2018.
seo-title: 23. März 2018
solution: Experience Manager
title: 23. März 2018
uuid: b 69 b 8715-ace 4-48 e 0-8 f 54-ce 4 e 12170 ef 3
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 23. März 2018{#march}

Versionshinweise für die Version vom 23. März 2018.

## Neue Funktionen {#section_syx_mdt_wcb}

Die folgenden Funktionen sind in der Produktionsversion dieser Version neu:

* **Neu in Produktion:** Facebook hat ein Sicherheits-Update auf Facebook-Anmeldung erstellt, das dazu führt, dass die Facebook-Anmeldung eines Kunden nicht ordnungsgemäß funktioniert hat. Um dieses Problem zu beheben, müssen Sie Folgendes tun:

   1. Fügen Sie die folgende URL zum **[!UICONTROL Valid OAuth redirect URIs]** Feld "Client oauth-Einstellungen" hinzu. Durch `<networkname>` Ihren richtigen Netzwerknamen ersetzen:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Wechseln **[!UICONTROL Use Strict Mode for Redirect URI]****[!UICONTROL Yes]**Sie zu.

* **Neu in UAT:** Sie können nun den Vertrauensschwellenwert für Smart-Tags in Streams auswählen. Wenn Sie die Genauigkeit (0-100) für Tags festlegen, können Sie die Genauigkeit der Assets steuern, die wir abrufen.

## Probleme {#section_ehw_ndt_wcb}

Die Probleme in den folgenden Tabellen wurden in dieser Version behoben.

## Produktionsversion

| **Ausgabentyp** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Bug | Medienpinnwand | Es wurde ein Problem in der Medienpinnwand behoben, bei dem Tags nicht anklickbar waren, wenn ein Instagram-Beitrag aus einer Stream-Regel hinzugefügt wurde. |
| Bug | Modq | Es wurde ein Problem behoben, durch das modq nicht ordnungsgemäß geladen wurde. |
| Bug | Modq | Es wurde ein Problem behoben, durch das das Einbetten von Audio dazu führte, dass modq nicht mehr funktionierte. |

## UAT-Version

| **Ausgabentyp** | **Komponente** | **Versionshinweise** |
|---|---|---|
| Verbesserung | Filmstreifen | Es wurden einige Probleme behoben, durch die der Filmstreifen leichter zugänglich gemacht werden konnte. |
| Verbesserung | Studio | Sie können sich jetzt mit einer IMS-Anmeldung bei Livefyre anmelden. |

