---
description: Livefyre.require stellt ein Plugin zur Verfügung, mit dem Autoren den Janrain Backplane Bus hören können.
seo-description: Livefyre.require stellt ein Plugin zur Verfügung, mit dem Autoren den Janrain Backplane Bus hören können.
seo-title: Verbinden von Janrain mit Livefyre mithilfe von AuthDelegate
title: Verbinden von Janrain mit Livefyre mithilfe von AuthDelegate
uuid: 9d56e3f4-960a-4108-aab5-2795b0e71c88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 1%

---


# Verbinden von Janrain mit Livefyre mithilfe von AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.require stellt ein Plugin zur Verfügung, mit dem Autoren den Janrain Backplane Bus hören können.

Wenn eine Identitäts-/Anmelde-Nachricht im Backplane-Kanal gesendet wird, wird auth.authentication() mit dem Livefyre-Authentifizierungstoken des Benutzers für Sie aufgerufen. Sie müssen weiterhin einen AuthDelegate implementieren.

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
>Das window.Backplane-Objekt muss auf Ihrer Seite definiert werden, bevor auth.plugin mit dem Livefyre Backplane-Plug-In aufgerufen wird. Um sicherzustellen, dass das Backplane-Objekt verfügbar ist, rufen Sie den Livefyre-Instanziierungscode eines onReady-Rückrufs auf. Wenden Sie sich an Ihren Janrain-Kontakt, um festzustellen, wann andere Anwendungen das Backplane-Objekt verwenden können.

Im Folgenden finden Sie einige Beispiele dafür, wie ein Auth-Delegierter nach einer Integration von Janrain Capture suchen könnte.

>[!NOTE]
>
>Ihr Auth-Delegate hängt von Ihrer Janrain-Instanz ab.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* Der Rückruf, der an die Anmeldemethode Ihres Authentidelegaten weitergeleitet wird
* Der Verweis auf Ihre Janrain-Erfassungsvariable.
* : Ein Verweis auf das Backplane-Objekt.

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

Abmeldung

* **OberflächeLogout:** Der Rückruf, der an die Anmeldemethode des Authentifizierungsdelegaten weitergeleitet wird.

* **window.backplane:** Ein Verweis auf Ihr Backplane-Objekt.

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

Dies kann zu jedem Teil der Site führen, den Sie zur Ansicht der eigenen Profil-Seite aufrufen möchten. In diesem Beispiel wird lediglich das übergebene Autorenobjekt ausgedruckt.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

Ansicht Profil

Wie beim Bearbeiten von Profil sollte dieser Link zu einer Benutzerseite führen, die sich vom derzeit angemeldeten Benutzer unterscheidet. Dies kann implementiert werden, wie Sie es für richtig halten. In diesem Beispiel wird der Parameter author einfach in der Konsole protokolliert.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

