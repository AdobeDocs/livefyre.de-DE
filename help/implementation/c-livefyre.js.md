---
description: Die Core-Livefyre-Bibliothek, die für den Betrieb von Livefyre auf Ihrer Site verwendet wird.
seo-description: Die Core-Livefyre-Bibliothek, die für den Betrieb von Livefyre auf Ihrer Site verwendet wird.
seo-title: Livefyre. js
solution: Experience Manager
title: Livefyre. js
uuid: 7 b 3 eca 57-d 5 e 8-416 d-badf-a 9 c 51 d 10 dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre. js {#livefyre-js}

Die Core-Livefyre-Bibliothek, die für den Betrieb von Livefyre auf Ihrer Site verwendet wird.

`Livefyre.js` ist die Core-Bibliothek, die Sie auf jeder Livefyre-fähigen Webseite installieren können. Es definiert das globale `window.Livefyre` Objekt und eine einzelne öffentliche Methode, `Livefyre.require`die zum Laden anderer Livefyre-javascript-Bibliotheken verwendet werden kann, die die [Einbettung von Livefyre-Apps unterstützen](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), die [Integration Ihres Authentifizierungsanbieters mit Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) und mehr.

## Zu Ihrer Site hinzufügen {#section_cst_twg_xz}

Fügen Sie der Webseite oder Website-Vorlage das folgende `<script>` Tag hinzu. Falls möglich, fügen Sie ihn dem `<head>` Abschnitt Ihres HTML-Dokuments hinzu, damit es schnell geladen wird.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Dieses Skript bettet eine sehr kleine (~ 1 Kb) Datei mit dem Namen Livefyre. js ein, die dann die aktuelle Version von Livefyre. js über dem Protokoll lädt, mit dem Ihre Webseite (HTTP oder HTTPS) aufgerufen wurde.

## Livefyre. erforderlich {#section_ipq_hwg_xz}

`Livefyre.require` ist ein benutzerdefinierter javascript Module Loader wie [curl. js](https://github.com/cujojs/curl) oder [requirejs](https://requirejs.org/). Sie kann verwendet werden, um die meisten von Livefyre veröffentlichten Pakete zu laden, und bietet einen praktischen und intuitiven Integrationspfad.

Barrierefreie Pakete werden `Livefyre.require` mit [der Semantic Versioning](https://semver.org/)versioniert. Pakete können in einer bestimmten Version oder in verschiedenen Versionen erforderlich sein, damit Ihre Webseite automatisch von neuen Bugfixes profitieren kann. Dies bietet Ihnen Flexibilität bei der Integration von Livefyre auf Ihrer Site. Es gibt drei Stufen von Versionen, mit `Livefyre.require`denen Sie arbeiten können.

* **package-name # 1:** Pin in Hauptversion v 1 Sie erhalten alle neuen Updates, die eine abwärtskompatible API gewährleisten. Veröffentlichen Sie eine Hauptversion, um Fehlerbehebungen und Verbesserungen an der Funktionalität dieser Version zu erhalten.
* **package-name # 1.1:** Pin in kleinere Version v 1.1. Sie erhalten alle Bugfixes für diese Nebenversion. Der Livefyre Engineering bugt immer die nebenversion eines Pakets ein, wenn sich sein Standardverhalten oder Funktionsbereich auf eine Weise ändert, die ein neues, unerwartetes Verhalten auf Ihrer Webseite verursachen kann. Veröffentlichen Sie eine kleinere Version, wenn Sie automatisierte Fehlerbehebungen erhalten möchten, aber keine zusätzlichen Funktionen oder Änderungen am Standardverhalten.
* **package-name # 1.1.1:** Pin in Patch Version v 1.1.1. Das Verhalten dieser Einbettung ändert sich nie, selbst wenn Bugfixes vorhanden sind. Verankern Sie eine Patch-Version, wenn Sie umfangreiche CSS-Anpassungen für Ihre Site verwenden, die von der Markierungsstruktur eines Pakets abhängen, oder wenn Sie andere Gründe haben, dass die Livefyre-Version, die Sie ausführen, in keiner Weise geändert wird.

Eine Beispielintegration könnte `Livefyre.require` wie folgt aussehen:

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

Wondering which Livefyre JavaScript packages are available through `Livefyre.require`? Sie können immer eine aktuelle Liste der unterstützten Pakete und der neuesten Versionen finden: [packages.html](https://cdn.livefyre.com/packages.html).

## Testen von Vorabversionen von Paketen {#section_pgm_dpg_xz}

Manchmal möchten Sie eventuell eine bevorstehende Version eines Livefyre-Pakets testen, um sicherzustellen, dass es auf Ihrer Website funktioniert oder dass eine Funktion getestet wird, die auf Anforderung entwickelt wird. Zusätzlich zur Verwendung eines Semantic-Versionsbereichs kann die UAT-Umgebung der Vorabversion angegeben werden.

Folgendes würde zum Beispiel die UAT-Version von `fyre.conv`, die Kommentare, Live Blog und Chat-Anwendungen erfordern.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
