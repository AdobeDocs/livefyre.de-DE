---
description: Fügen Sie den nativen mobilen Apps Livefyre hinzu.
seo-description: Fügen Sie den nativen mobilen Apps Livefyre hinzu.
seo-title: Mobile sdks
solution: Experience Manager
title: Mobile sdks
uuid: 84 c 7 ca 1 c -4401-492 a-bfa 5-62 b 996947 a 44
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Mobile sdks{#mobile-sdks}

Fügen Sie den nativen mobilen Apps Livefyre hinzu.

Es gibt verschiedene Optionen für Implementierungen mobiler Anwendungen, je nachdem, wie viel Anpassungen Sie vornehmen möchten:

* Mobile Web-Apps
* Livefyre Android- oder ios-sdks
* HTTP-apis

## Mobile Web-Apps {#section_t2k_vpb_11b}

Kunden, die eine Webseite auf einem Mobilgerät öffnen, erhalten automatisch einen Livefyre-Inhaltsstream, der für Mobilgeräte optimiert ist, einschließlich der Formatierung, um die reduzierte Bildschirmgröße und Änderungen an Berührungsereignissen anzupassen.

>[!NOTE]
>
>Bei Verwendung einer Livefyre-App in einer Android webview muss der Parameter Android [websettings. setdomstorageenabled](https://developer.android.com/reference/android/webkit/WebSettings.html) auf true gesetzt werden. Wenn localstorage nicht aktiviert ist, kann Livefyre einen Benutzer nicht in der Livefyre-App protokollieren.

Um für Mobilgeräte zu optimieren, schränkt Livefyre die Funktion Kommentare, Live Blog und Chat App ein:

* Beitrag
* Bearbeiten
* Flag
* Gefällt mir
* Antworten
* Listener-Anzahl
* Kommentaranzahl
* Inline-ausstehende Moderation
* Hoverkarten
* Top-Kommentare
* Hot Threads
* Warteschlangenkommentare

In mobilen Web-Apps werden durch Klicken auf den Namen eines Autors die Hoverkarteninformationen auf einer neuen Seite geöffnet.

## Livefyre Android SDK oder ios SDK {#section_zdz_spb_11b}

Livefyre stellt außerdem zwei mobile sdks bereit: ein ios-SDK und ein Android-SDK. Diese sdks sind Wrapper um unsere HTTP-Endpunkte, die eine einfachere Methode zum Senden und Empfangen von Daten bieten. Mit diesen sdks wird keine Schnittstelle bereitgestellt, wodurch mehr Flexibilität bei der Anzeige und Verwendung der Inhalte in Ihrer mobilen App gewährleistet wird.

Die Android- und ios-sdks unterstützen die folgenden Funktionen für Kommentare, Live-Blog und Chat:

| Ios-Funktionen: | Android-Funktionen: |
|--- |--- |
| <ul><li> Beitrag </li><li>Bearbeiten </li><li>Flag </li><li>Gefällt mir </li><li>Antworten </li><li>Hot Threads</li></ul> | <ul><li>Beitrag </li><li>Bearbeiten </li><li>Gefällt mir </li><li>Antworten </li><li>Hot Threads</li></ul> |

## HTTP-apis {#section_yqb_qpb_11b}

Die HTTP-apis sind die Gruppe von Endpunkten, mit denen Sie Unterhaltungen und Inhalte auf der Livefyre-Plattform erstellen können. Außerdem werden alle Livefyre aus den Box-Streams entfernt. Diese Lösung erfordert mehr Entwicklungszeit von Ihrem Technikteam, bietet jedoch mehr Flexibilität bei der Verwendung der Livefyre-Produktsuite und ermöglicht eine native mobile Integration.

>[!IMPORTANT]
>
>**Erstellen Sie** keine Benutzerauthentifizierungstoken im mobilen Client, da dies dazu erforderlich wäre, dass Sie den geheimen Livefyre-Schlüssel in einer nicht geschützten App bereitstellen. Eine solidere und sicherere Lösung finden Sie im Abschnitt Benutzerauthentifizierungstokens.

