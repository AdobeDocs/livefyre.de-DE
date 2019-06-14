---
description: Erstellen Sie die Struktur für die Pull-Anforderung, um Anforderungen für den Zugriff auf Ihr Benutzeridentitätssystem zu erhalten und zu beantworten.
seo-description: Erstellen Sie die Struktur für die Pull-Anforderung, um Anforderungen für den Zugriff auf Ihr Benutzeridentitätssystem zu erhalten und zu beantworten.
seo-title: Abfrageanforderungsstruktur
solution: Experience Manager
title: Abfrageanforderungsstruktur
uuid: bf 6 b 9 e 45-d 08 a -48 e 6-acc 6-e 4 fa 56428 d 25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

---


# Abfrageanforderungsstruktur{#pull-request-structure}

Erstellen Sie die Struktur für die Pull-Anforderung, um Anforderungen für den Zugriff auf Ihr Benutzeridentitätssystem zu erhalten und zu beantworten.

Livefyre sendet eine Pull-Anforderung an Ihre Endpunkt-URL.

Wenn Ihre Endpunkt-Endpunkt-URL beispielsweise:

```
https://example.yoursite.com/some_path/?id={id}
```

Die Livefyre-Pull-Anforderung an diesen Endpunkt lautet:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

Dabei `lftoken` ist ein JSON-Webtoken mit Ihrem Netzwerkschlüssel signiert und **[!UICONTROL {userAuthToken}]** ist das von Livefyre generierte Authentifizierungstoken.

1. Verwenden `lftoken` Sie zum Überprüfen, ob die Anforderungen für das Ping-URL für die Pull-URL gesendet wurden, von Livefyre und nicht von einem böswilligen Agenten.
1. Für alle eingehenden Anforderungen:

   * Stellen Sie sicher, dass die `lftoken` Abfragezeichenfolge für die Anforderung vorhanden ist.
   * Verwenden Sie die `validateLivefyreToken` Methode in den Livefyre-Bibliotheken, um sicherzustellen, `lftoken` dass sie mit Ihrem Netzwerkschlüssel signiert wurde.

   * Wenn nicht `lftoken` vorhanden ist oder die Überprüfung fehlschlägt, darf Ihr Endpunkt nicht mit Profilinformationen antworten. Beantworten Sie stattdessen den Status 403 (Forbidden) und keinen Antwortkörper.

1. `userAuthToken` wird durch die Livefyre `buildUserAuthToken` -Methode für den Benutzer mit der Benutzer-ID &quot;system&quot; generiert. Dieser Benutzer ist der erste Benutzer, der für jedes neue Netzwerk erstellt wurde.
