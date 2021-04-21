---
description: Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Anwendungsfall ab. Auf dieser Seite werden die Funktionen für die drei Möglichkeiten zum Erstellen einer App erläutert.
title: CMS-App-Integrationen
exl-id: 7590e247-87cc-470e-bab6-e61a19221dbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

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
