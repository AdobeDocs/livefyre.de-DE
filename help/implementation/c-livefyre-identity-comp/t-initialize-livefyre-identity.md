---
description: Das Auth-Paket von Livefyre. js stellt sicher, dass alle sozialen Komponenten
  auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken.
seo-description: Das Auth-Paket von Livefyre. js stellt sicher, dass alle sozialen
  Komponenten auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken.
seo-title: Livefyre-Identität initialisieren
title: Livefyre-Identität initialisieren
uuid: 9365 d 827-2734-4 a 84-bfe 7-9 be 573 b 2 b 03 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre-Identität initialisieren{#initialize-livefyre-identity}

Das Auth-Paket von Livefyre. js stellt sicher, dass alle sozialen Komponenten auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken.

Livefyre stellt ein `lfep-auth-delegate` Paket bereit, das eine geeignete Authentifizierung für Sie vornimmt. Auth muss ein authdelegobjekt zur Durchführung von Authentifizierungsaktionen wie Anmeldung und Abmeldung bereitstellen.

1. Fügen Sie Ihrer Webseite Livefyre. js hinzu.
1. Um Auth mitzuteilen, dass diese Aktionen an Livefyre-Identität delegiert werden sollen, fügen Sie Folgendes hinzu:

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
