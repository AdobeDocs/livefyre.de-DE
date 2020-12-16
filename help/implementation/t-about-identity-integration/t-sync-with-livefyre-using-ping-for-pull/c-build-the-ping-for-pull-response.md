---
description: Erstellen Sie die Ping for Pull-Antwort, um aktualisierte Benutzerinformationen an Livefyre zu senden.
seo-description: Erstellen Sie die Ping for Pull-Antwort, um aktualisierte Benutzerinformationen an Livefyre zu senden.
seo-title: Ping für vollständige Antwort erstellen
solution: Experience Manager
title: Ping für vollständige Antwort erstellen
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 1%

---


# Ping für Pullantwort{#build-the-ping-for-pull-response} erstellen

Erstellen Sie die Ping for Pull-Antwort, um aktualisierte Benutzerinformationen an Livefyre zu senden.

| Typ | Eigenschaft | Beschreibung |
|--- |--- |--- |
| Zeichenfolge *erforderlich* | id | Die Benutzer-ID des Profils. Dies muss für alle Benutzer in Ihrem Netzwerk eindeutig sein und darf sich nicht ändern. |
| Zeichenfolge *erforderlich* | display_name | Der Anzeigename des Benutzers. Dies wird mit Livefyre-Inhalten gerendert, die vom Benutzer gepostet werden. |
| Objekt *optional, jedoch empfohlen* | name | Zeichenfolgen zum Definieren der formatierten, ersten, mittleren und letzten Namen des Benutzers. |
| Zeichenfolge *optional, jedoch empfohlen* | E-Mail | E-Mail-Adresse des Benutzers. Dient zum Senden von E-Mail-Benachrichtigungen. |
| Zeichenfolge *optional, jedoch empfohlen* | image_url | URL zu einem Avatar, der für den Benutzer angezeigt werden soll. Livefyre skaliert hochgeladene Bilder auf 100 x 100, 75 x 75 oder 50 x 50 Pixel, je nach Bedarf. Die besten Ergebnisse erzielen Sie, wenn Sie ein quadratisches Bild mit 100 x 100 Pixeln hochladen. Um sicherzustellen, dass das Avatarbild in Livefyre aktualisiert wird, ändern Sie die image_url für jede Bildaktualisierung, damit Ping for Pull erkennt, dass das Bild geändert wurde. Fügen Sie beispielsweise dem Dateinamen einen Zeitstempel hinzu oder erhöhen Sie die Bildänderungen. Hinweis:  Alle URLs müssen vollständig qualifiziert und zugänglich sein. |
| Zeichenfolge *optional, jedoch empfohlen* | profil_url | URL zur Profil-Seite des Benutzers auf Ihrer Site. |
| Zeichenfolge *optional, jedoch empfohlen* | settings_url | URL zu einer Seite, auf der Benutzer die Benutzereinstellungen für das Profil Ihrer Site konfigurieren können. |
| Array *optional, jedoch empfohlen* | Tags | Dient zum Zuweisen von Benutzern zu Benutzergruppen. Tags können 1-63 alphanumerische Zeichen und Unterstriche enthalten. |
| Boolean *optional, jedoch empfohlen* | autofollow_convertions | Definiert, ob ein Benutzer einer Sammlung nach dem Posten in der Sammlung automatisch folgen möchte. Wenn Benutzer einer Sammlung folgen, erhalten sie E-Mail-Benachrichtigungen, wenn andere Benutzer teilnehmen. Kann wahr oder falsch sein. Der Standardwert ist true. |
| Objekt *optional, jedoch empfohlen* | email_notifications | Definiert die Häufigkeit verfügbarer Livefyre-E-Mail-Benachrichtigungen. Für jeden Benachrichtigungstyp können unterschiedliche Frequenzen festgelegt werden. Standardmäßig werden keine Benachrichtigungen gesendet. <br><ul><li> sofort Benachrichtigungen beim aufgelisteten Ereignis ausgeben. </li><li>gibt oft Benachrichtigungen in Stapeln aus. </li><li> keine E-Mail-Benachrichtigung für die Aktivität senden. </li><li>*Kommentare*: Definiert, wann Benachrichtigungen gesendet werden, wenn andere Benutzer Inhalte in Sammlungen veröffentlichen, denen dieser Benutzer folgt. </li><li>*Antworten*: Definiert, wann Benachrichtigungen gesendet werden, wenn ein anderer Benutzer auf den Inhalt dieses Benutzers antwortet.</li><li>*&quot;Gefällt mir&quot;*: Definiert, wann Benachrichtigungen gesendet werden, wenn der Inhalt dieses Benutzers einem anderen Benutzer gefällt.</li><li>*moderator_comments*: Definiert, wann Benachrichtigungen an Moderatoren gesendet werden, wenn Benutzer Inhalte an eine Sammlung im Netzwerk posten.</li><li>*moderator_flags*: Definiert, wann Benachrichtigungen an Moderatoren gesendet werden, wenn andere Benutzer Inhalte in einer Sammlung im Netzwerk kennzeichnen.</li></ul> |
| Zeichenfolge *optional* | Position | Ein vom Benutzer gesendeter Speicherort. |
| Zeichenfolge *optional* | bio | Eine vom Benutzer übermittelte Autobiografie. |
| Array *optional* | websites | Ein Array von vom Benutzer gesendeten Sites. Max = 2. |
| Objekt *optional* | display_rules | Definiert, welche Profil-Eigenschaften für andere Benutzer öffentlich sichtbar sind. Für jeden verfügbaren Parameter ist die boolesche Eingabe &quot;true&quot;oder &quot;false&quot;erforderlich. Verfügbare Parameter:  <br><ul><li>bio </li><li> Position</li><li>  Geschlecht </li><li>namimage </li><li> remote_Profil_url</li></ul> |
| Boolean *optional* | moderator | Definiert, ob der Benutzer über Moderatorberechtigungen im Netzwerk verfügt. |
| Boolean *optional* | gravatar_disabled | Definiert, ob Livefyre die Verwendung eines Gravatars deaktivieren soll, wenn keine image_url angegeben ist. |

## Beispielantwort {#section_uxt_3dd_mz}

```
{
 "id": "1234567890",
 "display_name": "Bob Dole",
 "name": {
   "formatted": "Bob Joseph Dole",
   "first": "Bob",
   "middle": "Joseph",
   "last": "Dole"
 },
   "email": "bob@dole.com",
   "image_url": "https://dole.com/images/bob.jpg",
   "profile_url": "https://site.com/bobdole",
   "settings_url":"https://site.com/settings",
   "tags": ["bob", "dole"],
   "autofollow_conversations": "true",
   "email_notifications": {
      "comments": "never",
      "replies": "immediately",
      "likes": "often",
      "moderator_comments": "immediately",
      "moderator_flags": "immediately" 
 },
  "location": "Washington D.C., USA",
  "bio": "Bob Dole speaks in the third person",
  "websites": ["https://dole.com/blog/", "https://bobdolerocks.com"],
  "display_rules": {
      "bio": "false",
      "location": "false",
      "gender": "false",
      "name": "false",
      "image": "false",
      "remote_profile_url": "false"
  },
  "moderator": "true",
  "gravatar_disabled": "false"
}
```
