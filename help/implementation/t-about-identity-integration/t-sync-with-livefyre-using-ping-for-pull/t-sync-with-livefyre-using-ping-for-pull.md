---
description: Verwenden Sie Ping for Pull, um Livefyre mit Ihrem Benutzerverwaltungssystem synchron zu halten.
seo-description: Verwenden Sie Ping for Pull, um Livefyre mit Ihrem Benutzerverwaltungssystem synchron zu halten.
seo-title: Mit Livefyre mit Ping synchronisieren
solution: Experience Manager
title: Mit Livefyre mit Ping synchronisieren
uuid: 7b059064-1cca-46d7-8055-dfe59f493ac1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Mit Livefyre mit Ping synchronisieren{#sync-with-livefyre-using-ping-for-pull}

Verwenden Sie Ping for Pull, um Livefyre mit Ihrem Benutzerverwaltungssystem synchron zu halten.

Im Allgemeinen ***Ping*** Livefyre jedes Mal, wenn ein Benutzer Ihrer Website/App sein Profil aktualisiert (Anzeigename, Avatar usw.) und Livefyre das aktualisierte Profil dieses Benutzers ***abruft*** .

![](assets/Ping-for-Pull.png)

Ping für Pullsequenz:

1. Der Kunde sendet eine Ping-Anfrage an Livefyre (einschließlich des zu aktualisierenden Benutzers).
1. Livefyre bestätigt den Eingang von Ping mit HTTP 200/Success.
1. Livefyre verarbeitet Pull-Anforderung.
1. Livefyre-Warteschlangen Pull-Anforderung.
1. Livefyre führt eine Pull-Anforderung an den Endpunkt aus, um aktualisierte Benutzerinformationen zu erfassen.
1. Der Kunde erhält die Antwort Pull und überprüft sie.
1. Livefyre aktualisiert Remote Profiles mit den externen Profilinformationen, die im Pull-Endpunkt enthalten sind.

Ping Livefyre jedes Mal, wenn ein Benutzer seine Profilinformationen aktualisiert. Während die Ping für die Pull-Fertigstellungszeit je nach Netzwerklast variieren kann, werden Benutzerinformationen in 1 bis 10 Minuten aktualisiert. Aktualisierte Profiländerungen werden zuerst in Livefyre Studio &gt; Benutzer angezeigt.

Aktualisierte Profilinformationen werden nach zwei Ereignissen in Ihren Livefyre-Apps angezeigt:

* Ein Benutzer meldet sich ab und meldet sich dann wieder bei der App an. Anzeigennamenwerte im userAuthToken haben bei Pull-Aktualisierungen Vorrang vor Ping. Ein Benutzer, der sich abmeldet/anmeldet, aktualisiert das Token, um die Sitzung zu aktualisieren.

   Um beim Aktualisieren der Profilinformationen neue userAuthTokens zu generieren, melden Sie sich mit dem SSO authDelegate erneut im Hintergrund an.

* Ein Bootstrap-Update zur Sammlung bringt die aktualisierten Informationen (höchstens alle 5-10 Minuten) ein.

So implementieren Sie Ping for Pull für Ihr Benutzerprofilsystem:

1. [Erstellen Sie den Pull-Endpunkt](#t_build_the_pull_endpoint).

   >[!NOTE]
   >
   >Die Livefyre-Bibliothek enthält eine syncUser-Methode, um Ihre Benutzerprofile auf dem neuesten Stand zu halten. Überspringen Sie die nächsten beiden Schritte, wenn Sie die Livefyre-Bibliothek verwenden.

1. [Registrieren Sie den Pull-Endpunkt in Studio](#register_the_endpoint_with_studio).
1. [Erstellen Sie den Ping](#t_build_the_ping).
1. [Erstellen Sie das Ping für Pull-Antwort].(#reference_n3x_pzb_mz)
