---
description: 'null '
seo-description: 'null '
seo-title: Verwenden von Livefyre mit anderen Analysetools
solution: Experience Manager
title: Verwenden von Livefyre mit anderen Analysetools
uuid: 26c835f6-aced-41f7-aabe-418afce8a829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# Verwenden Sie Livefyre mit dem anderen Analysetool{#use-livefyre-with-other-analytics-tool}

Mit den Analysetools können Sie Daten zu Benutzerinteraktionen mit Livefyre-Apps erfassen. Sie können Adobe Analytics oder ein Tool Ihrer Wahl verwenden.

Um Livefyre mit einem Tool Ihrer Wahl (nicht Adobe Analytics) zu verwenden, befolgen Sie das auf dieser Seite beschriebene Verfahren.

## Schritt 1: Einrichten des Ereignis-Handlers {#section_ngm_gzl_pdb}

Richten Sie einen Ereignis-Handler auf Seiten ein, auf denen Sie Livefyre-Apps verwenden. Auf diese Weise können Sie Daten aus den Apps auf dieser Seite erfassen, die Sie für die Analyse verwenden können.

hinzufügen Sie Livefyre.js auf eine Seite, um den Ereignis-Handler einzurichten. Livefyre.js wird asynchron geladen. Um die Dateigröße zu reduzieren und die Ladeleistung zu verbessern, stehen die Analysen nicht sofort zur Verfügung. Sie müssen das Analytics-Objekt abfragen, bis Daten verfügbar sind. Platzieren Sie dieses Skript an einer beliebigen Stelle auf der Seite oder bündeln Sie es in Ihren eigenen kompilierten Skripten.

```
/** 
 * Handler for Livefyre analytics batch events. 
 * @param {Array.<string>} events Array of events that have been fired since 
 * the last batch send. 
 */ 
function analyticsHandler(events) { 
  // Send to analytics 
  console.log(events); 
} 
 
var attempts = 0; 
 
function pollForAnalytics() { 
  if (Livefyre && Livefyre.analytics) { 
    Livefyre.analytics.addHandler(analyticsHandler); 
    return; 
  } 
  if (attempts === 10) { 
    return; 
  } 
  attempts++; 
  setTimeout(pollForAnalytics, 500); 
} 
 
pollForAnalytics(); 
```

## Schritt 2: Implementierungshandler-Funktion

Sobald die Livefyre.analytics-Funktion auf der Seite verfügbar ist, implementieren Sie die Funktion analyticsHandler, um die empfangenen Ereignis an den Analytics-Provider Ihrer Wahl zu senden.

1. Der Analytics-Handler empfängt ein Array von Ereignissen, die einzeln oder als Batch durchlaufen und gesendet werden müssen, wenn der Anbieter dies unterstützt.
1. Ordnen Sie die vom Handler empfangenen Ereignis-Daten einem Format zu, das vom Analytics-Anbieter benötigt wird.
1. Senden Sie die Daten an Ihren Analytics-Anbieter.

