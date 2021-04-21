---
title: Eine App einbetten
description: Eine App einbetten
exl-id: 12f75093-1b4d-4cf1-8593-dbd17ff33872
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Eine App{#embed-an-app} einbetten

hinzufügen Sie Livefyre-Apps mithilfe der Livefyre.js-Einbettungscode-Struktur auf Ihre Webseiten.

Diese Dokumentation ist für eine technische Audience gedacht. Für [nicht technische Informationen über Apps](/help/using/c-about-apps/c-about-apps.md).

In diesem Abschnitt wird die Codestruktur beschrieben, die Sie in Ihre Seitenvorlage aufnehmen müssen, um Livefyre-Apps auf Ihrer Site einzubetten.

1. Erstellen Sie eine HTML-Datei mit einem Livefyre-Platzhalter.

   Erstellen Sie eine neue HTML-Datei im Texteditor Ihrer Wahl. Erstellen Sie ein Platzhalter für das Element Livefyre `<div>`, in das die App eingebettet wird.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Schließen Sie die Bibliothek Livefyre.js ein.

   Schließen Sie dann die Livefyre JS-Bibliothek ein. Fügen Sie den folgenden Verweis in ein `<script>`-Element im `<head>`-Element ein. Öffnen Sie dann Ihre Seite in einem Browser und bestätigen Sie mit dem Webinspektor Ihres Browsers, dass Livefyre geladen wurde.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Erstellen Sie die Livefyre-App.

   Verwenden Sie `Livefyre.require`, um sowohl Core- als auch SDK-Apps zu erstellen, indem Sie die Livefyre-Pakete, die Sie verwenden möchten, übergeben.

   1. Erstellen Sie eine Core-App.

      Um eine Core-App (Kommentare, Live-Blog oder Chat) zu erstellen, verwenden Sie die folgende Struktur:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Erstellen Sie eine SDK-App.

      Verwenden Sie zum Erstellen einer SDK-App wie Media Pinnwand oder Feed die folgende Struktur:

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      Siehe [weitere Informationen zu bestimmten Apps](/help/using/c-about-apps/c-about-apps.md). Es wird empfohlen, die neueste Hauptversion des Pakets zu veröffentlichen (die über [Livefyre.require](https://cdn.livefyre.com/packages.html) zu finden ist), um unerwartete fehlerhafte Integrationen zu vermeiden.

Weiter: hinzufügen Authentifizierung für Ihre Site, damit Ihre Benutzer Kommentare posten können.
