---
description: Das authdelegate-Objekt implementiert das gewünschte Verhalten zur Durchführung
  von Authentifizierungsaktionen und Ereignissen, damit Sie die Integration mit dem
  bestehenden Authentifizierungssystem Ihrer Site anpassen können.
seo-description: Das authdelegate-Objekt implementiert das gewünschte Verhalten zur
  Durchführung von Authentifizierungsaktionen und Ereignissen, damit Sie die Integration
  mit dem bestehenden Authentifizierungssystem Ihrer Site anpassen können.
seo-title: Authdelegate-Objekt
solution: Experience Manager
title: Authdelegate-Objekt
uuid: a 6 acc 4 ef-d 442-4782-9 bfa-bbe 494547 c 2 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Authdelegate-Objekt{#authdelegate-object}

Das authdelegate-Objekt implementiert das gewünschte Verhalten zur Durchführung von Authentifizierungsaktionen und Ereignissen, damit Sie die Integration mit dem bestehenden Authentifizierungssystem Ihrer Site anpassen können.

## Erstellen einer Authentifizierungsdelegierung {#section_wmn_tv2_gz}

Bevor eine Aktion ausgeführt werden kann, muss das Authentifizierungspaket mit einer Authentifizierung bereitgestellt werden. Eine Authentifizierungsdelegierung ist ein javascript-Objekt, das eine der Methoden in diesem Thema implementiert.

## . login (finishlogin) {#section_mpk_lv2_gz}

Melden Sie sich einen gültigen Benutzer an und rufen Sie die Funktion finishlogin entweder mit einem Error-Objekt auf, wenn es einen Fehler gibt, oder die Livefyre-Anmeldeinformationen des Benutzers. Durch gängige Implementierungen dieser Methode wird der Benutzer auf eine Anmeldeseite umgeleitet oder ein neues Fenster oder Modal geöffnet.

In diesem Beispiel wird Authentifizierung eines Livefyre-Benutzers automatisch mit dem Authentifizierungstoken (Token) benachrichtigt:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

Die einfachste Anmeldungsdelegation könnte den Endbenutzer bitten, sein Livefyre-Authentifizierungstoken zu erhalten.

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## . Abmelden (finishlogout) {#section_uqz_2v2_gz}

Melden Sie sich einen Benutzer ab und rufen Sie die Funktion finishlogout entweder mit einem Error-Objekt auf, wenn ein Fehler aufgetreten ist, oder Null, um Auth mitzuteilen, dass die Abmeldung erfolgreich war.

Beispiel:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## . Viewprofile (Benutzer) {#section_kkv_dv2_gz}

Ergreifen Sie Aktion, um das Profil eines Benutzers anzuzeigen.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## . Editprofile (Benutzer) {#section_bkx_pq2_gz}

Ergreifen Sie Aktionen, um das Profil eines Benutzers zu bearbeiten.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Durch die Implementierung aller oben aufgeführten Methoden kann die Authentifizierung mit einer benutzerdefinierten Authentifizierung konfiguriert werden. Nachdem ein Delegate erstellt wurde, kann er zur Authentifizierung mithilfe der Delegate-Methode bereitgestellt werden.

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```

