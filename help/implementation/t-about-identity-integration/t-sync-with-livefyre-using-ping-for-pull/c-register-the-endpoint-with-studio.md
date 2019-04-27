---
description: Registrieren Sie den URL-Endpunkt, damit Livefyre die URL verwenden kann, um aktualisierte Profilinformationen abzurufen.
seo-description: Registrieren Sie den URL-Endpunkt, damit Livefyre die URL verwenden kann, um aktualisierte Profilinformationen abzurufen.
seo-title: Endpunkt mit Studio registrieren
solution: Experience Manager
title: Endpunkt mit Studio registrieren
uuid: 4 eb 816 ee-d 743-43 bf-bfee-d 9 b 9 fd 98 b 482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Endpunkt mit Studio registrieren{#register-the-endpoint-with-studio}

Registrieren Sie den URL-Endpunkt, damit Livefyre die URL verwenden kann, um aktualisierte Profilinformationen abzurufen.

Registrieren Sie das Ping für die Pull-URL nur einmal pro Netzwerk. Sobald der Wert festgelegt wurde, sollte sich dieser Wert nur ändern, wenn sich der Endpunkt zum Abrufen von Benutzerprofildaten aus Ihrem Benutzerverwaltungssystem ändert.

1. Verwenden Sie Studio, um diesen URL-Endpunkt mit Livefyre zu registrieren.
1. Registrieren Sie die URL, von der aus Livefyre aktualisierte Benutzerprofilinformationen abrufen soll, **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** und geben Sie sie in das **[!UICONTROL Ping for Pull URL]** Feld ein.

   Beispielsweise kann die URL wie folgt aussehen: `https://example.yoursite.com/some_path/?id={id}`

