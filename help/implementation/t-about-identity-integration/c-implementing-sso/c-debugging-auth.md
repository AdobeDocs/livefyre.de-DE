---
description: Sie können einen Benutzer während der Integration und während des Tests über die Konsole anmelden, um die Autorisierung zu debuggen.
seo-description: Sie können einen Benutzer während der Integration und während des Tests über die Konsole anmelden, um die Autorisierung zu debuggen.
seo-title: Debuggen des Auth-Delegates
solution: Experience Manager
title: Debuggen des Auth-Delegates
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Debuggen des Auth-Delegates{#debugging-auth-delegate}

Sie können einen Benutzer während der Integration und während des Tests über die Konsole anmelden, um die Autorisierung zu debuggen.

Melden Sie sich mit dem folgenden `auth.authenticate` (Token) über die Konsole an und übergeben Sie ein Livefyre-Benutzertoken, um Benutzer auf der Seite zu authentifizieren.

Sie können auch das oben gezeigte Beispiel ändern und das folgende Codefragment in Ihrem JavaScript einfügen, um einen Benutzer schnell bei Livefyre anzumelden (eine Referenz zu auth ist erforderlich).

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

