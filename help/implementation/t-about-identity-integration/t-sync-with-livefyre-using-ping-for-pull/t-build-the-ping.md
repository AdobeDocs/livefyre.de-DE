---
description: Erstellen Sie das Ping so, dass Ihre Seitenpings Livefyre lauten, wenn
  Benutzer ihr Profil aktualisieren.
seo-description: Erstellen Sie das Ping so, dass Ihre Seitenpings Livefyre lauten,
  wenn Benutzer ihr Profil aktualisieren.
seo-title: Ping erstellen
solution: Experience Manager
title: Ping erstellen
uuid: cb 8 cc 043-9 ea 5-407 c-b 70 f -3 f 1 e 37 accdae
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Ping erstellen{#build-the-ping}

Erstellen Sie das Ping so, dass Ihre Seitenpings Livefyre lauten, wenn Benutzer ihr Profil aktualisieren.

Wenn Livefyre eine Update-Benachrichtigung mit dem und `networkName` erhält `user_id`, sendet das System eine Pull-Anfrage an Ihre Ping-URL.

>[!NOTE]
>
>403/Nicht autorisiert als Antwort deutet auf eine ungültige `lftoken` Angehängung an die Ping-Anfrage hin. Stellen Sie sicher, `lftoken` dass die Einstellung für einen `user_id` Netzwerkinhaber oder den Systembenutzer gilt. Wenn Sie Livefyre-Bibliotheken verwenden, verwenden Sie die `buildLivefyreToken` Methode, um ein gültiges Systemtoken für die Anforderung zu generieren.

1. Fügen Sie Ihrer Seite einen Code hinzu, der Livefyre aufruft, wenn Benutzer ihr Profil aktualisieren. Erstellen Sie die URL auf diese Weise:

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** Ihr Livefyre-bereitgestellter Netzwerkname.
* **[!UICONTROL user_id:]** Die ID Ihres Benutzers.
* **[!UICONTROL token:]** Gültiges System-Token.

1. Rufen Sie die Anforderungsstruktur ab.
