---
description: Verwenden Sie Livefyre. js, um für Ihre Livefyre-Apps seitenweite Authentifizierung hinzuzufügen.
seo-description: Verwenden Sie Livefyre. js, um für Ihre Livefyre-Apps seitenweite Authentifizierung hinzuzufügen.
seo-title: Authentifizierung zu einer App mit Livefyre. js hinzufügen
solution: Experience Manager
title: Authentifizierung zu einer App mit Livefyre. js hinzufügen
uuid: b 7 c 61 e 07-e 341-45 d 7-9112-c 50155 e 38 f 1 d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# Authentifizierung zu einer App mit Livefyre. js hinzufügen{#add-authetication-to-an-app-using-livefyre-js}

Verwenden Sie Livefyre. js, um für Ihre Livefyre-Apps seitenweite Authentifizierung hinzuzufügen.

`Livefyre.js Aut`h ist ein javascript-Paket, das von Livefyre entwickelt wurde und alle Apps auf Ihrer Website zur Freigabe einer einzelnen Authentifizierungsintegration freigibt. Mit Auth können Sie festlegen, wie Ihre Benutzer sich registrieren, sich anmelden und abmelden müssen, indem Sie diese an ein authdelegobjekt delegieren, das Sie definieren.

## Schritt 1: Authentifizierung für eine Seite aktivieren {#section_pgp_jtt_bbb}

Verwenden `Livefyre.js` Sie diese Option, um die Authentifizierung für eine Seite zu aktivieren, damit Benutzer sich anmelden und mit Apps mit Ihrem bestehenden Authentifizierungssystem interagieren können.

1. Um die Authentifizierung auf einer Seite zu aktivieren, fügen `Livefyre.js`*Sie dem &lt; head &gt;* -Element Ihrer Webseite oder Website-Vorlage hinzu.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Zur `Livefyre.require` Aktivierung der Authentifizierung. Die Verwendung `Livefyre.require` ist ähnlich wie die Verwendung des erforderlichen Aufrufs anderer Pakete. Der Integrationscode, der authentifiziert werden muss, sieht wie folgt aus:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Schritt 2: Authdelegate registrieren {#section_oqm_15t_bbb}

Um die Authentifizierung zu aktivieren, müssen `AuthDelegate` Sie sie an `Livefyre.js` die Authentifizierung übergeben.

Bei einem `AuthDelegate` Objekt handelt es sich um ein Objekt, das festlegt, wie Benutzer sich anmelden, abmelden und anzeigen können.

1. Erstellen Sie eine `AuthDelegate`. Die Art und Weise, wie Sie ein Projekt erstellen, `AuthDelegate` hängt von Ihrem Identitäts-Provider ab. Detaillierte Anweisungen finden Sie unter Identitätsintegration.

1. Übergeben Sie die `AuthDelegate` an `Livefyre.js` die Authentifizierung. Die einfachste `AuthDelegate` Protokollierung protokolliert denselben Benutzer, wenn ein Benutzer die delegierten Anmeldungsmethoden aus einer App ausgelöst hat:

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## Schritt 3: Benutzerdaten synchronisieren {#section_u4m_j5t_bbb}

Synchronisieren Sie die Benutzerprofilinformationen zwischen Livefyre und Ihrem Identitäts-Provider.

Sie müssen Ihre Benutzerprofilinformationen zwischen Livefyre und Ihrem Identitäts-Provider synchronisieren. Weitere Informationen finden Sie unter [Janrain Capture Integration](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
