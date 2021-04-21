---
description: Registrieren Sie den URL-Endpunkt, damit Livefyre über die URL aktualisierte Profil-Informationen abrufen kann.
title: Endpunkt mit Studio registrieren
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Registrieren Sie den Endpunkt mit Studio{#register-the-endpoint-with-studio}

Registrieren Sie den URL-Endpunkt, damit Livefyre über die URL aktualisierte Profil-Informationen abrufen kann.

Registrieren Sie Ping für Pull-URL nur einmal pro Netzwerk. Nach der Einstellung sollte sich dieser Wert nur ändern, wenn sich der Endpunkt zum Abrufen von Benutzerdaten aus Ihrem Benutzerverwaltungssystem ändert.

1. Verwenden Sie Studio, um diesen URL-Endpunkt bei Livefyre zu registrieren.
1. Registrieren Sie die URL, von der Livefyre aktualisierte Benutzerinformationen abruft, gehen Sie zu **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** und geben Sie sie in das Feld **[!UICONTROL Ping for Pull URL]** ein.

   Die URL kann beispielsweise wie folgt aussehen: `https://example.yoursite.com/some_path/?id={id}`
