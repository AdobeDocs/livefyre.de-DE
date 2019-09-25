---
description: Fügen Sie Ihrer nativen iOS-App Livefyre hinzu.
seo-description: Fügen Sie Ihrer nativen iOS-App Livefyre hinzu.
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef31a-49fc-4b25-b0c5-300f27067302
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

Fügen Sie Ihrer nativen iOS-App Livefyre hinzu.

Verwenden Sie diese Open-Source-Bibliothek, um Livefyre-Dienste in Ihre native iOS-App zu integrieren. Das Livefyre StreamHub iOS SDK bietet eine dünne Schicht um unsere gemeinsamen API-Mechanismen, basierend auf der hervorragenden AFNetworking-Bibliothek.

Livefyre bietet außerdem zwei iOS-Beispielanwendungen, die auf diesem SDK basieren: einen Kommentar-Stream und eine Reviews-Beispielanwendung.

## Integrieren des SDKs in Ihr Projekt als Cocoa Pod (empfohlen) {#section_qc5_h3v_zz}

Die einfachste Möglichkeit, StreamHub-iOS SDK zu Ihrem Projekt hinzuzufügen, ist die Verwendung von CocoaPods. Wenn Sie nicht über CocoaPods verfügen, führen Sie Edelstein-Installations-Cocoapods und Pod-Setup aus. Hier ein Beispiel für eine Poddatei:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Sie müssen außerdem Ihrer CocoaPod-Installation ein SPECS-Repository hinzufügen (dies klont es in `~/.cocoapods/repos` Verzeichnis):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Nachdem Sie die Poddatei im Stammordner Ihres App-Projekts erstellt und das Repository oben hinzugefügt haben, führen Sie Folgendes aus:

```
pod install
```

Dadurch werden alle Abhängigkeiten heruntergeladen und eine Datei "MyApp.xcworkspace"erstellt, die Sie von jetzt an verwenden sollten, um Ihr App-Projekt in Xcode zu öffnen.

## Als Xcode-Unterprojekt {#section_jcm_g3v_zz}

Alternativ können Sie das Repository klonen:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Als Nächstes fügen Sie Ihrer App das Xcode-Projekt (LFSClient.xcodeproj) als Teilprojekt hinzu (einfach durch Ziehen der Datei "LFSClient.xcodeproj"in den Bereich "Project Navigator"in Xcode).

Sie müssen dies auch mit allen Abhängigkeiten tun ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

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
>Um Tests in Xcode 6 auszuführen, müssen Sie $(PLATFORM_DIR)/Developer/Library/Frameworks zu FRAMEWORK_SEARCH_PATHS in Pods-test-XCTest+OHHTTPStubSuiteCleanUp[podhttps://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704)hinzufügen.

Sie benötigen die Datei "LFSTestConfig.plist"aus Livefyre, die Livefyre auf Anfrage bereitstellt.

## Xcode-Dokumentation {#section_arl_b3v_zz}

Sie können die [Dokumentation](https://livefyre.github.com/StreamHub-iOS-SDK/) durchsuchen oder das Ziel "Dokumentation"in Ihrem Xcode (vorausgesetzt, dass Appledoc installiert werden muss) auf Ihrem System erstellen.

## Voraussetzungen {#section_m5l_13v_zz}

StreamHub iOS SDK-Versionen seit Version 0.2.0 erfordern iOS 6.0 oder höher.

## Anhang (JSON-Unterstützung) {#section_pcd_5hv_zz}

Für diejenigen, die StreamHub-iOS SDK-Internale betrachten, beachten Sie bitte, dass wir eine modifizierte Version von [JSONKit](https://github.com/escherba/JSONKit) als Standard-JSON-Parser verwenden (anstelle der von Apple bereitgestellten NSJSONSerialisierung). Wir mussten dies tun, weil der von Apple bereitgestellte Parser keine Dekodierung von JSON-Dateien unterstützt, die Ganzzahlen oder Gleitkommazahlen enthalten, die größer sind als jene, die vom System dargestellt werden können. Unsere modifizierte Version von JSONKit schneidet sehr große Zahlen auf das entsprechende Systemmaximum ab, anstatt eine Ausnahme auszulösen.
