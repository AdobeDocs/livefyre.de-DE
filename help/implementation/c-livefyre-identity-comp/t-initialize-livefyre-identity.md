---
description: Das Livefyre.js Auth-Paket stellt sicher, dass alle sozialen Komponenten auf Ihrer Seite eine einzige Authentifizierungsintegration entdecken können.
title: Livefyre-Identität initialisieren
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
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
