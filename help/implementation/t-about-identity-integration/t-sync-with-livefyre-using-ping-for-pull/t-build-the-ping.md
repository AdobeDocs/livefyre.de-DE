---
description: Erstellen Sie den Ping, damit Ihre Seite Livefyre pings, wenn Benutzer ihr Profil aktualisieren.
seo-description: Erstellen Sie den Ping, damit Ihre Seite Livefyre pings, wenn Benutzer ihr Profil aktualisieren.
seo-title: Ping erstellen
solution: Experience Manager
title: Ping erstellen
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: f76dcd31e58b94856bf551009c2ac50c3233e516

---


# Ping erstellen{#build-the-ping}

Erstellen Sie den Ping, damit Ihre Seite Livefyre pings, wenn Benutzer ihr Profil aktualisieren.

Wenn Livefyre eine Update-Benachrichtigung mit dem `networkName` und `user_id`erhält, sendet das System eine Pull-Anfrage an Ihr Ping für die Pull-URL.

>[!NOTE]
>
>403/Nicht autorisiert als Antwort auf Ihre Ping-Anforderung weist darauf hin, dass an die Ping-Anforderung ein ungültiger Wert `lftoken` angehängt wurde. Bitte stellen Sie sicher, dass die `lftoken` für einen `user_id` Benutzer mit Netzwerkinhaberberechtigungen oder für den Systembenutzer vorgesehen ist. Wenn Sie Livefyre-Bibliotheken verwenden, verwenden Sie die `buildLivefyreToken` Methode, um ein gültiges System-Token für die Anforderung zu generieren.

1. Hinzufügen Code auf Ihrer Seite, der Livefyre pingelt, wenn Benutzer ihr Profil aktualisieren. Erstellen Sie die URL wie folgt:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Ihr Livefyre hat den Netzwerknamen angegeben.
   * **[!UICONTROL user_id:]** Die ID Ihres Benutzers.
   * **[!UICONTROL token:]** Gültiges System-Token.

1. Ziehen Sie die Anforderungsstruktur.
