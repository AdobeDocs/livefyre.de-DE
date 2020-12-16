---
description: Kunden, die Janrain Capture und Backplane verwenden, können Livefyre Auth für die einmalige Anmeldung (SSO) verwenden, sodass Benutzer sofort mit Ihren Livefyre-Apps interagieren können, wenn sie sich bei Ihrer Site anmelden.
seo-description: Kunden, die Janrain Capture und Backplane verwenden, können Livefyre Auth für die einmalige Anmeldung (SSO) verwenden, sodass Benutzer sofort mit Ihren Livefyre-Apps interagieren können, wenn sie sich bei Ihrer Site anmelden.
seo-title: Janrain Capture/Backplane
solution: Experience Manager
title: Janrain Capture/Backplane
uuid: 776e9626-db04-4c34-adfe-681a71b552c5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 1%

---


# Janrain Capture/Backplane{#janrain-capture-backplane}

Kunden, die Janrain Capture und Backplane verwenden, können Livefyre Auth für die einmalige Anmeldung (SSO) verwenden, sodass Benutzer sofort mit Ihren Livefyre-Apps interagieren können, wenn sie sich bei Ihrer Site anmelden.

Um von dieser integrierten Capture/Backplane-Integration zu profitieren, müssen Sie Konfigurationsänderungen an Ihrer Capture-App und Ihrer Livefyre.js-Integration vornehmen.

>[!NOTE]
>
>Überspringen Sie diesen Abschnitt, wenn Sie nicht mit Janrain Capture arbeiten.

Weitere Informationen finden Sie unter [Janrains Backplane-Dokumentation](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Capture einrichten.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Optional) [Hinzufügen Livefyre-Standardwerte auf Ihre Capture-App](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Erstellen Sie das Objekt AuthDelegate.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Synchronisieren Sie Livefyre mit Ping für Pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Schritt 1: Capture einrichten {#section_r2f_kxt_bbb}

Livefyre benötigt bestimmte Anmeldeinformationen von Ihrer Janrain Capture-App.

1. Richten Sie die App &quot;Janrain Capture&quot;ein.
1. Sammeln Sie die folgenden Informationen für Livefyre:

   * Zugriff auf Ihre Janrain Capture-Instanz.
   * Zugang zu Ihrem Janrain Engage Dashboard.
   * Ihre Capture-Einstellungen und -Anmeldedaten.
   * Ihre Anmeldedaten für Interagieren.
   * Ihre Identitäts-URL.

>[!NOTE]
>
>Livefyre erhält Daten direkt vom CNAME; Daher kann diese Identitäts-URL kein CNAMEd-Datensatz (ein Vanity-URL-CNAME) sein, der zum tatsächlichen CNAME der Janrain Capture aufgelöst wird.

## Schritt 2: (Optional) Hinzufügen Livefyre-Standardeinstellungen auf Ihre Capture-App {#section_z2s_txt_bbb}

hinzufügen Livefyre-Standard sind Benutzer, die in Ihrer Capture-App gespeichert sind, damit Sie E-Mail-Benachrichtigungen an Benutzer senden oder ihnen erlauben können, automatisch Konversationen zu verfolgen, zu denen Benutzer Kommentare abgeben.

1. Führen Sie [Schritt 1 aus: &quot;Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb) einrichten&quot;.
1. hinzufügen die folgenden Livefyre-Standardfelder. Alle Felder sind optional.

| Parameter | Typ | Beschreibung |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Zeichenfolge | Benachrichtigen Sie den Benutzer, wenn jemand einen Artikel kommentiert, dass er ihm folgt. Kann sofort, oft oder nie sein. |
| **[!UICONTROL livefyre_likes]** | Zeichenfolge | Benachrichtigen Sie den Benutzer, wenn ihm einer seiner Beiträge gefällt. Kann sofort, oft oder nie sein. |
| **[!UICONTROL livefyre_replies]** | Zeichenfolge | Benachrichtigen Sie den Benutzer, wenn jemand auf einen seiner Beiträge antwortet.Kann sofort, häufig oder nie sein. |
| **[!UICONTROL livefyre_moderator_comments]** | Zeichenfolge | Benachrichtigen Sie den Moderator, wenn jemand zu einem Gespräch Stellung nimmt, dass er moderiert ist.Kann sofort, häufig oder nie sein. |
| **[!UICONTROL livefyre_moderator_flags]** | Zeichenfolge | Benachrichtigen Sie den Moderator, wenn jemand bei einer Unterhaltung einen Beitrag markiert, dass er moderiert wird.Kann sofort, häufig oder nie gesendet werden. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Boolesch | Lassen Sie den Benutzer beim Verlassen eines Beitrags automatisch eine Konversation durchführen. Kann wahr oder falsch sein. |

## Schritt 3: Erstellen des AuthDelegate-Objekts für die Janrain-Integration {#section_asv_vyt_bbb}

Livefyre.require stellt ein Plugin zur Verfügung, mit dem Autoren den Janrain Backplane Bus hören können.

### Anmelden {#login}

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



>[!NOTE]
>
>Ihr Auth-Delegate hängt von Ihrer Janrain-Instanz ab.

Im Folgenden finden Sie einige Beispiele dafür, wie ein Auth-Delegierter nach einer Integration von Janrain Capture suchen könnte.

* `errback`: Der Rückruf, der an die Anmeldemethode Ihres Authentidelegaten weitergeleitet wird
* `janrain`: Der Verweis auf Ihre Janrain-Erfassungsvariable.
* `window.Backplane`: Ein Verweis auf das Backplane-Objekt.

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

### Abmeldung {#logout}

* `finishLogout`: Der Rückruf, der an die Anmeldemethode des Authentifizierungsdelegaten weitergeleitet wird.

* `window.Backplane`: Ein Verweis auf das Backplane-Objekt.

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

### Ansicht Profil {#viewprofile}

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

## Schritt 4: Synchronisieren mit Livefyre mit Ping für Pull für Janrain Integration {#section_ilv_bzt_bbb}

Die Synchronisierung von Livefyre Remote-Profilen mit Ihrem Capture-Benutzerverwaltungssystem umfasst eine Reihe von Schritten, die als Ping for Pull bezeichnet werden. Dieser Vorgang erfordert, dass Sie ein gültiges Zugriffstoken von Janrain abrufen und dieses Token dann an einen in Schritt 3 unten angegebenen Endpunkt übergeben.

1. Besorgen Sie sich einen Zugangscode von Janrain.

   Um den Zugriffscode abzurufen, geben Sie die erforderlichen Anmeldeinformationen ein, geben Sie &quot;user_type&quot;als &quot;user&quot;an und die uuid als die zu aktualisierende UID des aktuellen Benutzers. Weitere Informationen finden Sie unter [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Geben Sie den Zugriffscode für ein Zugriffstoken ein. Geben Sie die erforderlichen Anmeldeinformationen, den aus Schritt 1 erhaltenen Zugriffscode und geben Sie als &quot;permission_code&quot;den &quot;grant_type&quot;an.

   Weitere Informationen finden Sie unter [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Treten Sie auf den Endpunkt Livefyre &quot;Ping to Pull Capture&quot;.

   Endpunkt-URL: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] wobei ***{networkName}*** der Netzwerkname ist, der Ihnen von Livefyre bereitgestellt wird, und das jrtoken das Token ist, das Sie von Janrain in Schritt 2 erhalten haben.

   Sobald Sie diesen Endpunkt erreicht haben, erhalten Sie eine 202-Antwort und Livefyre beginnt einen asynchronen Prozess.

## So funktioniert alles {#concept_mty_f31_2cb}

Um von dieser integrierten Capture/Backplane-Integration zu profitieren, müssen Sie einige Konfigurationsänderungen an Ihrer Capture-App und Ihrer Livefyre.js-Integration vornehmen.

Janrain sendet erfolgreiche Anmelde-/Abmeldemeldungen über den Backplane-Bus, auf dem die Livefyre-App bei ordnungsgemäßer Konfiguration wartet. Diese Meldungen enthalten alle Informationen, die erforderlich sind, um App-Benutzer als angemeldet oder abgemeldet anzuzeigen. Entwickler können Backplane-Bus-Ansichten durch Prüfen der Registerkarte &quot;Netzwerk&quot;in der Entwicklerkonsole Ihres Browsers erstellen.

## Beispiel für einen Anmeldungscode {#section_ftt_tvp_mz}

Anfrage:

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

## Beispiel für einen Abmelde-Code {#section_t52_svp_mz}

Anfrage:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Antwort:

```
Backplane.finishInit("{CHANNEL}");
```

Wenn diese Nachrichten nicht in Ihren Netzwerkanforderungen angezeigt werden, wird Livefyre die Anmeldeversuche/Abmeldeversuche nicht kennen, daher kann Livefyre den Benutzer nicht in die App integrieren.
