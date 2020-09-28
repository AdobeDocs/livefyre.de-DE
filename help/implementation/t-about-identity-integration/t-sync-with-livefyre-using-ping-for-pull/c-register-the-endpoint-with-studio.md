---
description: Registrieren Sie den URL-Endpunkt, damit Livefyre über die URL aktualisierte Profilinformationen abrufen kann.
seo-description: Registrieren Sie den URL-Endpunkt, damit Livefyre über die URL aktualisierte Profilinformationen abrufen kann.
seo-title: Endpunkt mit Studio registrieren
solution: Experience Manager
title: Endpunkt mit Studio registrieren
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Endpunkt mit Studio registrieren{#register-the-endpoint-with-studio}

Registrieren Sie den URL-Endpunkt, damit Livefyre über die URL aktualisierte Profilinformationen abrufen kann.

Registrieren Sie Ping für Pull-URL nur einmal pro Netzwerk. Nach der Einstellung sollte sich dieser Wert nur ändern, wenn sich der Endpunkt zum Abrufen von Benutzerprofildaten aus Ihrem Benutzerverwaltungssystem ändert.

1. Verwenden Sie Studio, um diesen URL-Endpunkt bei Livefyre zu registrieren.
1. Registrieren Sie die URL, von der Livefyre aktualisierte Benutzerprofilinformationen abruft, gehen Sie zu **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** und geben Sie sie in das **[!UICONTROL Ping for Pull URL]** Feld ein.

   Die URL kann beispielsweise wie folgt aussehen: `https://example.yoursite.com/some_path/?id={id}`

