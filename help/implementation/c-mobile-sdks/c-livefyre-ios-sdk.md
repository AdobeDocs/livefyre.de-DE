---
description: Fügen Sie Livefyre zu Ihrer nativen ios-App hinzu.
seo-description: Fügen Sie Livefyre zu Ihrer nativen ios-App hinzu.
seo-title: Livefyre ios SDK
solution: Experience Manager
title: Livefyre ios SDK
uuid: bfdef 31 a -49 fc -4 b 25-b 0 c 5-300 f 27067302
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre ios SDK{#livefyre-ios-sdk}

Fügen Sie Livefyre zu Ihrer nativen ios-App hinzu.

Verwenden Sie diese Open Source-Bibliothek, um Livefyre-Dienste in Ihre native ios-App zu integrieren. Das Livefyre streamhub ios SDK stellt anhand der hervorragenden afnetworking-Bibliothek eine dünne Ebene um unsere allgemeinen API-Mechanismen bereit.

Livefyre stellt außerdem zwei ios-Beispielapps auf Basis dieses SDK bereit: Ein Kommentar-Stream und eine Überprüfungs-App.

## Integration des SDK in das Projekt als Cocoa-Pod (empfohlen) {#section_qc5_h3v_zz}

Das einfachste Verfahren zum Hinzufügen von streamhub-ios SDK zu Ihrem Projekt besteht darin, cocoapods zu verwenden. Wenn Sie keine cocoapods haben, führen Sie "Batch-Installationsknoten" und" Werbeunterbrechung" aus. Beispiel: Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Außerdem müssen Sie Ihrer unternehmenapod-Installation ein Specs-Repository hinzufügen (dies klonen Sie in `~/.cocoapods/repos` den Ordner):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Nachdem Sie Ihre Poddatei im App-Projektstamm erstellt und das oben aufgeführte Repository hinzugefügt haben, führen Sie Folgendes aus:

```
pod install
```

Dadurch werden alle Abhängigkeiten heruntergeladen und eine Datei myapp. xcworkspace erstellt, die Sie ab jetzt verwenden sollten, um Ihr App-Projekt in Xcode zu öffnen.

## Als Xcode-Subprojekt {#section_jcm_g3v_zz}

Alternativ können Sie das Repository klonen:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Fügen Sie anschließend Ihrer App das Xcode-Projekt (lfsclient. xcodeproj) als Subprojekt hinzu (einfach durch Ziehen der lfsclient. xcodeproj-Datei in den Projektnavigator-Bereich in Xcode).

Sie müssen auch mit allen Abhängigkeiten ([afnetworking](https://github.com/AFNetworking/AFNetworking), [jsonkit](https://github.com/escherba/JSONKit)) identisch sein.

## Alles auf einmal herunterladen (nicht empfohlen) {#section_rpb_f3v_zz}

```
cd ~/dev 
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
cd StreamHub-iOS-SDK 
git submodule init 
git submodule update 
pod repo add livefyre https://github.com/Livefyre/cocoapods.git 
pod install 
cd examples/CommentStream 
pod install 
open CommentStream.xcworkspace
```

>[!NOTE]
>
>Um Tests in Xcode 6 auszuführen, müssen Sie $ (PLATFORM_ DIR)/Developer/Library/Frameworks zu FRAMEWORK_ SEARCH_ PATHS in Pods-test-xctest + ohhttpstubsuitecleanup podhttps://stackoverflow.com/a/24651704 hinzufügen[](https://stackoverflow.com/a/24651704).

Sie benötigen die Datei "lfstestconfig. plist" von Livefyre, die Livefyre auf Anforderung bereitstellt.

## Xcode-Dokumentation {#section_arl_b3v_zz}

Sie können die [Dokumentation](https://livefyre.github.com/StreamHub-iOS-SDK/) durchsuchen oder das Ziel "Dokumentation" in Ihrem Xcode-Code (Appledoc muss installiert werden) auf Ihrem System erstellen.

## Anforderungen {#section_m5l_13v_zz}

Streamhub ios SDK-Versionen seit Version 0.2.0 erfordern ios 6.0 oder höher.

## Anhang (JSON-Unterstützung) {#section_pcd_5hv_zz}

Beachten Sie, dass wir eine modifizierte Version von [jsonkit](https://github.com/escherba/JSONKit) als JSON-Standardparser verwenden (anstelle von Apple-bereitgestellter nsjsonserialization), wenn Sie die streamhub-ios SDK-Betriebssysteme anzeigen. Wir mussten dies tun, da der von Apple bereitgestellte Parser keine JSON-Dateien unterstützt, die Ganzzahlen oder Gleitkommazahlen enthalten, die größer sind als die, die vom System dargestellt werden können. Unsere modifizierte Version von jsonkit schneidet sehr große Zahlen zu dem entsprechenden System-Maximum ab, anstatt eine Ausnahme auszulösen.
