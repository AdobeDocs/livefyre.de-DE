---
description: Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Anwendungsfall ab. Auf dieser Seite werden die Funktionen für die drei Möglichkeiten zum Erstellen einer App erläutert.
seo-description: Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Anwendungsfall ab. Auf dieser Seite werden die Funktionen für die drei Möglichkeiten zum Erstellen einer App erläutert.
seo-title: CMS-App-Integrationen
solution: Experience Manager
title: CMS-App-Integrationen
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CMS-App-Integrationen{#cms-app-integrations}

Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Anwendungsfall ab. Auf dieser Seite werden die Funktionen für die drei Möglichkeiten zum Erstellen einer App erläutert.

Die Livefyre-Integration ist unabhängig von jeder CMS- und User Profile- und Auth-Plattform. Implementieren Sie Livefyre auf eine oder mehrere Arten, je nach Anwendungsfall und Anforderungen.

Sie können die herkömmliche Integration verwenden, um benutzerdefinierte AEM-Komponenten zu erstellen.

## Übersicht über den CMS-App-Integrationstyp

| Typ | Entwicklungserfordernis | Funktionen | Vorteile | Einschränkungen |
|--- |--- |--- |--- |--- |
| App-Designer | Sehr niedrig | Erstellen Sie JS-Einbettungen in Studio, um Seiten ohne <br>eingeschränkten Stil und verfügbare Konfigurationen hinzuzufügen </br>Verwendungsfall: Seiten mit einmaliger Nutzung (Ereignisabdeckung, Kampagnen, Hubs) | Sie können eine App in kurzer Zeit einrichten und ausführen. <br>Konfigurationen können von einem nicht-technischen Mitglied durchgeführt werden. <br>Einfache Änderungen an Konfigurationen im Handumdrehen | Muss zuerst eine App mit Livefyre Studio <br>Nicht automatisiert erstellen |
| Livefyre.js | Mittel | Integrieren von Apps in das JavaScript Ihrer Seiten <br>Anwendungsfall: Wiederverwendbare Vorlagen (redaktioneller Inhalt, Produktübersichten) | Verwenden der vollständigen Suite von App-Anpassungen und -Konfigurationen <br>Automatisiert den Prozess zum dynamischen Instanziieren von Apps aus dem CMS auf Ihre Seiten | Benötigen Sie einen Entwickler im Vordergrund. |
| SDK-APIs | Advanced | Abrufen Ihrer Inhalte aus Livefyre zur Verwendung für benutzerdefinierte Anwendungen <br>Anpassen des Front-End über das unterstützte <br>Angebotsszenario hinaus: Data/Analytics-Integrationen und benutzerdefinierte Front-End-Apps | Volle Power über das Erscheinungsbild der App | Erfordert Entwicklung im Vordergrund. <br>Höhere Entwicklungsbemühungen zur Implementierung. |
