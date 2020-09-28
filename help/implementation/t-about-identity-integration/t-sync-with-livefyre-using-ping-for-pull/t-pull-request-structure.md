---
description: Erstellen Sie die Pull-Anforderungsstruktur, um Anforderungen für den Zugriff auf Ihr Benutzeridentitätssystem zu empfangen und zu beantworten.
seo-description: Erstellen Sie die Pull-Anforderungsstruktur, um Anforderungen für den Zugriff auf Ihr Benutzeridentitätssystem zu empfangen und zu beantworten.
seo-title: Anforderungsstruktur abrufen
solution: Experience Manager
title: Anforderungsstruktur abrufen
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

---


# Anforderungsstruktur abrufen{#pull-request-structure}

Erstellen Sie die Pull-Anforderungsstruktur, um Anforderungen für den Zugriff auf Ihr Benutzeridentitätssystem zu empfangen und zu beantworten.

Livefyre gibt eine Pull-Anforderung an Ihre Endpunkt-URL aus.

Wenn Ihre Pull-Endpunkt-URL beispielsweise wie folgt lautet:

```
https://example.yoursite.com/some_path/?id={id}
```

Die Livefyre Pull-Anforderung an diesen Endpunkt lautet:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

Dabei `lftoken` handelt es sich um ein JSON-WebToken, das mit Ihrem Netzwerkschlüssel signiert wurde, und **[!UICONTROL {userAuthToken}]** um das von Livefyre generierte Benutzerauth-Token.

1. Verwenden Sie `lftoken` zur Überprüfung, dass Anfragen an Ihre Ping für die Pull-URL von Livefyre gesendet wurden und nicht von einem böswilligen Agenten.
1. Für alle eingehenden Anforderungen:

   * Stellen Sie sicher, dass die `lftoken` Abfragezeichenfolge in der Anforderung vorhanden ist.
   * Verwenden Sie die `validateLivefyreToken` Methode in den Livefyre-Bibliotheken, um sicherzustellen, dass sie mit Ihrem Netzwerkschlüssel signiert `lftoken` wurden.

   * Wenn `lftoken` die Überprüfung nicht oder nicht erfolgreich ist, lassen Sie nicht zu, dass Ihr Endpunkt mit Profilinformationen reagiert. Antworten Sie stattdessen mit einem Statuscode des Typs 403 (Verboten) und ohne Antworttext.

1. `userAuthToken` wird von der Livefyre- `buildUserAuthToken` Methode für den Benutzer mit der Benutzer-ID "system"generiert. Dieser Benutzer ist der erste Benutzer, der für jedes neue Netzwerk erstellt wurde.
