---
description: hinzufügen Sie Livefyre auf Ihre native iOS-App.
title: Livefyre iOS SDK
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Livefyre iOS SDK{#livefyre-ios-sdk}

hinzufügen Sie Livefyre auf Ihre native iOS-App.

Verwenden Sie diese Open-Source-Bibliothek, um Livefyre-Dienste in Ihre native iOS-App zu integrieren. Das Livefyre StreamHub iOS SDK bietet eine dünne Schicht um unsere gemeinsamen API-Mechanismen, basierend auf der hervorragenden AFNetworking-Bibliothek.

Livefyre bietet außerdem zwei iOS-Beispielanwendungen, die auf diesem SDK basieren: einen Kommentar-Stream und eine Reviews-Beispielanwendung.

## Integrieren des SDK in Ihr Projekt als Cocoa Pod (empfohlen) {#section_qc5_h3v_zz}

Die einfachste Möglichkeit, StreamHub-iOS SDK zu Ihrem Projekt hinzuzufügen, ist die Verwendung von CocoaPods. Wenn Sie nicht über CocoaPods verfügen, führen Sie Edelstein-Installations-Cocoapods und Pod-Setup aus. Hier ein Beispiel für eine Poddatei:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Sie müssen Ihrer CocoaPod-Installation auch ein SPECS-Repository hinzufügen (dies klont es in den Ordner `~/.cocoapods/repos`):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Nachdem Sie die Poddatei im Stammordner Ihres App-Projekts erstellt und das Repository oben hinzugefügt haben, führen Sie Folgendes aus:

```
pod install
```

Dadurch werden alle Abhängigkeiten heruntergeladen und eine Datei &quot;MyApp.xcworkspace&quot;erstellt, die Sie von jetzt an verwenden sollten, um Ihr App-Projekt in Xcode zu öffnen.

## Als Xcode-Unterprojekt {#section_jcm_g3v_zz}

Alternativ können Sie das Repository klonen:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Als Nächstes fügen Sie Ihrer App das Xcode-Projekt (LFSClient.xcodeproj) als Teilprojekt hinzu (einfach durch Ziehen der Datei &quot;LFSClient.xcodeproj&quot;in den Bereich &quot;Project Navigator&quot;in Xcode).

Sie müssen dies auch bei allen Abhängigkeiten tun ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

## Laden Sie alles auf einmal herunter (nicht empfohlen) {#section_rpb_f3v_zz}

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
>Um Tests in Xcode 6 auszuführen, müssen Sie $(PLATFORM_DIR)/Developer/Library/Frameworks zu FRAMEWORK_SEARCH_PATHS in Pods-test-XCTest+OHHTTPStubSuiteCleanUp pod[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704) hinzufügen.

Sie benötigen die Datei &quot;LFSTestConfig.plist&quot;aus Livefyre, die Livefyre auf Anfrage bereitstellt.

## Xcode-Dokumentation {#section_arl_b3v_zz}

Sie können die [documentation](https://livefyre.github.com/StreamHub-iOS-SDK/) durchsuchen oder die &quot;Documentation&quot;-Zielgruppe in Ihrem Xcode (erfordert die Installation von appledoc) auf Ihrem System erstellen.

## Voraussetzungen {#section_m5l_13v_zz}

StreamHub iOS SDK-Versionen seit Version 0.2.0 erfordern iOS 6.0 oder höher.

## Anhang (JSON-Unterstützung) {#section_pcd_5hv_zz}

Für diejenigen, die sich die StreamHub-iOS SDK-Internale ansehen, beachten Sie, dass wir eine modifizierte Version von [JSONKit](https://github.com/escherba/JSONKit) als Standard-JSON-Parser verwenden (anstelle der von Apple bereitgestellten NSJSONSerialisierung). Wir mussten dies tun, weil der von Apple bereitgestellte Parser keine Dekodierung von JSON-Dateien unterstützt, die Ganzzahlen oder Gleitkommazahlen enthalten, die größer sind als jene, die vom System dargestellt werden können. Unsere modifizierte Version von JSONKit schneidet sehr große Zahlen auf das entsprechende Systemmaximum ab, anstatt eine Ausnahme auszulösen.
