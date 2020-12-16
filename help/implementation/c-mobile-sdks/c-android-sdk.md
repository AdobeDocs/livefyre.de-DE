---
description: Erstellen Sie Android-Apps mit Livefyre.
seo-description: Erstellen Sie Android-Apps mit Livefyre.
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 1%

---


# Android SDK{#android-sdk}

Erstellen Sie Android-Apps mit Livefyre.

Verwenden Sie diese Bibliothek, um Livefyre-Dienste in Ihre native Android-App zu integrieren. Das [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) bietet eine dünne Ebene um unsere gängigen API-Mechanismen, basierend auf der Entwicklungs-Umgebung von Gradle/Android Studio.

Livefyre bietet auch eine auf diesem SDK basierende Musteranwendung [Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App).

Dieses Livefyre Android SDK kann sowohl in Eclipse als auch in Android Studio verwendet werden.

>[!NOTE]
>
>Vor der Installation des Livefyre Android SDK muss das [Android SDK](https://developer.android.com/sdk/index.html) auf Ihrer Umgebung installiert sein. Sie müssen auch einige zusätzliche Android SDK-Pakete einschließen, wie unter Android Developer docs > beschrieben.
>[Hinzufügen von SDK-Paketen](https://developer.android.com/sdk/installing/adding-packages.html)

Verwenden Sie den Android SDK Manager (verfügbar über die Android Studio- oder Eclipse-Symbolleiste), um alle empfohlenen Pakete zu installieren. Achten Sie darauf, auch das Android-Support-Repository einzuschließen.

## Eclipse {#section_dtm_slv_zz}

So fügen Sie das Livefyre Android SDK Ihrem Projekt in Eclipse hinzu:

1. Holen Sie sich das neueste [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) von GitHub.
1. Beginn mit einem vorhandenen Projekt oder erstellen Sie ein neues.
1. Um das StreamHub-Android-SDK in Ihren Arbeitsbereich zu importieren, gehen Sie zu **[!UICONTROL File > Import > General > Existing Project into Workspace]**.
1. StreamHub-Android-SDK durchsuchen und auswählen; es sollte nun im Paket-Explorer angezeigt werden.
1. Klicken Sie mit der rechten Maustaste auf Ihr Projekt und wählen Sie **[!UICONTROL Properties,]** und dann die Registerkarte Android.
1. Wählen Sie im Abschnitt Bibliothek die Option **[!UICONTROL Add button,]** und wählen Sie dann StreamHub-Android-SDK aus der Liste der Bibliotheken.
1. Klicken Sie auf **[!UICONTROL Apply]** und **[!UICONTROL OK]**.

## Android Studio {#section_vpw_klv_zz}

So fügen Sie das Livefyre Android SDK Ihrem Projekt in Android Studio hinzu:

1. Holen Sie sich das neueste [StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) von GitHub.
1. Beginn mit einem vorhandenen Projekt oder erstellen Sie ein neues.
1. Klicken Sie mit der rechten Maustaste auf Ihr Projekt und wählen Sie **[!UICONTROL Open Module Settings]**.
1. Klicken Sie auf die Schaltfläche **[!UICONTROL +]** in der oberen linken Ecke des Fensters.
1. Wählen Sie **[!UICONTROL Import Existing Project.]** (In der neuen Version des Android-Studios finden Sie **[!UICONTROL Import Existing Project]** unter **[!UICONTROL More Modules]**.)

1. Durchsuchen Sie das StreamHub-Android-SDK und wählen Sie es aus.

Android Studio kann verlangen, dass Sie das SDK in die Greifversion konvertieren. Wenn dies der Fall ist, wählen Sie **[!UICONTROL next]** und dann **[!UICONTROL finish]**.

Wechseln Sie zu **Projektordner > App-Ordner > build.gradle** unter Abhängigkeiten, um die folgende Abhängigkeit hinzuzufügen:

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

Vergewissern Sie sich, dass sich die folgende Zeile in der Datei **Projektordner > settings.gradle** befindet:

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>Sie können Konfigurationen in Config.java anpassen.

## Kunden {#section_yfq_blv_zz}

Das StreamHub Android SDK stellt mehrere Client-Klassen bereit, mit denen Livefyre-API-Endpunkte angefordert werden können:

* **** AdminClientExchange ein Benutzerauthentifizierungstoken für Benutzerinformationen, Schlüssel und andere Metadaten.

* **** BootstrapClientAbrufen aktueller Inhalte und Metadaten zu einer bestimmten Sammlung.

* **** StreamClientUmfasst einen Stream für eine Sammlung, um neue, aktualisierte und gelöschte Inhalte abzurufen.

* **** WriteClientPost, Flag und ähnliche Inhalte in einer Sammlung.

