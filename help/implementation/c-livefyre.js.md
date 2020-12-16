---
description: Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.
seo-description: Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# Livefyre.js {#livefyre-js}

Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.

`Livefyre.js` ist die Kernbibliothek, die Sie auf jeder Livefyre-fähigen Webseite installieren können. Es definiert das globale `window.Livefyre`-Objekt und eine einzelne öffentliche Methode, `Livefyre.require`, die zum Laden anderer Livefyre-JavaScript-Bibliotheken verwendet werden kann, die mit [Einbetten von Livefyre-Apps](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [Integration Ihres Authentifizierungsanbieters mit Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) und mehr helfen.

## hinzufügen auf Ihrer Site {#section_cst_twg_xz}

hinzufügen Sie das folgende `<script>`-Tag in Ihre Webseite oder Website-Vorlage ein. Wenn möglich, fügen Sie es zum Abschnitt `<head>` Ihres HTML-Dokuments hinzu, damit es schnell geladen wird.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Dieses Skript wird eine sehr kleine Datei (~1 Kb) namens Livefyre.js scout einbetten, die dann die neueste Version von Livefyre.js über das Protokoll lädt, mit dem auf Ihre Webseite zugegriffen wurde (HTTP oder HTTPS).

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` ist ein benutzerdefinierter JavaScript-Modul-Lader wie  [curl.](https://github.com/cujojs/curl) jsor  [RequireJS](https://requirejs.org/). Es kann zum Laden der meisten von Livefyre veröffentlichten Pakete verwendet werden und stellt einen bequemen und intuitiven Integrationspfad dar.

Pakete, auf die über `Livefyre.require` zugegriffen werden kann, werden mit [Semantic Versioning](https://semver.org/) versioniert. Pakete können für eine bestimmte Version oder eine Reihe von Versionen erforderlich sein, damit Ihre Webseite automatisch von neuen Bugfixes-Funktionen profitieren kann. Dadurch erhalten Sie Flexibilität bei der Integration von Livefyre in Ihre Site. Es gibt drei Stufen des Versionsinnings, die Sie mit `Livefyre.require` verwenden können.

* **package-name#1:** In Hauptversion v1 veröffentlichen. Sie erhalten alle neuen Aktualisierungen, die eine abwärtskompatible API beibehalten. Schließen Sie eine Hauptversion an, um Fehlerbehebungen und kleinere Funktionsverbesserungen für diese Version zu erhalten.
* **package-name#1.1:** In Nebenversion v1.1 veröffentlichen Sie erhalten alle Bugfixes zu dieser kleineren Version. Livefyre Engineering stellt die Nebenversion eines Pakets immer auf den Kopf, wenn sich das Standardverhalten oder der Funktionsumfang so ändert, dass neue, unerwartete Verhaltensweisen auf Ihrer Webseite entstehen können. Schließen Sie eine Nebenversion an, wenn Sie automatische Fehlerbehebungen erhalten möchten, jedoch keine zusätzliche Funktionalität oder Änderungen am Standardverhalten.
* **package-name#1.1.1:** Pin to patch version v1.1.1. Das Verhalten dieser Einbettung ändert sich nie, selbst wenn es Fehlerbehebungen gibt. Pinnen Sie an eine Patch-Version, wenn Sie umfangreiche CSS-Anpassungen für Ihre Site vornehmen, die von der möglicherweise geänderten Markup-Struktur eines Pakets abhängen, oder wenn Sie andere Gründe haben, vorzuziehen, dass sich die ausgeführte Livefyre-Version in keiner Weise ändert.

Eine Beispielintegration mit `Livefyre.require` könnte wie folgt aussehen:

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## Verfügbare Pakete {#section_ygd_dwg_xz}

Sie fragen sich, welche Livefyre JavaScript-Pakete über `Livefyre.require` verfügbar sind? Eine aktuelle Liste der unterstützten Pakete und der jeweils aktuellen Versionen finden Sie hier: [packages.html](https://cdn.livefyre.com/packages.html).

## Testen von Versionen vor der Veröffentlichung von Paketen {#section_pgm_dpg_xz}

Manchmal ist es sinnvoll, eine bevorstehende Version eines Livefyre-Pakets zu testen, um sicherzustellen, dass es auf Ihrer Website funktioniert, oder um eine Funktion zu akzeptieren, die auf Ihre Anfrage hin entwickelt wird. Zusätzlich zum Bereich Semantic Version kann die UAT-Umgebung für die Vorabversion angegeben werden.

Für Folgendes ist beispielsweise die UAT-Version von `fyre.conv`, die Anwendungen Kommentare, Live-Blog und Chat erforderlich.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
