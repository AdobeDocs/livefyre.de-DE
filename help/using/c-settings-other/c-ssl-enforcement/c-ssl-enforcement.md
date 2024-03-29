---
title: SSL-Durchsetzung
description: SSL-Durchsetzung
exl-id: 033e15d9-84f6-42d5-8457-04263dcbd11c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 2%

---

# SSL-Durchsetzung{#ssl-enforcement}

Um sicherzustellen, dass Ihre Daten sicher bleiben, wird HTTP zugunsten von HTTPS eingestellt. Adobe Livefyre wird alle HTTP- und unsicheren SSL/TLS-Chiffren bis Ende August 2018 vollständig deaktivieren. Dies ist eine Adobe Standard zum Schutz der Privatsphäre von Ihnen und Ihren Benutzern.

## Wer ist betroffen? {#section_jf2_4yz_kcb}

Dies könnte sich auf Livefyre-Kunden auswirken, die:

* Server-zu-Server-Aufrufe von CRM, CMS, WordPress oder einem anderen Client.
* Mobile Integrationen (Android- und iOS-Apps)
* Benutzerdefinierte Anwendungen oder benutzerspezifischer Code

## Was muss ich tun? {#section_unv_dc5_kcb}

1. Alle Livefyre-Kunden müssen für den gesamten Traffic mit allen APIs über HTTPS kommunizieren, einschließlich:

   * Server-zu-Server-Integrationen (CRM, CMS, WordPress usw.)
   * Mobile Integrationen (Android- und iOS-Apps)
   * Benutzerdefinierte Anwendungen (Streamhub-SDK oder direkt kodiert).

1. Server to Server und Mobile HTTP Clients müssen TLS 1.2 unterstützen
1. Ändern Sie die Hostnamen von `{*}.<network>.fyre.co` in `<network>.{*}.fyre.co`. Beispielsweise ändert sich der Hostname `example.network.fyre.co` in `network.`example.fyre.co&quot;. Beispiel:

   * `bootstrap.<network_name>.fyre.co`auf `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co`auf `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co`auf `<network_name>.admin.fyre.co`

## Woher weiß ich, ob ich die Änderungen vorgenommen habe? {#section_sqk_5d5_kcb}

Sie können möglicherweise bereits HTTPS verwenden, aber Livefyre empfiehlt eine Überprüfung der Dublette, insbesondere wenn Sie über Folgendes verfügen:

* Server-zu-Server-Aufrufe von Ihrem CMS oder CRM.
* Benutzerdefinierter Code oder Verwendung von SDKs für benutzerdefinierte Apps in JavaScript oder Mobile.
* Wenn Ihre Integration älter als ein Jahr ist.
* Wenn die Technologie in Ihrem Stapel älter als ein Jahr ist.

Auch wenn Sie bereits HTTPS verwenden, müssen Sie sicherstellen, dass Ihre API-Clients TLS 1.2 unterstützen.

## Wie kann ich überprüfen, ob meine API-Clients TLS 1.2 unterstützen? {#section_nd1_j25_kcb}

Eine Person, die an der Entwicklung Ihrer Site arbeitet, kann:

* Identifizieren Sie die Clientsoftware.
* Identifizieren Sie die Version.
* Lesen Sie die Dokumentation, um sicherzustellen, dass der API-Client TLS 1.2 unterstützt.
* Schalten Sie bei Bedarf den Debug-Modus ein.

## Java-Unterstützung für TLS 1.2 {#section_lwn_rwk_ycb}

Oracle und OpenJDK JVMs für Java 8 und höher sind standardmäßig für alle SSL-Verbindungen für die Verwendung von TLS 1.2 konfiguriert. Wenn Sie Java 8 oder höher verwenden, müssen Sie keine weiteren Schritte ausführen.

Benutzer von Java 7 oder früher sollten sich die öffentliche Dokumentation zur Aktivierung von TLS 1.2 ansehen.

## Warum muss ich meine Hostnamen ändern? {#section_d5q_p25_kcb}

Livefyre verfügt nicht über SSL-Zertifikate für `{*}.<network>.fyre.co`-Domänen. Wenn Sie die URL einfach in HTTPS ändern, wird die Anwendung unterbrochen.

## Muss ich auf die neueste Version von Livefyre SDKs aktualisieren? {#section_dw5_s25_kcb}

Nein. Stattdessen können Sie den Code patchen. Um den Code zu patchen, ändern Sie einige statische Zeichenfolgen und erstellen Sie den Code neu. Wenn Ihr HTTP-Client veraltet ist, müssen Sie auch ein Upgrade durchführen oder einen anderen verwenden.

## Wie lange dauert das? {#section_lgd_v25_kcb}

Wie lange dies dauert, hängt von Ihrem Setup ab. Wenn Sie eine einfache Implementierung haben, sollte es wenig Zeit dauern, diese zu bestätigen. Wenn Sie viele Anpassungen vornehmen, müssen Sie aktualisierten Code auf Ihren Servern oder neuen Apps für App Stores testen und bereitstellen. Um optimale Ergebnisse zu erzielen, sollten Sie eine erste Prüfung der Arbeit durchführen, damit Sie eine längerfristige Arbeit planen können.

## Welchen Zeitplan gibt es für den Abschluss dieser Arbeit? {#section_kgk_w25_kcb}

Livefyre wird bis Ende August 2018 den Anschluss 80 (HTTP) für unsere Dienste deaktivieren und nur Verbindungen mit 443 (HTTPS) unterstützen. Browser und andere Clients, die versuchen, HTTP zu verwenden, schlagen fehl.

## Wann muss ich mit dieser Arbeit fertig werden? {#section_rvb_x25_kcb}

Alle Kunden müssen bis Ende Juli 2018 HTTPS verwenden. Wenn Sie diese Frist nicht einhalten können, wenden Sie sich an unser Team unter prioritysupport@livefyre.com.
