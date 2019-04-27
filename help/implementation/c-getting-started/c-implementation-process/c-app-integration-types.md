---
description: Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Verwendungsfall ab. Auf dieser Seite werden die Funktionen erläutert, mit denen Sie eine App erstellen können.
seo-description: Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Verwendungsfall ab. Auf dieser Seite werden die Funktionen erläutert, mit denen Sie eine App erstellen können.
seo-title: CMS App Integrationen
solution: Experience Manager
title: CMS App Integrationen
uuid: 14 fd 7 e 36-0 e 50-4 ae 3-97 f 0-2 de 731 c 184 f 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CMS App Integrationen{#cms-app-integrations}

Wenn Sie Livefyre-Apps implementieren, hängt der Stil der Implementierung von Ihrem Verwendungsfall ab. Auf dieser Seite werden die Funktionen erläutert, mit denen Sie eine App erstellen können.

Die Livefyre-Integration ist für alle CMS- und Benutzerprofil- und Auth-Plattformen agnostisch. Implementieren Sie Livefyre auf eine oder mehrere Arten, je nach Verwendungsfall und Anforderungen.

Sie können die herkömmliche Integration verwenden, um benutzerdefinierte AEM-Komponenten zu erstellen.

## Übersicht über den CMS App Integrationstyp

| Typ | Entwicklungsanforderung | Funktionen | Vorteile | Einschränkungen |
|--- |--- |--- |--- |--- |
| App Designer | Sehr niedrig | Erstellen Sie JS-Embed in Studio, um Seiten ohne Entwickler <br>Limited Styling und Konfigurationen hinzuzufügen </br>. Anwendungsfall: Seiten mit einzelnem Einsatz (Ereignisabdeckung, Kampagnen, Hubs) | Eine App kann in kurzer Zeit in Betrieb genommen werden. <br>Konfigurationen können von einem nicht technischen Mitglied vorgenommen werden. <br>Einfache Änderungen an den Konfigurationen | Muss eine App mit Livefyre Studio erstellen, zuerst <br>nicht automatisiert |
| Livefyre. js | Mittel | Apps in javascript Ihrer Seiten <br>integrieren Anwendungsfall: Wiederverwendbare Vorlagen (redaktionelle Inhalte, Produktüberprüfungen) | Verwenden Sie die vollständige Suite der App-Anpassungen und -konfigurationen <br>Automatisiert den Prozess, um Apps dynamisch aus Ihrem CMS auf Ihre Seiten zu instanziieren. | Sie benötigen einen Entwickler voraus. |
| SDK-apis | Erweitert | Rufen Sie Ihren Inhalt von Livefyre ab, der für benutzerdefinierte Anwendungen <br>verwendet werden soll, um Frontend-Übergänge außerhalb von &quot;Nutzungsfall&quot; zu <br>verwenden: Data/Analytics-Integrationen und benutzerdefinierte Frontend-Apps | Volle Leistung über dem Erscheinungsbild der App | Vorausentwicklung erforderlich. <br>Höhere dev-Bemühungen zur Implementierung. |
