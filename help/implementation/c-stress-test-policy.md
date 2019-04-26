---
description: Führen Sie Stresstests für die Livefyre-Plattform aus.
seo-description: Führen Sie Stresstests für die Livefyre-Plattform aus.
seo-title: Stresstest-Richtlinie
solution: Experience Manager
title: Stresstest-Richtlinie
uuid: f 2 d 49 b 55-f 4 fc -485 f -9 aea-a 17 ce 64813 ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Stresstest-Richtlinie{#stress-test-policy}

Führen Sie Stresstests für die Livefyre-Plattform aus.

Dieses Dokument enthält Anleitungen zum Ausführen von Stresstests für die Livefyre-Plattform. Ad-hoc-Tests von Kunden ohne Benachrichtigung sind streng verboten. Weitere Informationen zu [nicht zulässigen und zulässigen Aktivitäten](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Stresstests sind optional. Sie sind nicht erforderlich oder erwartet einen Stresstest. Adobe Livefyre führt im Zuge der Veröffentlichung regelmäßige Stresstests und Überprüfungen durch. Wenn Sie Tests durchführen, werden in diesem Dokument die Anforderungen und Einschränkungen für die Durchführung von Stresstests erläutert.

## Benachrichtigung {#section_ihs_bfz_vdb}

Sie müssen Ihren Livefyre-Kundenerfolgsspezialisten und den technischen Berater von Adobe Ihren geplanten Tests drei oder mehr Wochen vor dem Start der geplanten Tests mitteilen.

Um Livefyre zu benachrichtigen, senden Sie die folgenden Informationen an Ihren Livefyre-Kundenerfolgsspezialisten und den technischen Berater von Adobe:

* Zweck und Beschreibung des Tests
* Der Anwendungsfall, den Sie testen
* Liste aller Livefyre-apis, die Sie im Test verwenden möchten
* Datum, Uhrzeit und Dauer des Tests
* IP-Adressen, aus denen Sie die Tests starten

## Anforderungen {#section_khs_bfz_vdb}

Sie können Tests nur durchführen, wenn sie die folgenden Anforderungen erfüllen:

* Vor Beginn des Tests müssen Sie eine ausdrückliche schriftliche Genehmigung von einem technischen Berater von Adobe 3 Wochen oder mehr erhalten.
* **Sie können nur Tests im UIN-Netzwerk durchführen.**
* Sie müssen vor realistischen Szenarien testen. Sie können beispielsweise nicht davon ausgehen, dass Ihre Eigenschaft *jeden Tag Millionen* von Post-Anforderungen erbringt, da dies kein realistisches Szenario ist. Wenn Sie Hilfe bei der Entscheidung benötigen, ob Ihr Szenario realistisch ist oder nicht, fragen Sie Ihren Livefyre-Kundenerfolgsspezialisten oder den technischen Berater von Adobe.
* Tests sollten während der Geschäftszeiten für die Pacific Standard Zeitzone (UTC -7\) durchgeführt werden.
* Möglicherweise müssen Sie Daten und Ihre Argumente für den Test erstellen.

## Governance {#section_mhs_bfz_vdb}

Livefyre behält sich das Recht vor, einen Test zu beenden, wenn Sie einen Test durchführen:

* Im Produktionsnetzwerk.
* Ohne explizite Genehmigung von einem technischen Berater von Adobe drei Wochen oder mehr im Voraus.
* Gegen unechte Szenarios.

Livefyre beendet Tests durch Blockieren des Zugriffs auf apis, Deaktivieren von Livefyre-Netzwerken und Ablehnen einer Lastanalyseanforderung, wenn diese die Anforderungen nicht erfüllen.
