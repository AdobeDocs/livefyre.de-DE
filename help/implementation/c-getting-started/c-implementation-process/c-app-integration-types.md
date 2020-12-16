---
description: Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Anwendungsfall ab. Auf dieser Seite werden die Funktionen für die drei Möglichkeiten zum Erstellen einer App erläutert.
seo-description: Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Anwendungsfall ab. Auf dieser Seite werden die Funktionen für die drei Möglichkeiten zum Erstellen einer App erläutert.
seo-title: CMS-App-Integrationen
solution: Experience Manager
title: CMS-App-Integrationen
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---


# CMS-App-Integrationen{#cms-app-integrations}

Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Anwendungsfall ab. Auf dieser Seite werden die Funktionen für die drei Möglichkeiten zum Erstellen einer App erläutert.

Die Livefyre-Integration ist unabhängig von jeder CMS- und User Profil- und Auth-Plattform. Implementieren Sie Livefyre auf eine oder mehrere Arten, je nach Anwendungsfall und Anforderungen.

Sie können die herkömmliche Integration verwenden, um benutzerdefinierte AEM zu erstellen.

## Übersicht über den CMS-App-Integrationstyp

| Typ | Entwicklungserfordernis | Funktionen | Vorteile | Einschränkungen |
|--- |--- |--- |--- |--- |
| App-Designer | Sehr niedrig | Erstellen Sie JS-Einbettungen in Studio, um Seiten ohne Entwickler <br>Verfügbare eingeschränkte Formatierung und Konfigurationen hinzuzufügen </br>Anwendungsfall: Seiten mit einmaliger Nutzung (Ereignis-Abdeckung, Kampagnen, Hubs) | Sie können eine App in kurzer Zeit einrichten und ausführen. <br>Konfigurationen können von einem nicht-technischen Mitglied durchgeführt werden. <br>Einfache Änderungen an Konfigurationen im Handumdrehen | Muss eine App mit Livefyre Studio zuerst <br>Nicht automatisiert erstellen |
| Livefyre.js | Mittel | Integrieren von Apps in das JavaScript Ihrer Seiten <br>Verwendungsfall: Wiederverwendbare Vorlagen (redaktioneller Inhalt, Produktübersichten) | Verwenden Sie die vollständige Suite der App-Anpassungen und -Konfigurationen <br>Automatisiert den Prozess zum dynamischen Instanziieren von Apps aus Ihrem CMS auf Ihre Seiten | Benötigen Sie einen Entwickler im Vordergrund. |
| SDK-APIs | Advanced | Rufen Sie Ihre Inhalte von Livefyre ab, um sie für benutzerdefinierte Anwendungen <br>Anpassen des Front-End-Angebots über das unterstützte Angebot hinaus <br>Anwendungsfall: Data/Analytics-Integrationen und benutzerdefinierte Front-End-Apps | Volle Power über das Erscheinungsbild der App | Erfordert Entwicklung im Vordergrund. <br>Höhere Entwicklungsbemühungen zur Implementierung. |
