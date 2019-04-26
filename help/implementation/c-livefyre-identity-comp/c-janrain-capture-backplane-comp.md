---
description: Kunden, die Janrain Capture und Backplane verwenden, können Livefyre
  Auth für Single Sign On (SSO) verwenden, sodass Benutzer sofort mit Ihren Livefyre-Apps
  interagieren können, wenn sie sich bei Ihrer Site anmelden.
seo-description: Kunden, die Janrain Capture und Backplane verwenden, können Livefyre
  Auth für Single Sign On (SSO) verwenden, sodass Benutzer sofort mit Ihren Livefyre-Apps
  interagieren können, wenn sie sich bei Ihrer Site anmelden.
seo-title: Janrain Capture/Backplane
solution: Experience Manager
title: Janrain Capture/Backplane
uuid: 776 e 9626-db 04-4 c 34-adfe -681 a 71 b 552 c 5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capture/Backplane{#janrain-capture-backplane}

Kunden, die Janrain Capture und Backplane verwenden, können Livefyre Auth für Single Sign On (SSO) verwenden, sodass Benutzer sofort mit Ihren Livefyre-Apps interagieren können, wenn sie sich bei Ihrer Site anmelden.

Um diese integrierte Erfassung/Backplane-Integration nutzen zu können, müssen Sie Konfigurationsänderungen sowohl an Ihrer Capture-App als auch an Ihrer Livefyre. js-Integration vornehmen.

>[!NOTE]
>
>Überspringen Sie diesen Abschnitt, wenn Sie Janrain Capture nicht verwenden.

Weitere Informationen finden Sie in [der Backebeners-Dokumentation von Janrain](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Einrichten der Erfassung.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Optional) [Fügen Sie Ihrer Capture-App "Livefyre Standard"](#c_janrain_capture_backplane/section_z2s_txt_bbb)hinzu.
1. [Erstellen Sie das authdelegate-Objekt.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Synchronisieren Sie mit Livefyre mit Ping für Pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Schritt 1: Einrichten der Erfassung {#section_r2f_kxt_bbb}

Livefyre benötigt bestimmte Anmeldeinformationen aus Ihrer Janrain Capture-App.

1. Richten Sie die Janrain Capture-App ein.
1. Erfassen Sie die folgenden Informationen für Livefyre:

   * Zugriff auf Ihre Janrain Capture-Instanz.
   * Zugriff auf Ihr Janrain Engagement Dashboard.
   * Ihre Aufnahmeeinstellungen und Anmeldedaten.
   * Ihre Anmeldedaten.
   * Ihre Identitäts-URL.

>[!NOTE]
>
>Livefyre erhält Daten direkt aus dem CNAME; Daher kann diese Identitätsurl kein cnamed-Record (Vanity-URL-CNAME) sein, der in den tatsächlichen CNAME von Janrain Capture aufgelöst wird.

## Schritt 2: (Optional) Fügen Sie Ihrer Capture-App "Livefyre Standard" hinzu. {#section_z2s_txt_bbb}

Fügen Sie den in Ihrer Capture-App gespeicherten Benutzern standardmäßig Livefyre hinzu, damit Sie Benutzern E-Email-Benachrichtigungen senden oder die Unterhaltungen automatisch verfolgen können, auf die Benutzer Kommentare abgeben.

1. Führen Sie Schritt [1 aus: Einrichten der Erfassung](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Fügen Sie die folgenden Livefyre-Standardfelder hinzu. Alle Felder sind optional.

| Parameter | Typ | Beschreibung |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Zeichenfolge | Benachrichtigen Sie den Benutzer, wenn jemand Kommentare zu einem Artikel erhält, den sie verfolgen. Kann sofort oder nie auftreten. |
| **[!UICONTROL livefyre_likes]** | Zeichenfolge | Benachrichtigen Sie den Benutzer, wenn jemand ihren Beitrag gefällt. Kann sofort oder nie auftreten. |
| **[!UICONTROL livefyre_replies]** | Zeichenfolge | Benachrichtigen Sie Benutzer, wenn jemand auf einen ihrer Beiträge antwortet. Können Sie sofort oder nie reagieren. |
| **[!UICONTROL livefyre_moderator_comments]** | Zeichenfolge | Benachrichtigen Sie Moderatoren, wenn jemand Kommentare zu einer Moderation abgeben kann, die sie moderieren. |
| **[!UICONTROL livefyre_moderator_flags]** | Zeichenfolge | Benachrichtigen Sie Moderatoren, wenn jemand einen Beitrag in einer Konversation kennzeichnet, die moderiert wird. Können Sie sofort oder nie handeln. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Boolescher Wert | Bitten Sie den Benutzer, eine Unterhaltung zu folgen, wenn sie einen Beitrag hinterlassen. Kann wahr oder falsch sein. |

## Schritt 3: Authdelegate-Objekt für Janrain Integration erstellen {#section_asv_vyt_bbb}

Livefyre. erforderlich ist ein Plugin, mit dem die Authentifizierung des Janrain Backplane-Bus aktiviert wird.

### Anmeldung {#login}

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



>[!NOTE]
>
>Ihre Authentifizierungsdelegation variiert je nach Ihrer Janrain-Instanz.

Im Folgenden finden Sie einige Beispiele dafür, wie eine Authentifizierungsdelegation nach einer Janrain Capture-Integration sucht.

* `errback`: Der Rückruf, der an die Anmeldemethode der Authentifizierungsmethode übergeben wird
* `janrain`: Der Verweis auf Ihre Janrain-Erfassungsvariable.
* `window.Backplane`: Ein Verweis auf Ihr Backplane-Objekt.

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

### Abmelden {#logout}

* `finishLogout`: Der Rückruf, der an die Anmeldemethode Ihres Authentifizierungsdelegate übergeben wird.

* `window.Backplane`: Ein Verweis auf Ihr Backplane-Objekt.

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

### Profil bearbeiten {#editprofile}

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

### Profil anzeigen {#viewprofile}

Wie bei "Profile bearbeiten" sollte sich dies mit der Seite eines Benutzers verknüpfen, die sich vom aktuell angemeldeten Benutzer unterscheidet. Dies kann jedoch implementiert werden. Dieses Beispiel protokolliert einfach den Autor-Parameter an die Konsole.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## Schritt 4: Synchronisieren mit Livefyre mit Ping for Pull for Janrain Integration {#section_ilv_bzt_bbb}

Wenn Sie Livefyre Remote Profile synchronisieren, die sich mit Ihrem Datenerfassungssystem synchronisieren, sind eine Reihe von Schritten erforderlich, die als Ping für Pull bezeichnet werden. Für diesen Prozess ist es erforderlich, dass Sie ein gültiges Zugriffstoken von Janrain erhalten und dieses Token dann an einen in Schritt 3 angegebenen Endpunkt weitergeben.

1. Verschaffen Sie sich einen Zugriff von Janrain.

   Um den Zugriffscode abzurufen, geben Sie die erforderlichen Anmeldeinformationen an, geben Sie den user_ type als "Benutzer" und die uuid als aktuelle uuid des Benutzers an, um ihn zu aktualisieren. Weitere Informationen finden Sie unter [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Tauschen Sie den Zugriffscode für ein Zugriffstoken aus. Geben Sie die erforderlichen Anmeldeinformationen an, den aus Schritt 1 erhaltenen Zugriffscode und geben Sie den grant_ type als "authorization_ code" an.

   Weitere Informationen finden Sie unter [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Klicken Sie auf den Endpunkt Livefyre "Ping to Pull Capture" .

   Endpunkt-URL: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] Dabei ***ist {networkname}*** der Netzwerkname, den Sie von Livefyre erhalten, und das jrtoken ist das Token, das von Janrain in Schritt 2 empfangen wurde.

   Sobald Sie diesen Endpunkt erreicht haben, erhalten Sie eine 202-Antwort und Livefyre beginnt mit einem asynchronen Prozess.

## So funktioniert es alle {#concept_mty_f31_2cb}

Um diese integrierte Erfassung/Backplane-Integration nutzen zu können, müssen Sie einige Konfigurationsänderungen sowohl an Ihrer Capture-App als auch an Ihrer Livefyre. js-Integration vornehmen.

Janrain sendet erfolgreiche Anmeldungs-/Abmeldemeldungen über den Backplane-Bus, auf dem die Livefyre-App nach der ordnungsgemäßen Konfiguration überwacht wird. Diese Meldungen enthalten alle erforderlichen Informationen, um App-Benutzer als angemeldet oder abgemeldet anzuzeigen. Entwickler können die Backplane-Bus-Nachrichten anzeigen, indem sie die Registerkarte "Netzwerk" in der Entwicklerkonsole Ihres Browsers überprüfen.

## Beispiel für eine Anmeldung {#section_ftt_tvp_mz}

Anforderung:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

Antwort:

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

Leere Antwort:

```
Backplane.response([]);
```

## Beispiel für einen Abmeldecode {#section_t52_svp_mz}

Anforderung:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Antwort:

```
Backplane.finishInit("{CHANNEL}");
```

Wenn diese Meldungen nicht in Ihren Netzwerkanforderungen angezeigt werden, wird Livefyre nicht über die Anmelde-/Abmeldeversuche informiert. Daher kann Livefyre den Benutzer nicht in die App integrieren.
