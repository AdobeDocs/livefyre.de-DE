---
description: Um einen Benutzer mit Livefyre über einen Fluss zu authentifizieren,
  der nicht durch eine Livefyre-App ausgelöst wird, empfiehlt Livefyre, dass Sie die
  foreachauthentication-Methode für Ihr authdelegate-Objekt implementieren.
seo-description: Um einen Benutzer mit Livefyre über einen Fluss zu authentifizieren,
  der nicht durch eine Livefyre-App ausgelöst wird, empfiehlt Livefyre, dass Sie die
  foreachauthentication-Methode für Ihr authdelegate-Objekt implementieren.
seo-title: Implementierung von SSO
solution: Experience Manager
title: Implementierung von SSO
uuid: c 96 d 456 c-b 1 ac -40 e 0-8 d 18-224652 b 9697 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Implementierung von SSO{#implementing-sso}

Um einen Benutzer mit Livefyre über einen Fluss zu authentifizieren, der nicht durch eine Livefyre-App ausgelöst wird, empfiehlt Livefyre, dass Sie die foreachauthentication-Methode für Ihr authdelegate-Objekt implementieren.

Dies wird aufgerufen, wenn das `authDelegate` Weitergereicht an `auth.delegate`und wird eine Authentifizierungsfunktion übergeben, die mehrmals übergeben werden kann. Diese Methode bietet eine Inversion der Authentifizierung für Authentifizierungsereignisse, damit sie `AuthDelegateobject` eigenständig gespeichert werden können, ohne dass eine globale Referenz auf Authentifizierung erforderlich ist.

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre basiert auf Benutzertoken, um die Authentifizierung zu koordinieren. Daher muss dieses Token von Ihrem Identitäts-Service zurückgegeben werden, um einen Benutzer mit Livefyre zu authentifizieren. Informationen zum Erstellen eines Livefyre-Benutzertokens finden Sie unter Erstellen eines Token für die Benutzerauthentifizierung.

>[!NOTE]
>
>Nach einer erfolgreichen Anmeldung erstellt die Authentifizierung eine Sitzung für den Benutzer und versucht, die Sitzung eines Benutzers beim Aktualisieren und Neuladen der Seite zu laden. `auth.logout()` wird diese Sitzung löschen. Dies bedeutet, dass es nicht notwendig ist, die Sitzung eines Benutzers unabhängig von der Autorisierung zu verwalten.

