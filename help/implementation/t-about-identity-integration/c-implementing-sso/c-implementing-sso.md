---
description: Um einen Benutzer mit Livefyre über einen Fluss zu authentifizieren, der nicht von einer Livefyre-App ausgelöst wird, empfiehlt Livefyre, die forAnyAuthentication-Methode für das AuthDelegate-Objekt zu implementieren.
title: Implementierung der SSO
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Implementierung von SSO{#implementing-sso}

Um einen Benutzer mit Livefyre über einen Fluss zu authentifizieren, der nicht von einer Livefyre-App ausgelöst wird, empfiehlt Livefyre, die forAnyAuthentication-Methode für das AuthDelegate-Objekt zu implementieren.

Dies wird aufgerufen, wenn `authDelegate` an `auth.delegate` übergeben wird, und es wird eine Authentifizierungsfunktion übergeben, die mehrmals übergeben werden kann. Diese Methode stellt eine Inversion der Steuerung für Authentifizierungs-Ereignis bereit, sodass `AuthDelegateobject` unabhängig voneinander sein kann, ohne dass ein globaler Verweis auf auth erforderlich ist.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre nutzt zur Koordination der Authentifizierung Token. Daher muss dieses Token von Ihrem Identitätsdienst zurückgegeben werden, um einen Benutzer bei Livefyre zu authentifizieren. Informationen zum Erstellen eines Livefyre-Benutzertokens finden Sie unter Erstellen eines Benutzerauthentifizierungstokens.

>[!NOTE]
>
>Nach erfolgreicher Anmeldung erstellt auth eine Sitzung für den Benutzer und versucht, die Sitzung des Benutzers zu laden, wenn die Seite aktualisiert und neu geladen wird. `auth.logout()` wird diese Sitzung beenden. Das bedeutet, dass die Sitzung eines Benutzers nicht unabhängig von der Autorisierung verwaltet werden muss.
