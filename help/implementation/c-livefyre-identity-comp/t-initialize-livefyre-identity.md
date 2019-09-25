---
description: Das Livefyre.js Auth-Paket stellt sicher, dass alle sozialen Komponenten auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken können.
seo-description: Das Livefyre.js Auth-Paket stellt sicher, dass alle sozialen Komponenten auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken können.
seo-title: Livefyre-Identität initialisieren
title: Livefyre-Identität initialisieren
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre-Identität initialisieren{#initialize-livefyre-identity}

Das Livefyre.js Auth-Paket stellt sicher, dass alle sozialen Komponenten auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken können.

Livefyre bietet ein `lfep-auth-delegate` Paket, das einen entsprechenden Auth-Delegate für Sie bereitstellt. Auth muss ein AuthDelegate-Objekt zur Verfügung gestellt werden, das Authentifizierungsaktionen wie Anmeldung und Abmeldung durchführen kann.

1. Fügen Sie Ihrer Webseite Livefyre.js hinzu.
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
