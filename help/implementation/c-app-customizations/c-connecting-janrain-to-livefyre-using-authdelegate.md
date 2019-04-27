---
description: Livefyre. erforderlich ist ein Plugin, mit dem die Authentifizierung des Janrain Backplane-Bus aktiviert wird.
seo-description: Livefyre. erforderlich ist ein Plugin, mit dem die Authentifizierung des Janrain Backplane-Bus aktiviert wird.
seo-title: Verbinden von Janrain mit Livefyre mit authdelegate
title: Verbinden von Janrain mit Livefyre mit authdelegate
uuid: 9 d 56 e 3 f 4-960 a -4108-aab 5-2795 b 0 e 71 c 88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Verbinden von Janrain mit Livefyre mit authdelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre. erforderlich ist ein Plugin, mit dem die Authentifizierung des Janrain Backplane-Bus aktiviert wird.

Wenn eine Identitäts-/Anmeldungsnachricht auf dem Backplane-Kanal übertragen wird, wird auth. authenticate () für Sie mit dem Livefyre-Authentifizierungstoken des Benutzers aufgerufen. Sie müssen dennoch eine authdelegate implementieren.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>Das window. Backplane-Objekt muss auf Ihrer Seite definiert werden, bevor auth. plugin mit dem Livefyre-Backplane-Plugin aufgerufen wird. Um sicherzustellen, dass das Backplane-Objekt verfügbar ist, rufen Sie den Livefyre-Instanziierungscode aus einem onready-Rückruf auf. Wenden Sie sich an Ihren Janrain-Kontakt, um festzustellen, wann andere Anwendungen das Backplane-Objekt verwenden können.

Im Folgenden finden Sie einige Beispiele dafür, wie eine Authentifizierungsdelegation nach einer Janrain Capture-Integration sucht.

>[!NOTE]
>
>Ihre Authentifizierungsdelegation variiert je nach Ihrer Janrain-Instanz.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* Der Rückruf, der an die Anmeldemethode der Authentifizierungsmethode übergeben wird
* Der Verweis auf Ihre Janrain-Erfassungsvariable.
* : Ein Verweis auf Ihr Backplane-Objekt.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

Abmelden

* **Finishlogout:** Der Rückruf, der an die Anmeldemethode Ihres Authentifizierungsdelegate übergeben wird.

* **window. Backplane:** Ein Verweis auf Ihr Backplane-Objekt.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

Profil bearbeiten

Dies kann zu einem beliebigen Teil der Site führen, den Benutzer besuchen möchten, um ihre eigene Profilseite anzuzeigen. Dieses Beispiel druckt nur das erstellte Autorenobjekt.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

Profil anzeigen

Wie bei &quot;Profile bearbeiten&quot; sollte sich dies mit der Seite eines Benutzers verknüpfen, die sich vom aktuell angemeldeten Benutzer unterscheidet. Dies kann jedoch implementiert werden. Dieses Beispiel protokolliert einfach den Autor-Parameter an die Konsole.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

