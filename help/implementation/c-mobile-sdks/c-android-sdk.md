---
description: Erstellen Sie Android-Apps mit Livefyre.
seo-description: Erstellen Sie Android-Apps mit Livefyre.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

Erstellen Sie Android-Apps mit Livefyre.

Verwenden Sie diese Bibliothek, um Livefyre-Dienste in Ihre native Android-App zu integrieren. Das [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) bietet eine dünne Schicht um unsere gemeinsamen API-Mechanismen, basierend auf der Entwicklungsumgebung von Gradle/Android Studio.

Livefyre bietet außerdem eine Beispielanwendung für [Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) , die auf diesem SDK basiert.

Dieses Livefyre Android SDK kann sowohl in Eclipse als auch in Android Studio verwendet werden.

>[!NOTE]
>
>Vor der Installation des Livefyre Android SDK muss das [Android SDK](https://developer.android.com/sdk/index.html) in Ihrer Umgebung installiert sein. Sie müssen auch einige zusätzliche Android SDK-Pakete einschließen, wie unter Android Developer docs &gt; beschrieben.
>[Hinzufügen von SDK-Paketen](https://developer.android.com/sdk/installing/adding-packages.html)

Verwenden Sie den Android SDK Manager (verfügbar über die Android Studio- oder Eclipse-Symbolleiste), um alle empfohlenen Pakete zu installieren. Achten Sie darauf, auch das Android-Support-Repository einzuschließen.

## Eclipse {#section_dtm_slv_zz}

Hinzufügen des Livefyre Android SDK zu Ihrem Projekt in Eclipse:

1. Holen Sie sich das neueste [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) von GitHub.
1. Beginnen Sie mit einem vorhandenen Projekt oder erstellen Sie ein neues.
1. Um das StreamHub-Android-SDK in Ihren Arbeitsbereich zu importieren, gehen Sie zu **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. StreamHub-Android-SDK durchsuchen und auswählen; es sollte nun im Paket-Explorer angezeigt werden.
1. Klicken Sie mit der rechten Maustaste auf Ihr Projekt und wählen Sie **[!UICONTROL Properties,]** dann die Registerkarte Android.
1. Wählen Sie im Abschnitt Bibliothek die Option StreamHub-Android-SDK **[!UICONTROL Add button,]** und wählen Sie dann in der Liste der Bibliotheken die Option StreamHub-Android-SDK.
1. Klicken Sie auf **[!UICONTROL Apply]** und **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

So fügen Sie das Livefyre Android SDK Ihrem Projekt in Android Studio hinzu:

1. Holen Sie sich das neueste [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) von GitHub.
1. Beginnen Sie mit einem vorhandenen Projekt oder erstellen Sie ein neues.
1. Klicken Sie mit der rechten Maustaste auf das Projekt und wählen Sie **[!UICONTROL Open Module Settings]**.
1. Klicken Sie auf die **[!UICONTROL +]** Schaltfläche in der oberen linken Ecke des Fensters.
1. Wählen Sie **[!UICONTROL Import Existing Project.]** (In der neuen Version des Android-Studios finden Sie **[!UICONTROL Import Existing Project]** unter **[!UICONTROL More Modules]**.)

1. Durchsuchen Sie das StreamHub-Android-SDK und wählen Sie es aus.

Android Studio kann verlangen, dass Sie das SDK in die Greifversion konvertieren. Wenn dies der Fall ist, wählen Sie **[!UICONTROL next]** dann **[!UICONTROL finish]**.

Wechseln Sie zum **Projektordner &gt; App-Ordner &gt; Datei "build.gradle** "unter "Abhängigkeiten", um die folgende Abhängigkeit hinzuzufügen:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Vergewissern Sie sich, dass die folgende Zeile im **Projektordner &gt; settings.gradle** -Datei enthalten ist:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Sie können Konfigurationen in Config.java anpassen.

## Kunden {#section_yfq_blv_zz}

Das StreamHub Android SDK stellt mehrere Client-Klassen bereit, mit denen Livefyre-API-Endpunkte angefordert werden können:

* **AdminClient** tauscht ein Benutzerauthentifizierungstoken für Benutzerinformationen, Schlüssel und andere Metadaten aus.

* **BootstrapClient** Erhalten Sie aktuelle Inhalte und Metadaten zu einer bestimmten Sammlung.

* **StreamClient** fragt einen Stream nach einer Sammlung ab, um neue, aktualisierte und gelöschte Inhalte abzurufen.

* **WriteClient** Post, Flag und Ähnliches wie Inhalt in einer Sammlung.

