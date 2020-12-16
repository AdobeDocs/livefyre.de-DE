---
description: Das Livefyre.js Auth-Paket stellt sicher, dass alle sozialen Komponenten auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken können.
seo-description: Das Livefyre.js Auth-Paket stellt sicher, dass alle sozialen Komponenten auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken können.
seo-title: Livefyre-Identität initialisieren
title: Livefyre-Identität initialisieren
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Livefyre-Identität initialisieren{#initialize-livefyre-identity}

Das Livefyre.js Auth-Paket stellt sicher, dass alle sozialen Komponenten auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken können.

Livefyre stellt ein `lfep-auth-delegate`-Paket bereit, das einen entsprechenden auth-Delegate für Sie bereitstellt. Auth muss ein AuthDelegate-Objekt zur Verfügung gestellt werden, das Authentifizierungsaktionen wie Anmeldung und Abmeldung durchführen kann.

1. hinzufügen Sie Livefyre.js auf Ihre Webseite.
1. Um Auth anzuweisen, diese Aktionen an Livefyre Identity zu delegieren, fügen Sie Folgendes hinzu:

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
