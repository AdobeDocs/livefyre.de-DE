---
description: Sie können einen Benutzer über die Konsole während der Integration und
  beim Testen protokollieren, um die Autorisierung zu debuggen.
seo-description: Sie können einen Benutzer über die Konsole während der Integration
  und beim Testen protokollieren, um die Autorisierung zu debuggen.
seo-title: Debugging-Authentifizierung
solution: Experience Manager
title: Debugging-Authentifizierung
uuid: fb 0 c 7396-190 e -4 dc 9-bf 26-23 dde 9 efd 45 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Debugging-Authentifizierung{#debugging-auth-delegate}

Sie können einen Benutzer über die Konsole während der Integration und beim Testen protokollieren, um die Autorisierung zu debuggen.

Melden Sie einen Benutzer über die Konsole mit folgendem `auth.authenticate` Token (Token) und übergeben Sie ein Livefyre-Benutzertoken, um Benutzer auf der Seite zu authentifizieren.

Sie können auch das oben aufgeführte Beispiel ändern und das folgende Codefragment in Ihrem javascript hinzufügen, um einen Benutzer schnell in Livefyre zu protokollieren (eine Referenz muss auf die Authentifizierung verweisen).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

