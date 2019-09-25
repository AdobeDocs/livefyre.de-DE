---
description: Führen Sie Stresstests für die Livefyre-Plattform durch.
seo-description: Führen Sie Stresstests für die Livefyre-Plattform durch.
seo-title: Stresstest-Richtlinie
solution: Experience Manager
title: Stresstest-Richtlinie
uuid: f2d49b55-f4fc-485f-9aea-a17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Stresstest-Richtlinie{#stress-test-policy}

Führen Sie Stresstests für die Livefyre-Plattform durch.

Dieses Dokument enthält Anleitungen zum Ausführen von Stresstests für die Livefyre-Plattform. Ad-hoc-Tests durch Kunden ohne Benachrichtigung sind streng verboten. Für mehr über [verbotene und erlaubte Aktivitäten](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Stresstests sind optional. Sie müssen keinen Stresstest durchführen oder müssen diesen durchführen. Adobe Livefyre führt im Rahmen des Veröffentlichungsprozesses regelmäßige Stresstests und Überprüfungen durch. Wenn Sie Tests durchführen möchten, werden in diesem Dokument die Anforderungen und Einschränkungen für die Durchführung von Stresstests beschrieben.

## Benachrichtigung {#section_ihs_bfz_vdb}

Sie müssen Ihren Livefyre Customer Success Specialist und Adobe Technical Consultant drei oder mehr Wochen vor dem geplanten Start über Ihre geplanten Tests informieren.

Um Livefyre zu benachrichtigen, senden Sie die folgenden Informationen an Ihren Livefyre Customer Success Specialist und Adobe Technical Consultant:

* Zweck und Beschreibung der Prüfung
* Der Verwendungsfall, gegen den Sie testen
* Liste der Livefyre-APIs, die Sie im Test verwenden möchten
* Datum, Uhrzeit und Dauer der Prüfung
* IP-Adressen, von denen Sie die Tests starten

## Voraussetzungen {#section_khs_bfz_vdb}

Sie dürfen Tests nur durchführen, wenn sie die folgenden Anforderungen erfüllen:

* Sie müssen eine explizite schriftliche Genehmigung von einem Adobe Technical Consultant erhalten, mindestens 3 Wochen vor Beginn des Tests.
* **Sie dürfen nur Tests im UAT-Netzwerk durchführen.**
* Sie müssen mit realistischen Szenarien testen. Sie können beispielsweise nicht davon ausgehen, dass Ihre Eigenschaft täglich *Millionen* von Beitragsanfragen bereitstellt, da dies kein realistisches Szenario ist. Wenn Sie Hilfe bei der Feststellung benötigen, ob Ihr Szenario realistisch ist, wenden Sie sich an Ihren Livefyre Customer Success Specialist oder den technischen Berater von Adobe.
* Tests sollten während der Geschäftszeiten für die Pacific Standard Time Zone \(UTC -7\) durchgeführt werden.
* Möglicherweise müssen Sie Daten und Ihre Gründe für den Test angeben.

## Governance {#section_mhs_bfz_vdb}

Livefyre behält sich das Recht vor, einen Test jederzeit zu beenden, wenn Sie einen Test durchführen:

* Im Produktionsnetzwerk.
* Ohne ausdrückliche schriftliche Genehmigung durch einen technischen Berater von Adobe 3 Wochen oder länger im Voraus.
* Gegen unrealistische Szenarien.

Livefyre beendet Tests, indem es den Zugriff auf APIs blockiert, Livefyre-Netzwerke deaktiviert und eine Anforderung zum Testen von Daten verweigert, wenn die Anforderungen nicht erfüllt werden.
