---
description: Erstellen Sie die Pull-Anforderungsstruktur, um Anforderungen für den Zugriff auf Ihr Benutzeridentitätssystem zu empfangen und zu beantworten.
title: Anforderungsstruktur abrufen
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

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

wobei `lftoken` ein JSON-WebToken ist, das mit Ihrem Netzwerkschlüssel signiert wurde, und **[!UICONTROL {userAuthToken}]** das von Livefyre generierte Benutzerauth-Token ist.

1. Verwenden Sie `lftoken`, um zu überprüfen, dass Anfragen an Ihren Ping für die Pull-URL von Livefyre gesendet wurden und nicht von einem böswilligen Agenten.
1. Für alle eingehenden Anforderungen:

   * Stellen Sie sicher, dass die `lftoken`-Abfrage-Zeichenfolge in der Anforderung vorhanden ist.
   * Verwenden Sie die Methode `validateLivefyreToken` in den Livefyre-Bibliotheken, um sicherzustellen, dass `lftoken` mit Ihrem Netzwerkschlüssel signiert wurde.

   * Wenn `lftoken` nicht vorhanden ist oder die Überprüfung fehlschlägt, lassen Sie nicht zu, dass Ihr Endpunkt mit Profil-Informationen reagiert. Antworten Sie stattdessen mit einem Statuscode des Typs 403 (Verboten) und ohne Antworttext.

1. `userAuthToken` wird von der Livefyre- `buildUserAuthToken` Methode für den Benutzer mit der Benutzer-ID &quot;system&quot;generiert. Dieser Benutzer ist der erste Benutzer, der für jedes neue Netzwerk erstellt wurde.
