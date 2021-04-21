---
description: Das AuthDelegate-Objekt implementiert Ihr gewünschtes Verhalten zum Durchführen von Authentifizierungsaktionen und Ereignissen, damit Sie die Integration mit dem vorhandenen Authentifizierungssystem Ihrer Site anpassen können.
title: AuthDelegate-Objekt
exl-id: 7c669138-627e-476e-a177-c71346f730df
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# AuthDelegate-Objekt{#authdelegate-object}

Das AuthDelegate-Objekt implementiert Ihr gewünschtes Verhalten zum Durchführen von Authentifizierungsaktionen und Ereignissen, damit Sie die Integration mit dem vorhandenen Authentifizierungssystem Ihrer Site anpassen können.

## Erstellen eines Auth-Delegates {#section_wmn_tv2_gz}

Das auth-Paket muss mit einem auth-Delegaten bereitgestellt werden, bevor eine Aktion durchgeführt werden kann. Ein auth-Delegat ist ein JavaScript-Objekt, das eine der Methoden in diesem Thema implementiert.

## .login(completedLogin) {#section_mpk_lv2_gz}

Melden Sie sich bei einem gültigen Benutzer an und rufen Sie die Funktion &quot;OberflächeLogin&quot;entweder mit einem Error-Objekt bei einem Fehler oder mit den Livefyre-Anmeldeinformationen des Benutzers auf. Allgemeine Implementierungen dieser Methode leiten den Benutzer zu einer Anmeldeseite oder öffnen ein neues Fenster oder ein neues Modell.

In diesem Beispiel wird der Autor eines Livefyre-Benutzers automatisch mit dem Authentifizierungstoken (Token) benachrichtigt:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

Der einfachste Delegate für die Anmeldung könnte den Endbenutzer nach seinem Livefyre-Authentifizierungstoken fragen.

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

## .logout(completedLogout) {#section_uqz_2v2_gz}

Melden Sie sich bei einem Benutzer ab und rufen Sie die Funktion &quot;OberflächeLogout&quot;mit einem Error-Objekt auf, wenn ein Fehler aufgetreten ist, oder mit null, um die Benachrichtigung zu erhalten, dass die Abmeldung erfolgreich war.

Beispiel:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

Gehen Sie vor, um das Profil eines Benutzers Ansicht.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

Gehen Sie vor, um das Profil eines Benutzers zu bearbeiten.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Durch die Implementierung aller oben aufgeführten Methoden kann auth mit einem benutzerdefinierten Autor-Delegaten konfiguriert werden. Nachdem ein Delegat erstellt wurde, kann er mithilfe der Delegate-Methode für auth bereitgestellt werden.

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
