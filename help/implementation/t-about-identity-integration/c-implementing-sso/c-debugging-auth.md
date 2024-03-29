---
description: Sie können einen Benutzer während der Integration und während des Tests über die Konsole anmelden, um die Autorisierung zu debuggen.
title: Debuggen des Auth-Delegates
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
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
