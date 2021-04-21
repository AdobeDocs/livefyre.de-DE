---
description: Führen Sie Stresstests für die Livefyre-Plattform durch.
title: Stresstest-Richtlinie
exl-id: cb87b6ca-4107-46fc-9b1e-dc9399ec6d3a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Stresstest-Richtlinie{#stress-test-policy}

Führen Sie Stresstests für die Livefyre-Plattform durch.

Dieses Dokument bietet Anleitungen zur Durchführung von Stresstests gegen die Livefyre-Plattform. Ad-hoc-Tests durch Kunden ohne Benachrichtigung sind streng verboten. Für weitere Informationen über [Unzulässige und zulässige Aktivitäten](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Stresstests sind optional. Sie müssen keinen Stresstest durchführen oder müssen diesen durchführen. Adobe Livefyre führt regelmäßig Stresstests und Validierungen im Rahmen des Veröffentlichungsvorgangs durch. Wenn Sie Tests durchführen möchten, werden in diesem Dokument die Anforderungen und Einschränkungen für die Durchführung von Stresstests erläutert.

## Benachrichtigung {#section_ihs_bfz_vdb}

Sie müssen Ihren Livefyre Customer Success Specialist und Adobe Technical Consultant drei oder mehr Wochen vor Beginn über Ihre geplanten Tests informieren.

Um Livefyre zu benachrichtigen, senden Sie die folgenden Informationen an Ihren Livefyre Customer Success Specialist und Adobe Technical Consultant:

* Zweck und Beschreibung der Prüfung
* Der Verwendungsfall, gegen den Sie testen
* Liste aller Livefyre-APIs, die Sie im Test verwenden möchten
* Datum, Uhrzeit und Dauer der Prüfung
* IP-Adressen, von denen Sie die Tests starten

## Voraussetzungen {#section_khs_bfz_vdb}

Sie dürfen Tests nur durchführen, wenn sie die folgenden Anforderungen erfüllen:

* Sie müssen eine ausdrückliche schriftliche Genehmigung von einem technischen Berater der Adobe 3 Wochen oder länger erhalten, bevor Sie mit dem Test beginnen.
* **Sie dürfen nur Tests im UAT-Netzwerk durchführen.**
* Sie müssen einen Test mit realistischen Szenarien durchführen. Sie können beispielsweise nicht davon ausgehen, dass Ihre Eigenschaft *millionen* von Beitragsanforderungen jeden Tag bereitstellt, da dies kein realistisches Szenario ist. Wenn Sie Hilfe benötigen, um festzustellen, ob Ihr Szenario realistisch ist, fragen Sie Ihren Livefyre Customer Success Specialist oder Adobe Technical Consultant.
* Tests sollten während der Geschäftszeiten für die Pacific Standard Time Zone \(UTC -7\) durchgeführt werden.
* Möglicherweise müssen Sie Daten und Ihre Gründe für den Test angeben.

## Governance {#section_mhs_bfz_vdb}

Livefyre behält sich das Recht vor, einen Test jederzeit zu beenden, wenn Sie einen Test durchführen:

* Im Produktionsnetzwerk.
* Ohne ausdrückliche, schriftliche Genehmigung durch einen technischen Berater der Adobe drei Wochen oder länger im Voraus.
* Gegen unrealistische Szenarien.

Livefyre beendet Tests, indem es den Zugriff auf APIs blockiert, Livefyre-Netzwerke deaktiviert und eine Anforderung zum Testen von Daten verweigert, wenn die Anforderungen nicht erfüllt werden.
