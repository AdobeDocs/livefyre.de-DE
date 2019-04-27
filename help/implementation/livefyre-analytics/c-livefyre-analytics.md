---
description: 'null '
seo-description: 'null '
seo-title: Verwenden von Livefyre mit anderen Analytics-Werkzeugen
solution: Experience Manager
title: Verwenden von Livefyre mit anderen Analytics-Werkzeugen
uuid: 26 c 835 f 6-aced -41 f 7-aabe -418 afce 8 a 829
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Verwenden von Livefyre mit anderen Analytics-Werkzeugen{#use-livefyre-with-other-analytics-tool}

Sie können Analysetools verwenden, um Daten über Benutzerinteraktionen mit Livefyre-Apps zu sammeln. Sie können Adobe Analytics oder ein Tool Ihrer Wahl verwenden.

Um Livefyre mit einem Tool Ihrer Wahl (nicht Adobe Analytics) zu verwenden, befolgen Sie das auf dieser Seite beschriebene Verfahren.

## Schritt 1: Ereignishandler einrichten {#section_ngm_gzl_pdb}

Richten Sie einen Ereignishandler auf Seiten ein, auf denen Sie Livefyre-Apps verwenden. Auf diese Weise können Sie Daten aus den Apps erfassen, die Sie für die Analyse verwenden können.

Fügen Sie Livefyre. js einer Seite hinzu, um den Ereignishandler einzurichten. Livefyre. js wird asynchron geladen. Um die Dateigröße zu reduzieren und die Ladeleistung zu verbessern, sind die Analysen nicht sofort verfügbar. Sie müssen das Analytics-Objekt abrufen, bis die Daten verfügbar sind. Platzieren Sie dieses Skript an einer beliebigen Stelle auf der Seite oder bündeln Sie es in Ihren eigenen kompilierten Skripten.

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

## Schritt 2: Handler-Funktion implementieren

Sobald die Livefyre. analytics-Funktionen auf der Seite verfügbar sind, implementieren Sie die Funktion analyticshandler, um die empfangenen Ereignisse an den Analytics-Provider Ihrer Wahl zu senden.

1. Der Analytics-Handler empfängt ein Array von Ereignissen, die durchlaufen und einzeln oder als Batch gesendet werden müssen, wenn Ihr Anbieter diese unterstützt.
1. Ordnen Sie die vom Handler empfangenen Ereignisdaten einem Format zu, das der Analytics-Anbieter benötigt.
1. Senden Sie die Daten an Ihren Analytics-Anbieter.

