---
description: Um einen Benutzer mit Livefyre über einen Fluss zu authentifizieren, der nicht von einer Livefyre-App ausgelöst wird, empfiehlt Livefyre, die forAnyAuthentication-Methode für das AuthDelegate-Objekt zu implementieren.
seo-description: Um einen Benutzer mit Livefyre über einen Fluss zu authentifizieren, der nicht von einer Livefyre-App ausgelöst wird, empfiehlt Livefyre, die forAnyAuthentication-Methode für das AuthDelegate-Objekt zu implementieren.
seo-title: Implementierung der SSO
solution: Experience Manager
title: Implementierung der SSO
uuid: c96d456c-b1ac-40e0-8d18-224652b9697f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '218'
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

