---
description: Verwenden Sie Livefyre.js, um eine seitenweite Authentifizierung für Ihre Livefyre-Apps hinzuzufügen.
seo-description: Verwenden Sie Livefyre.js, um eine seitenweite Authentifizierung für Ihre Livefyre-Apps hinzuzufügen.
seo-title: Hinzufügen einer Authentifizierung zu einer App mit Livefyre.js
solution: Experience Manager
title: Hinzufügen einer Authentifizierung zu einer App mit Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# Hinzufügen einer Authentifizierung zu einer App mit Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Verwenden Sie Livefyre.js, um eine seitenweite Authentifizierung für Ihre Livefyre-Apps hinzuzufügen.

`Livefyre.js Aut`h ist ein von Livefyre entwickeltes JavaScript-Paket, das allen Apps auf Ihrer Website die gemeinsame Nutzung einer Authentifizierungsintegration ermöglicht. Mit Auth können Sie festlegen, wie sich Benutzer registrieren, anmelden und abmelden sollen, indem Sie diese Datenströme an ein von Ihnen definiertes AuthDelegate-Objekt delegieren.

## Schritt 1: Aktivieren der Authentifizierung für eine Seite {#section_pgp_jtt_bbb}

Verwenden Sie diese Option, `Livefyre.js` um die Authentifizierung für eine Seite zu aktivieren, damit sich Benutzer mit Ihrem vorhandenen Authentifizierungssystem anmelden und mit Apps interagieren können.

1. Um die Authentifizierung auf einer Seite zu aktivieren, fügen Sie `Livefyre.js` das Element *&lt;head&gt;* Ihrer Webseite oder Website-Vorlage hinzu.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Aktivieren Sie `Livefyre.require` die Authentifizierung. Die Verwendung `Livefyre.require` ähnelt der Verwendung von "erfordern", um andere Pakete aufzurufen. Der Integrationscode, für den auth erforderlich ist, sieht wie folgt aus:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Schritt 2: AuthDelegate registrieren {#section_oqm_15t_bbb}

Um die Authentifizierung zu aktivieren, erstellen Sie eine `AuthDelegate` und übergeben Sie sie an die `Livefyre.js` Authentifizierung.

Ein `AuthDelegate` Objekt, das Sie definieren, bestimmt, wie Benutzer sich anmelden, abmelden und Profile anzeigen.

1. Erstellen Sie eine `AuthDelegate`. Die Art und Weise, wie Sie eine `AuthDelegate` erstellen, hängt von Ihrem Identitätsanbieter ab. Detailliertere Anweisungen finden Sie unter Identitätsintegration.

1. Übergeben Sie die `AuthDelegate` an `Livefyre.js` Authentifizierung. Am einfachsten `AuthDelegate` protokolliert derselbe Benutzer, wenn ein Benutzer die Methode zur delegierten Anmeldung von einer App auslöste:

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

Synchronisieren Sie die Benutzerprofilinformationen zwischen Livefyre und Ihrem Identitätsanbieter.

Sie müssen Ihre Benutzerprofilinformationen zwischen Livefyre und Ihrem Identitäts-Provider synchronisieren. Weitere Informationen finden Sie unter Integration von [Janrain Capture](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
