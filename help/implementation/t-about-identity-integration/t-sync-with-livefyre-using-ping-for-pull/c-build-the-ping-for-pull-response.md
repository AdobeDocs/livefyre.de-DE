---
description: Erstellen Sie das Ping für die Antwort, um aktualisierte Benutzerinformationen
  auf Livefyre zu übertragen.
seo-description: Erstellen Sie das Ping für die Antwort, um aktualisierte Benutzerinformationen
  auf Livefyre zu übertragen.
seo-title: Ping für Pull-Antwort erstellen
solution: Experience Manager
title: Ping für Pull-Antwort erstellen
uuid: f 90871 d 5-601 f -40 dc-b 3 d 2-ab 78635 e 4 a 88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Ping für Pull-Antwort erstellen{#build-the-ping-for-pull-response}

Erstellen Sie das Ping für die Antwort, um aktualisierte Benutzerinformationen auf Livefyre zu übertragen.

| Typ | Eigenschaft | Beschreibung |
|--- |--- |--- |
| Zeichenfolge *erforderlich* | id | Die Benutzer-ID des Benutzers in Ihrem Profilsystem. Dies muss für alle Benutzer in Ihrem Netzwerk eindeutig sein und darf sich niemals ändern. |
| Zeichenfolge *erforderlich* | display_ name | Der Anzeigename des Benutzers. Dies wird mit dem vom Benutzer veröffentlichten Livefyre-Inhalt wiedergegeben. |
| Objekt *optional, empfohlen jedoch* | name | Zeichenfolgen zum Definieren der formatierten, ersten, mittleren und Nachnamen des Benutzers. |
| Zeichenfolge *optional, empfohlen jedoch empfohlen* | E-Email | E-Mail-Adresse des Benutzers. Wird zum Senden von E-Mail-Benachrichtigungen verwendet. |
| Zeichenfolge *optional, empfohlen jedoch empfohlen* | image_ url | URL zu einem Avatar, der für den Benutzer angezeigt werden soll. Livefyre skaliert hochgeladene Bilder je nach Bedarf auf 100 x 100, 75 x 75 oder 50 x 50 Pixel. Um optimale Ergebnisse zu erzielen, sollten Benutzer ein quadratisches Bild von 100 x 100 Pixeln hochladen. Um sicherzustellen, dass das Avatar-Bild in Livefyre aktualisiert wird, ändern Sie die image_ url für jedes Bild-Update, sodass Ping für Pull erkennt, dass das Bild geändert wurde. Fügen Sie dem Dateinamen beispielsweise einen Zeitstempel hinzu oder erhöhen Sie das Bild. Hinweis: Alle urls müssen voll qualifiziert und zugänglich sein. |
| Zeichenfolge *optional, empfohlen jedoch empfohlen* | profile_ url | URL zur Profilseite des Benutzers auf Ihrer Site. |
| Zeichenfolge *optional, empfohlen jedoch empfohlen* | settings_ url | URL zu einer Seite, auf der Benutzer die Profileinstellungen des Benutzers für Ihre Site konfigurieren können. |
| Array *optional, empfohlen jedoch* | Tags | Dient zum Zuweisen von Benutzern zu Benutzergruppen. Tags können 1-63 alphanumerische Zeichen und Unterstriche enthalten. |
| Boolescher Wert *optional, empfohlen* | auto autofollow_ talking conversations | Legt fest, ob ein Benutzer einer Sammlung nach dem Posten automatisch folgen möchte. Bei einer Sammlung erhalten Benutzer E-Email-Benachrichtigungen, wenn andere Benutzer teilnehmen. Kann wahr oder falsch sein. Der Standardwert ist "true" . |
| Objekt *optional, empfohlen jedoch* | email_ notifications | Definiert die Häufigkeit der verfügbaren Livefyre-E-Email-Benachrichtigungen. Für jeden Benachrichtigungstyp können unterschiedliche Frequenzen festgelegt werden. Standardmäßig werden keine Benachrichtigungen gesendet. <br><ul><li> Benachrichtigungen unmittelbar nach dem aufgelisteten Ereignis umgehend benachrichtigt. </li><li>häufig Benachrichtigungen in Stapeln aufrufen. </li><li> wird niemals E-Email-Benachrichtigungen für die Aktivität gesendet. </li><li>*Kommentare*: Definiert, wann Benachrichtigungen gesendet werden, wenn andere Benutzer Inhalte in Sammlungen veröffentlichen, denen dieser Benutzer folgt. </li><li>*Antworten*: Definiert, wann Benachrichtigungen gesendet werden, wenn ein anderer Benutzer auf den Inhalt dieses Benutzers antwortet.</li><li>*" Gefällt mir"*-Klicks: Definiert, wann Benachrichtigungen gesendet werden, wenn ein anderer Benutzer den Inhalt dieses Benutzers angibt.</li><li>*moderator_ comments*: Definiert, wann Benachrichtigungen an Moderatoren gesendet werden, wenn Benutzer Inhalte für eine Sammlung im Netzwerk veröffentlichen.</li><li>*moderator_ flags*: Definiert, wann Benachrichtigungen an Moderatoren gesendet werden, wenn andere Benutzer Inhalte in einer Sammlung im Netzwerk kennzeichnen.</li></ul> |
| *Zeichenfolge optional* | Ort | Ein vom Benutzer gesendeter Speicherort. |
| *Zeichenfolge optional* | biografisch | Eine vom Benutzer übermittelte automatische Biografie. |
| Array *optional* | Websites | Ein Array von Benutzern gesendeten Sites. Max. = 2. |
| Objekt *optional* | display_ rules | Definiert, welche Profileigenschaften für andere Benutzer öffentlich sichtbar sind. Jeder verfügbare Parameter akzeptiert boolesche Eingaben true oder false. Verfügbare Parameter: <br><ul><li>biografisch </li><li> Ort</li><li>  Geschlecht </li><li>nameimage </li><li> remote_ profile_ url</li></ul> |
| *Boolescher Wert* | Moderator | Definiert, ob der Benutzer über Moderatorberechtigungen für das Netzwerk verfügt. |
| *Boolescher Wert* | gravatar_ disabled | Definiert, ob die Verwendung eines Gravars von Livefyre deaktiviert wird, wenn keine image_ url angegeben ist. |

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
