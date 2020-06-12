---
description: Livefyre verwendet eine PUSH-Schnittstelle, um externe Systeminformationen über Änderungen an Benutzerberechtigungen zu senden.
seo-description: Livefyre verwendet eine PUSH-Schnittstelle, um externe Systeminformationen über Änderungen an Benutzerberechtigungen zu senden.
seo-title: Veröffentlichen von Benutzerberechtigungen auf externen Systemen (optional)
solution: Experience Manager
title: Veröffentlichen von Benutzerberechtigungen auf externen Systemen (optional)
uuid: 9c18b20d-3b93-4666-b7de-1ec60318cf88
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---


# Veröffentlichen von Benutzerberechtigungen auf externen Systemen (optional){#posting-user-permissions-to-external-systems-optional}

Livefyre verwendet eine PUSH-Schnittstelle, um externe Systeminformationen über Änderungen an Benutzerberechtigungen zu senden.

## Typen von Benutzern in Livefyre Studio

| Benutzertyp | Beschreibung |
|--- |--- |
| owner | Dieser Benutzer ist Eigentümer und kann sowohl Inhalte moderieren als auch neue Moderatoren zuweisen. |
| admin | Dieser Benutzer ist Moderator und kann Inhalte moderieren. |
| Mitglied | Dieser Benutzer ist zulässig. Gepostete Inhalte werden nicht durch Spam- oder Profitabilität-Filter weitergeleitet und erfordern keine Genehmigung in vormoderierten Streams. |
| Keine | Dieser Benutzer ist ein Standardbenutzer und hat keine speziellen Berechtigungen. |
| outcast | Dieser Benutzer wurde von der Teilnahme an Unterhaltungen ausgeschlossen. |

Um Benutzerberechtigungen für externe Systeme zu veröffentlichen, müssen Sie eine URL registrieren, die Berechtigungsdaten als POST-Anforderungen erhält.

Beispiel:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parameter | Beschreibung |
|--- |--- |
| networkName | Ihr Livefyre hat den Netzwerknamen angegeben. |
| token | Gültiges System-Token. |
| url | Zu registrierende URL. |

Die registrierte URL sollte POSTs mit den folgenden Daten als Inhaltstyp akzeptieren: application/x-www-form-urlencoded.

| Parameter | Beschreibung |
|--- |--- |
| jid | JID des Benutzers, dessen Verbindung geändert wird. Eine JID ist eine Zeichenfolge im Formular `user_id@network`. |
| Mitgliedschaft | Name der zugewiesenen Berechtigungen, die einer der folgenden sein müssen:  `{admin | member | none | outcast | owner}` |

Weitere Informationen zum Aktualisieren der Einstellungen für die Benutzerzugehörigkeit finden Sie in der [Hinzufügen Benutzerzuordnungs-API-Referenz](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
