---
seo-title: App einbetten
solution: Experience Manager
title: App einbetten
uuid: e 75 caf 0 e -04 ea -4 b 04-89 ed-fea 1183 ecf 63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# App einbetten{#embed-an-app}

Fügen Sie mithilfe der Embed-Codestruktur von Livefyre. js Livefyre-Apps Ihren Webseiten hinzu.

Diese Dokumentation ist für eine technische Zielgruppe gedacht. Für [nicht technische Informationen zu Apps](/help/using/c-about-apps/c-about-apps.md).

In diesem Abschnitt wird die Codestruktur beschrieben, die Sie in Ihre Seitenvorlage aufnehmen müssen, um Livefyre-Apps in Ihre Website einzubetten.

1. Erstellen Sie eine.html datei mit einem Livefyre-Platzhalter.

   Erstellen Sie eine neue.html Datei im Texteditor Ihrer Wahl. Erstellen Sie ein Platzhalterelement Livefyre `<div>` , in das die App eingebettet wird.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Schließen Sie die Bibliothek &quot;Livefyre. js&quot; ein.

   Schließen Sie dann die Livefyre JS-Bibliothek ein. Platzieren Sie die folgende Referenz in ein `<script>` Element in Ihrem `<head>` Element. Öffnen Sie dann Ihre Seite in einem Browser und verwenden Sie den Webinspektor Ihres Browsers, um zu bestätigen, dass Livefyre geladen wird.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Erstellen Sie die Livefyre-App.

   Verwenden `Livefyre.require` Sie zum Erstellen von Core- und SDK-Apps die Livefyre-Pakete, die Sie verwenden möchten.

   1. Erstellen einer Core-App.

      Verwenden Sie zum Erstellen einer Core-App (Kommentare, Live-Blog oder Chat) die folgende Struktur:

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Erstellen einer SDK-App.

      Um eine SDK-App wie Media Wall oder Feed zu erstellen, verwenden Sie die folgende Struktur:

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

      Weitere [Informationen zu bestimmten Apps](/help/using/c-about-apps/c-about-apps.md)finden Sie unter. Es wird empfohlen, auf die neueste Hauptversion des Pakets zu dringen (die über [Livefyre. erforderlich gefunden werden kann](https://cdn.livefyre.com/packages.html)), um unerwartete fehlerhafte Integrationen zu vermeiden.

Weiter: Fügen Sie Ihrer Site Authentifizierung hinzu, damit Ihre Benutzer Kommentare posten können.
