---
description: Verwenden Sie Livefyre.js, um eine seitenweite Authentifizierung für Ihre Livefyre-Apps hinzuzufügen.
seo-description: Verwenden Sie Livefyre.js, um eine seitenweite Authentifizierung für Ihre Livefyre-Apps hinzuzufügen.
seo-title: hinzufügen einer App mithilfe von Livefyre.js
solution: Experience Manager
title: hinzufügen einer App mithilfe von Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# hinzufügen der Authentifizierung für eine App mit Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Verwenden Sie Livefyre.js, um eine seitenweite Authentifizierung für Ihre Livefyre-Apps hinzuzufügen.

`Livefyre.js Aut`h ist ein von Livefyre entwickeltes JavaScript-Paket, das allen Apps auf Ihrer Website die gemeinsame Nutzung einer Authentifizierungsintegration ermöglicht. Mit Auth können Sie festlegen, wie sich Ihre Benutzer registrieren, anmelden und abmelden sollen, indem Sie diese Datenströme an ein von Ihnen definiertes AuthDelegate-Objekt delegieren.

## Schritt 1: Aktivieren der Authentifizierung für eine Seite {#section_pgp_jtt_bbb}

Verwenden Sie `Livefyre.js`, um die Authentifizierung für eine Seite zu aktivieren, damit sich Benutzer mit Ihrem vorhandenen Authentifizierungssystem anmelden und mit Apps interagieren können.

1. Um die Authentifizierung auf einer Seite zu aktivieren, fügen Sie `Livefyre.js` zum *&lt;head>*-Element Ihrer Webseite oder Website-Vorlage hinzu.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Verwenden Sie `Livefyre.require`, um die Authentifizierung zu aktivieren. Die Verwendung von `Livefyre.require` ähnelt der Verwendung von &quot;erfordern&quot;, um andere Pakete aufzurufen. Der Integrationscode, für den auth erforderlich ist, sieht wie folgt aus:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Schritt 2: Registrieren eines AuthDelegate {#section_oqm_15t_bbb}

Um die Authentifizierung zu aktivieren, erstellen Sie eine `AuthDelegate` und übergeben Sie sie an `Livefyre.js`-Authentifizierung.

Ein `AuthDelegate` ist ein von Ihnen definiertes Objekt, das bestimmt, wie sich Benutzer anmelden, abmelden und Ansichten-Profil ausführen.

1. Erstellen Sie eine `AuthDelegate`. Die Art und Weise, wie Sie ein `AuthDelegate` erstellen, hängt von Ihrem Identitätsanbieter ab. Detailliertere Anweisungen finden Sie unter Integration von Identitäten.

1. Übergeben Sie die `AuthDelegate`-Authentifizierung an `Livefyre.js`. Der einfachste `AuthDelegate` meldet denselben Benutzer bei jeder Auslösung der delegierten Anmeldemethode aus einer App an:

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

Synchronisieren Sie die Benutzerdaten zwischen Livefyre und Ihrem Identitätsanbieter.

Sie müssen Ihre Benutzerdaten zwischen Livefyre und Ihrem Identitäts-Provider synchronisieren. Weitere Informationen finden Sie unter [Janrain Capture Integration](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
