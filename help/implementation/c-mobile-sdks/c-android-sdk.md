---
description: Erstellen Sie Android-Apps, die mit Livefyre erstellt wurden.
seo-description: Erstellen Sie Android-Apps, die mit Livefyre erstellt wurden.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 88793 fa 9-3 ea 1-4890-b 36 d-b 631 f 1 c 6 f 7 de
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Android SDK{#android-sdk}

Erstellen Sie Android-Apps, die mit Livefyre erstellt wurden.

Verwenden Sie diese Bibliothek, um Livefyre-Dienste in Ihre native Android-App zu integrieren. Das [Livefyre streamhub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) stellt unsere allgemeinen API-Mechanismen anhand der Gradle-/Android Studio-Entwicklungsumgebung bereit.

Livefyre stellt auch eine Beispiel-App [für die Überprüfung](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) bereit, die auf diesem SDK basiert.

Dieses Livefyre Android SDK kann sowohl in Eclipse als auch in Android Studio verwendet werden.

>[!NOTE]
>
>Vor der Installation des Livefyre Android SDK muss das [Android SDK](https://developer.android.com/sdk/index.html) in Ihrer Umgebung installiert sein. Sie müssen auch einige weitere Android SDK-Pakete einbeziehen, wie in den Android Developer docs > beschrieben.
>[SDK-Pakete hinzufügen](https://developer.android.com/sdk/installing/adding-packages.html)

Verwenden Sie den Android SDK Manager (verfügbar über die Android Studio oder Eclipse-Symbolleiste), um alle empfohlenen Pakete zu installieren. Stellen Sie sicher, dass Sie auch das Android-Support-Repository einschließen.

## Eclipse {#section_dtm_slv_zz}

So fügen Sie dem Projekt in Eclipse das Livefyre Android SDK hinzu:

1. Besorgen Sie sich das neueste [streamhub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) von github.
1. Beginnen Sie mit einem vorhandenen Projekt oder erstellen Sie eine neue.
1. Gehen **[!UICONTROL File > Import > General > Existing Project into Workspace]**Sie zum Import von streamhub-Android-SDK in Ihren Arbeitsbereich.
1. Suchen Sie das streamhub-Android-SDK und wählen Sie es aus. Sie sollte nun im Paket-Explorer angezeigt werden.
1. Klicken Sie mit der rechten Maustaste auf Ihr Projekt und wählen **[!UICONTROL Properties,]** Sie dann die Android-Registerkarte.
1. Wählen Sie im Abschnitt Bibliothek die **[!UICONTROL Add button,]** Option streamhub-Android-SDK aus der Liste der Bibliotheken aus.
1. Klicken Sie auf **[!UICONTROL Apply]** und **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

So fügen Sie dem Projekt das Livefyre Android SDK in Android Studio hinzu:

1. Besorgen Sie sich das neueste [streamhub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) von github.
1. Beginnen Sie mit einem vorhandenen Projekt oder erstellen Sie eine neue.
1. Klicken Sie mit der rechten Maustaste auf Ihr Projekt und wählen **[!UICONTROL Open Module Settings]**Sie.
1. Wählen Sie die **[!UICONTROL +]** Schaltfläche in der oberen linken Ecke des Fensters aus.
1. Auswählen **[!UICONTROL Import Existing Project.]** (in der neuen Version von Android Studio finden Sie **[!UICONTROL Import Existing Project]** unter **[!UICONTROL More Modules]**.)

1. Suchen Sie das streamhub-Android-SDK und wählen Sie es aus.

Android Studio kann anfordern, dass Sie das SDK in eine Gradationsversion konvertieren. Wenn dies eintritt, wählen **[!UICONTROL next]****[!UICONTROL finish]**Sie dann.

Wechseln Sie zu **Projektordner > App-Ordner > build. gradle** file unter Abhängigkeiten, um die folgende Abhängigkeit hinzuzufügen:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Stellen Sie sicher, dass sich die folgende Zeile in Ihrer **Projektordner > settings. gradle** -Datei befindet:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Sie können Konfigurationen in Config. java anpassen.

## Kunden {#section_yfq_blv_zz}

Das streamhub Android SDK stellt mehrere Clientklassen offen, die zum Anfordern von Livefyre-API-Endpunkten verwendet werden können:

* **Adminclient** Exchange Ein Benutzerauthentifizierungstoken für Benutzerinformationen, Schlüssel und andere Metadaten.

* **Bootstrapclient** Abrufen aktueller Inhalte und Metadaten zu einer bestimmten Sammlung.

* **Streamclient** Umfrage a stream for a Collection to get new, updated, and gelöschter Inhalt.

* **Writeclient** Post, flag und like Inhalt in einer Sammlung.

