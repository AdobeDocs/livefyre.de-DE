---
description: Erstellen Sie die Ping for Pull-Antwort, um aktualisierte Benutzerinformationen an Livefyre zu senden.
seo-description: Erstellen Sie die Ping for Pull-Antwort, um aktualisierte Benutzerinformationen an Livefyre zu senden.
seo-title: Ping für vollständige Antwort erstellen
solution: Experience Manager
title: Ping für vollständige Antwort erstellen
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Ping für vollständige Antwort erstellen{#build-the-ping-for-pull-response}

Erstellen Sie die Ping for Pull-Antwort, um aktualisierte Benutzerinformationen an Livefyre zu senden.

| Typ | Eigenschaft | Beschreibung |
|--- |--- |--- |
| Zeichenfolge *erforderlich* | id | Die Benutzer-ID des Benutzers in Ihrem Profilsystem. Dies muss für alle Benutzer in Ihrem Netzwerk eindeutig sein und darf sich nicht ändern. |
| Zeichenfolge *erforderlich* | display_name | Der Anzeigename des Benutzers. Dies wird mit Livefyre-Inhalten gerendert, die vom Benutzer veröffentlicht wurden. |
| Objekt *optional, jedoch empfohlen* | name | Zeichenfolgen zum Definieren der formatierten, ersten, mittleren und letzten Namen des Benutzers. |
| Zeichenfolge *optional, jedoch empfohlen* | E-Mail | User’s email address. Dient zum Senden von E-Mail-Benachrichtigungen. |
| String optional, but recommended ** | image_url | URL to an avatar to display for the user. Livefyre scales uploaded images to 100×100, 75×75, or 50×50 pixels, as appropriate. For best results, users should upload a square image, at 100×100 pixels. To ensure the avatar image is updated in Livefyre, modify the image_url for each image update so Ping for Pull detects that the image was changed. For example, attach a timestamp to the filename or increment the image changes. Hinweis:  All URLs must be fully qualified and accessible. |
| String optional, but recommended ** | profile_url | URL to the user’s profile page on your site. |
| String optional, but recommended ** | settings_url | URL to a page where users may configure the user’s profile settings for your site. |
| Array *optional, jedoch empfohlen* | Tags | Used to assign users to user groups. Tags may include 1-63 alphanumeric and underscore characters. |
| Boolescher Wert *optional, jedoch empfohlen* | autofollow_convertions | Definiert, ob ein Benutzer einer Sammlung nach dem Posten in der Sammlung automatisch folgen möchte. Wenn Benutzer einer Sammlung folgen, erhalten sie E-Mail-Benachrichtigungen, wenn andere Benutzer teilnehmen. Kann wahr oder falsch sein. Der Standardwert ist true. |
| Objekt *optional, jedoch empfohlen* | email_notifications | Definiert die Häufigkeit verfügbarer Livefyre-E-Mail-Benachrichtigungen. Für jeden Benachrichtigungstyp können unterschiedliche Frequenzen festgelegt werden. Standardmäßig werden keine Benachrichtigungen gesendet. <br><ul><li> sofort Benachrichtigungen beim aufgelisteten Ereignis ausgeben. </li><li>gibt oft Benachrichtigungen in Stapeln aus. </li><li> keine E-Mail-Benachrichtigung für die Aktivität senden. </li><li>*Kommentare*: Definiert, wann Benachrichtigungen gesendet werden, wenn andere Benutzer Inhalte in Sammlungen veröffentlichen, denen dieser Benutzer folgt. </li><li>*Antworten*: Definiert, wann Benachrichtigungen gesendet werden, wenn ein anderer Benutzer auf den Inhalt dieses Benutzers antwortet.</li><li>*gefällt*: Definiert, wann Benachrichtigungen gesendet werden, wenn der Inhalt dieses Benutzers einem anderen Benutzer gefällt.</li><li>*moderator_comments*: Definiert, wann Benachrichtigungen an Moderatoren gesendet werden, wenn Benutzer Inhalte an eine Sammlung im Netzwerk posten.</li><li>*moderator_flags*: Definiert, wann Benachrichtigungen an Moderatoren gesendet werden, wenn andere Benutzer Inhalte in einer Sammlung im Netzwerk kennzeichnen.</li></ul> |
| Zeichenfolge *optional* | Position | Ein vom Benutzer gesendeter Speicherort. |
| Zeichenfolge *optional* | bio | Eine vom Benutzer übermittelte Autobiografie. |
| Array *optional* | websites | Ein Array von vom Benutzer übermittelten Sites. Max = 2. |
| Objekt *optional* | display_rules | Defines which profile properties are publicly visible to other users. Each available parameter takes Boolean input true or false. Available parameters:  <br><ul><li>bio </li><li> Position</li><li>  Geschlecht </li><li>nameimage </li><li> remote_profile_url</li></ul> |
| Boolean optional ** | moderator | Defines whether the user has moderator privileges across the network. |
| Boolean optional ** | gravatar_disabled | Defines whether to disable Livefyre’s use of a gravatar if no  image_url is provided. |

## Example Response {#section_uxt_3dd_mz}

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
