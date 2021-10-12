---
description: Fügen Sie Livefyre zu Ihrer nativen iOS App hinzu.
title: Livefyre iOS SDK
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Livefyre iOS SDK{#livefyre-ios-sdk}

Fügen Sie Livefyre zu Ihrer nativen iOS App hinzu.

Verwenden Sie diese Open-Source-Bibliothek, um Livefyre-Dienste in Ihre native iOS-App zu integrieren. Das Livefyre StreamHub iOS SDK bietet eine dünne Schicht um unsere gemeinsamen API-Mechanismen, basierend auf der hervorragenden AFNetworking-Bibliothek.

Livefyre bietet außerdem zwei iOS-Beispiel-Apps, die auf diesem SDK basieren: einen Kommentar-Stream und eine Beispiel-App &quot;Bewertungen&quot;.

## Integrieren des SDK in Ihr Projekt als Kakao-Pod (empfohlen) {#section_qc5_h3v_zz}

Die einfachste Möglichkeit, StreamHub-iOS SDK zu Ihrem Projekt hinzuzufügen, besteht in der Verwendung von CocoaPods. Wenn Sie nicht über CocoaPods verfügen, führen Sie die Einrichtung von Edelstein-Installations-Cocoapods und -Pods durch. Im Folgenden finden Sie ein Beispiel für eine Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

Sie müssen außerdem ein SPECS-Repository zu Ihrer CocoaPod-Installation hinzufügen (dadurch wird es in das Verzeichnis `~/.cocoapods/repos` klont):

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

Nachdem Sie Ihre Podfile im Stammverzeichnis Ihres App-Projekts erstellt und das oben hinzugefügte Repository hinzugefügt haben, führen Sie Folgendes aus:

```
pod install
```

Dadurch werden alle Abhängigkeiten heruntergeladen und eine Datei &quot;MyApp.xcworkspace&quot;erstellt, die Sie von jetzt an verwenden sollten, um Ihr App-Projekt in Xcode zu öffnen.

## Als Xcode-Unterprojekt {#section_jcm_g3v_zz}

Alternativ können Sie das Repository klonen:

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

Fügen Sie anschließend das Xcode-Projekt (LFSClient.xcodeproj) als Unterprojekt zu Ihrer App hinzu (einfach durch Ziehen der Datei LFSClient.xcodeproj in den Bereich Projektnavigator in Xcode).

Dasselbe müssen Sie auch mit allen Abhängigkeiten tun ([AFNetworking](https://github.com/AFNetworking/AFNetworking), [JSONKit](https://github.com/escherba/JSONKit)).

## Alles gleichzeitig herunterladen (nicht empfohlen) {#section_rpb_f3v_zz}

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

Sie können die [Dokumentation](https://github.com/Livefyre/StreamHub-iOS-SDK) durchsuchen oder das Ziel &quot;Dokumentation&quot;in Ihrem Xcode erstellen (es ist erforderlich, dass Appledoc installiert wird).

## Voraussetzungen {#section_m5l_13v_zz}

StreamHub iOS SDK-Versionen seit Version 0.2.0 erfordern iOS 6.0 oder höher.

## Anhang (JSON-Unterstützung) {#section_pcd_5hv_zz}

Für diejenigen, die sich die internen StreamHub-iOS SDK ansehen, beachten Sie bitte, dass wir eine modifizierte Version von [JSONKit](https://github.com/escherba/JSONKit) als standardmäßigen JSON-Parser verwenden (anstelle der von Apple bereitgestellten NSJSONSerialization). Wir mussten dies tun, da der von Apple bereitgestellte Parser die Dekodierung von JSON-Dateien, die Ganzzahlen oder Gleitkommazahlen enthalten, die größer sind als die, die vom System dargestellt werden können, nicht unterstützt. Unsere modifizierte Version von JSONKit schneidet sehr große Zahlen auf das entsprechende Systemmaximum ab, anstatt eine Ausnahme auszulösen.
