---
description: Livefyre verwendet eine PUSH-Schnittstelle, um externe Systeminformationen
  über Änderungen an Benutzerberechtigungen zu senden.
seo-description: Livefyre verwendet eine PUSH-Schnittstelle, um externe Systeminformationen
  über Änderungen an Benutzerberechtigungen zu senden.
seo-title: Veröffentlichen von Benutzerberechtigungen für externe Systeme (optional)
solution: Experience Manager
title: Veröffentlichen von Benutzerberechtigungen für externe Systeme (optional)
uuid: 9 c 18 b 20 d -3 b 93-4666-b 7 de -1 ec 60318 cf 88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Veröffentlichen von Benutzerberechtigungen für externe Systeme (optional){#posting-user-permissions-to-external-systems-optional}

Livefyre verwendet eine PUSH-Schnittstelle, um externe Systeminformationen über Änderungen an Benutzerberechtigungen zu senden.

## Benutzertypen in Livefyre Studio

| Benutzertyp | Beschreibung |
|--- |--- |
| Eigentümer | Dieser Benutzer ist ein Inhaber und kann sowohl Inhalte moderieren als auch neue Moderatoren zuweisen. |
| admin | Dieser Benutzer ist ein Moderator und kann Inhalte moderieren. |
| member | Dieser Benutzer wird in die Positivliste eingetragen. Gepostete Inhalte werden weder Spam noch Gewinn-Filter durchlaufen und erfordern keine Genehmigung in vorab moderierten Streams. |
| none | Dieser Benutzer ist ein Standardbenutzer und hat keine besonderen Berechtigungen. |
| outcast | Dieser Benutzer wurde daran gehindert, an Unterhaltungen teilzunehmen. |

Um Benutzerberechtigungen für externe Systeme zu veröffentlichen, müssen Sie eine URL registrieren, die Berechtigungen als POST-Anforderungen erhält.

Beispiel:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parameter | Beschreibung |
|--- |--- |
| Networkname | Ihr Livefyre-bereitgestellter Netzwerkname. |
| Token | Gültiges System-Token. |
| url | URL zur Registrierung. |

Die registrierte URL akzeptiert POSTS mit den folgenden Daten als Inhaltstyp: application/x-www-form-urlencoded.

| Parameter | Beschreibung |
|--- |--- |
| jid | JID des Benutzers, dessen Affiliation geändert wird. Eine JID ist eine Zeichenfolge des Formulars `user_id@network`. |
| affiliation | Der Name der zugewiesenen Berechtigungen, die einer der folgenden sein müssen: `{admin | member | none | outcast | owner}` |

Weitere Informationen zum Aktualisieren von Benutzeraffiliationseinstellungen finden Sie in [der API-Referenz zur Benutzeraffiliation hinzufügen](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
