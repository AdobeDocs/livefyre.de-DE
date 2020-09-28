---
description: Fügen Sie Livefyre zu Ihren nativen mobilen Apps hinzu.
seo-description: Fügen Sie Livefyre zu Ihren nativen mobilen Apps hinzu.
seo-title: Mobile SDKs
solution: Experience Manager
title: Mobile SDKs
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Mobile SDKs{#mobile-sdks}

Fügen Sie Livefyre zu Ihren nativen mobilen Apps hinzu.

Es stehen verschiedene Optionen für mobile Implementierungen zur Verfügung, je nach Umfang der Anpassung, die Sie planen:

* Mobile Web-Apps
* Livefyre Android- oder iOS-SDKs
* HTTP-APIs

## Mobile Web-Apps {#section_t2k_vpb_11b}

Kunden, die eine Webseite auf einem Mobilgerät öffnen, erhalten automatisch einen Livefyre-Inhaltsstream, der für Mobilgeräte optimiert ist. Dazu gehören die Formatierung, die an die reduzierte Bildschirmgröße angepasst wird, und Änderungen zur Handhabung von Berührungsereignissen.

>[!NOTE]
>
>Bei Verwendung einer Livefyre-App in einer Android-WebView muss der Parameter Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) auf true eingestellt sein. Wenn localStorage nicht aktiviert ist, kann Livefyre keinen Benutzer bei der Livefyre-App anmelden.

Zur Optimierung für Mobilgeräte beschränkt Livefyre die Funktionen "Kommentare", "Live-Blog"und "Chat-App"auf Folgendes:

* Posten
* Vorlage     
* Markierung
* Gefällt mir
* Antwort
* Listener-Anzahl
* Anzahl der Kommentare
* Inline-Moderation ausstehend
* Hovercards
* Wichtigste Kommentare
* Hotkeys
* Warteschlangenkommentare

Wenn Sie in mobilen Web-Apps auf den Namen eines Autors klicken, werden die Informationen zur Karte in einer neuen Seite geöffnet.

## Livefyre Android SDK oder iOS SDK {#section_zdz_spb_11b}

Livefyre bietet außerdem zwei mobile SDKs: ein iOS-SDK und ein Android-SDK. Diese SDKs sind Wrapper um unsere HTTP-Endpunkte herum, die eine einfachere Methode zum Senden und Empfangen von Daten bieten. Mit diesen SDKs wird keine Oberfläche bereitgestellt, was eine größere Flexibilität bei der Anzeige und Verwendung der Inhalte in Ihrer mobilen App ermöglicht.

Die Android- und iOS-SDKs unterstützen die folgenden Funktionen für Kommentare, Live-Blog und Chat:

| iOS-Funktionen: | Android-Funktionen: |
|--- |--- |
| <ul><li> Posten </li><li>Vorlage      </li><li>Markierung </li><li>Gefällt mir </li><li>Antwort </li><li>Hotkeys</li></ul> | <ul><li>Posten </li><li>Vorlage      </li><li>Gefällt mir </li><li>Antwort </li><li>Hotkeys</li></ul> |

## HTTP-APIs {#section_yqb_qpb_11b}

Die HTTP-APIs sind die Gruppe von Endpunkten, mit denen Sie Konversationen und Inhalte auf der Livefyre-Plattform erstellen können. Außerdem werden alle Livefyre-Streams sofort einsatzbereit gemacht. Diese Lösung erfordert zwar mehr Entwicklungszeit von Ihrem Entwicklungsteam, bietet jedoch mehr Flexibilität bei der Verwendung der Livefyre-Produktsuite und ermöglicht die native Integration von Mobilgeräten.

>[!IMPORTANT]
>
>**Erstellen Sie keine** Benutzerauthentifizierungstoken im mobilen Client, da dies erfordert, dass Sie Ihren Livefyre-geheimen Netzwerkschlüssel in einer unbesicherten App verfügbar machen. Eine stabilere und sicherere Lösung finden Sie im Abschnitt Benutzerauthentifizierungstoken.

