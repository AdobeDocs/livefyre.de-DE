---
description: 'null'
seo-description: 'null'
seo-title: SSL-Durchsetzung
solution: Experience Manager
title: SSL-Durchsetzung
uuid: e 64 af 8 c 2-3 ab 6-4034-b 385-0 e 552 d 828 c 6 e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053

---


# SSL-Durchsetzung{#ssl-enforcement}

Um sicherzustellen, dass Ihre Daten sicher bleiben, wird HTTP zugunsten von HTTPS nicht mehr unterstützt. Adobe Livefyre deaktiviert alle HTTP- und unsicheren SSL/TLS-Streänen vollständig bis Ende August 2018. Dies ist ein Adobe Standard-Dokument zum Schutz der Privatsphäre von Ihnen und Ihren Benutzern.

## Wer hat betroffen? {#section_jf2_4yz_kcb}

Dies könnte sich auf Livefyre-Kunden auswirken, die über folgende Möglichkeiten verfügen:

* Server-zu-Server-Aufrufe aus ihrem CRM-, CMS-, wordpress- oder anderen Client.
* Mobile Integrationen (Android- und ios-Apps)
* Benutzerdefinierte Anwendungen oder benutzerdefinierter Code

## Was muss ich tun? {#section_unv_dc5_kcb}

1. Alle Livefyre-Kunden müssen über HTTPS für den gesamten Datenverkehr mit allen apis kommunizieren, einschließlich:

   * Server zu Serverintegrationen (CRM, CMS, wordpress usw.)
   * Mobile Integrationen (Android- und ios-Apps)
   * Benutzerdefinierte Anwendungen (Streamhub SDK oder direkt codiert).

1. Server to Server and Mobile HTTP Clients must support TLS 1.2
1. Ändern Sie die Hostnamen `{*}.<network>.fyre.co` von `<network>.{*}.fyre.co`. Der Hostname `example.network.fyre.co` ändert sich beispielsweise in `network.`example. fyre. co «. Beispiel:

   * `bootstrap.<network_name>.fyre.co` to `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` to `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` to `<network_name>.admin.fyre.co`

## Woher weiß ich, ob ich die Änderungen vorgenommen habe? {#section_sqk_5d5_kcb}

Sie können zwar bereits HTTPS verwenden, aber Livefyre empfiehlt, dass Sie doppelt prüfen, insbesondere wenn Sie:

* Server-zu-Server-Aufrufe von Ihrem CMS oder CRM.
* Benutzerdefinierter Code oder Verwendung von sdks für benutzerdefinierte Apps in Javascript oder Mobile.
* Wenn Ihre Integration mehr als ein Jahr alt ist.
* Wenn die Technologie in Ihrem Stapel älter als ein Jahr ist.

Selbst wenn Sie HTTPS bereits verwenden, müssen Sie sicherstellen, dass Ihre API-Clients TLS 1.2 unterstützen.

## Wie kann ich sicherstellen, dass meine API-Clients TLS 1.2 unterstützen? {#section_nd1_j25_kcb}

Eine Person, die an der Entwicklung Ihrer Site arbeitet, kann Folgendes tun:

* Identifizieren Sie die Clientsoftware.
* Identifizieren Sie die Version.
* Lesen Sie die Dokumentation, um sicherzustellen, dass der API-Client TLS 1.2 unterstützt.
* Schalten Sie bei Bedarf Debug-Modus ein.

## Java-Unterstützung für TLS 1.2 {#section_lwn_rwk_ycb}

Oracle und openjdk jvms für Java 8 und höher sind für alle SSL-Verbindungen standardmäßig für die Verwendung von TLS 1.2 konfiguriert. Sie müssen keine zusätzlichen Aktionen durchführen, wenn Sie Java 8 oder höher verwenden.

Benutzer von Java 7 oder früher sollten sich an der öffentlichen Dokumentation zur Aktivierung von TLS 1.2 beteiligen.

## Warum muss ich meine Hostnamen ändern? {#section_d5q_p25_kcb}

Livefyre hat für `{*}.<network>.fyre.co` Domänen keine SSL-Zertifikate. Wenn Sie einfach die URL in HTTPS ändern, wird die Anwendung beschädigt.

## Muss ich auf die neueste Version von Livefyre sdks aktualisieren? {#section_dw5_s25_kcb}

Nein. Stattdessen können Sie den Code ausbessern. Um den Code zu patchen, ändern Sie einige statische Zeichenfolgen und erstellen den Code neu. Wenn Ihr HTTP-Client veraltet ist, müssen Sie auch ein Upgrade vornehmen oder eine andere verwenden.

## Wie lange dauert dies? {#section_lgd_v25_kcb}

Wie lange dies dauert, hängt von Ihrem Setup ab. Wenn Sie eine einfache Implementierung haben, sollte es wenig Zeit für die Bestätigung benötigen. Wenn Sie viele Anpassungen haben, müssen Sie aktualisierte Code auf Ihren Servern oder neuen Apps für App Stores testen und bereitstellen. Um optimale Ergebnisse zu erzielen, empfehlen wir Ihnen, eine erste Überprüfung der Arbeit durchzuführen, damit Sie alle längerfristigen Arbeiten planen können.

## Was ist die Zeitschiene für das Abschließen dieser Arbeit? {#section_kgk_w25_kcb}

Livefyre deaktiviert bis Ende August 2018 den Anschluss 80 (HTTP) und unterstützt nur Verbindungen mit 443 (HTTPS). Browser und andere Clients, die HTTP verwenden möchten, schlagen fehl.

## Wann muss ich diese Arbeit abschließen? {#section_rvb_x25_kcb}

Alle Kunden müssen HTTPS Ende Juli 2018 verwenden. Wenn Sie diesen Termin nicht erreichen können, wenden Sie sich an unser Team unter prioritysupport@livefyre.com.
