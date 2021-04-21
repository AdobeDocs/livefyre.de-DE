---
description: Erstellen Sie den Ping, damit Ihre Seite Livefyre pings, wenn Benutzer ihr Profil aktualisieren.
title: Ping erstellen
exl-id: 626c200b-eaff-483f-b1eb-7d8993fe5e7c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Erstellen Sie die Ping{#build-the-ping}

Erstellen Sie den Ping, damit Ihre Seite Livefyre pings, wenn Benutzer ihr Profil aktualisieren.

Wenn Livefyre eine Update-Benachrichtigung mit den Werten `networkName` und `user_id` erhält, sendet das System eine Pull-Anfrage an Ihr Ping für die Pull-URL.

>[!NOTE]
>
>403/Nicht autorisiert als Antwort auf Ihre Ping-Anforderung weist auf eine ungültige `lftoken` an die Ping-Anforderung angehängt hin. Vergewissern Sie sich, dass `lftoken` für ein `user_id` mit Netzwerkeigentümerberechtigungen oder dem Systembenutzer gilt. Wenn Sie Livefyre-Bibliotheken verwenden, verwenden Sie die `buildLivefyreToken`-Methode, um ein gültiges System-Token für die Anforderung zu generieren.

1. hinzufügen Code auf Ihrer Seite, der Livefyre pingelt, wenn Benutzer ihr Profil aktualisieren. Erstellen Sie die URL wie folgt:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** Ihr Livefyre hat den Netzwerknamen angegeben.
   * **[!UICONTROL user_id:]** Die ID Ihres Benutzers.
   * **[!UICONTROL token:]** Gültiges System-Token.

1. Ziehen Sie die Anforderungsstruktur.
