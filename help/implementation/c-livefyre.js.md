---
description: Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.
seo-description: Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre.js {#livefyre-js}

Die Core Livefyre-Bibliothek, die verwendet wird, um Livefyre auf Ihrer Site zu aktivieren.

`Livefyre.js` ist die Kernbibliothek, die Sie auf jeder Livefyre-fähigen Webseite installieren können. Es definiert das globale `window.Livefyre` Objekt und eine einzelne öffentliche Methode, `Livefyre.require`die zum Laden anderer Livefyre JavaScript-Bibliotheken verwendet werden kann, die beim [Einbetten von Livefyre-Apps](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), der [Integration Ihres Authentifizierungsanbieters mit Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) und mehr helfen.

## Zur Site hinzufügen {#section_cst_twg_xz}

Fügen Sie Ihrer Webseite oder Website-Vorlage das folgende `<script>` Tag hinzu. Fügen Sie sie nach Möglichkeit dem `<head>` Abschnitt Ihres HTML-Dokuments hinzu, damit sie schnell geladen werden kann.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Dieses Skript wird eine sehr kleine Datei (~1 Kb) namens Livefyre.js scout einbetten, die dann die neueste Version von Livefyre.js über das Protokoll lädt, mit dem auf Ihre Webseite zugegriffen wurde (HTTP oder HTTPS).

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` ist ein benutzerdefinierter JavaScript-Modul-Lader wie [curl.js](https://github.com/cujojs/curl) oder [RequireJS](https://requirejs.org/). Es kann zum Laden der meisten von Livefyre veröffentlichten Pakete verwendet werden und stellt einen bequemen und intuitiven Integrationspfad dar.

Pakete, auf die zugegriffen werden `Livefyre.require` kann, werden mit [Semantic Versioning](https://semver.org/)versioniert. Pakete können für eine bestimmte Version oder eine Reihe von Versionen erforderlich sein, damit Ihre Webseite automatisch von neuen Bugfixes-Funktionen profitieren kann. Dadurch erhalten Sie Flexibilität bei der Integration von Livefyre in Ihre Site. Es gibt drei Stufen des Versionsinnings, mit denen Sie arbeiten können `Livefyre.require`.

* **** package-name#1: An Hauptversion v1 anheften. Sie erhalten alle neuen Aktualisierungen, die eine abwärtskompatible API beibehalten. Schließen Sie eine Hauptversion an, um Fehlerbehebungen und kleinere Funktionsverbesserungen für diese Version zu erhalten.
* **** package-name#1.1: An Nebenversion v1.1 anheften. Sie erhalten alle Bugfixes zu dieser kleineren Version. Livefyre Engineering stellt die Nebenversion eines Pakets immer auf den Kopf, wenn sich das Standardverhalten oder der Funktionsumfang so ändert, dass neue, unerwartete Verhaltensweisen auf Ihrer Webseite entstehen können. Schließen Sie eine Nebenversion an, wenn Sie automatische Fehlerbehebungen erhalten möchten, jedoch keine zusätzliche Funktionalität oder Änderungen am Standardverhalten.
* **** package-name#1.1.1: An Patch-Version v1.1.1 anheften. Das Verhalten dieser Einbettung ändert sich nie, selbst wenn es Fehlerbehebungen gibt. Pinnen Sie an eine Patch-Version, wenn Sie umfangreiche CSS-Anpassungen für Ihre Site vornehmen, die von der möglicherweise geänderten Markup-Struktur eines Pakets abhängen, oder wenn Sie andere Gründe haben, vorzuziehen, dass sich die ausgeführte Livefyre-Version in keiner Weise ändert.

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

Welche Livefyre JavaScript-Pakete stehen zur Verfügung `Livefyre.require`? Eine aktuelle Liste der unterstützten Pakete und der aktuellen Versionen finden Sie hier: [packages.html](https://cdn.livefyre.com/packages.html).

## Testen von Versionen von Paketen vor der Veröffentlichung {#section_pgm_dpg_xz}

Manchmal ist es sinnvoll, eine bevorstehende Version eines Livefyre-Pakets zu testen, um sicherzustellen, dass es auf Ihrer Website funktioniert, oder um eine Funktion zu akzeptieren, die auf Ihre Anfrage hin entwickelt wird. Zusätzlich zum Bereich Semantic Version kann die UAT-Umgebung für die Vorabversion angegeben werden.

Zum Beispiel würde Folgendes die UAT-Version der Anwendungen `fyre.conv`, Kommentare, Live-Blog und Chat erfordern.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
