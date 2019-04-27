---
description: In diesem Abschnitt wird beschrieben, wie Sie das JSON-Objekt "userauth" generieren, das das Token für die Benutzerauthentifizierung erstellt, das zum Protokollieren von Benutzern in Ihren Apps erforderlich ist.
seo-description: In diesem Abschnitt wird beschrieben, wie Sie das JSON-Objekt "userauth" generieren, das das Token für die Benutzerauthentifizierung erstellt, das zum Protokollieren von Benutzern in Ihren Apps erforderlich ist.
seo-title: Benutzerauthentifizierungstoken
solution: Experience Manager
title: Benutzerauthentifizierungstoken
uuid: 6483 debd -453 c -4780-b 19 c -1 d 8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Benutzerauthentifizierungstoken{#user-auth-token}

In diesem Abschnitt wird beschrieben, wie Sie das JSON-Objekt &quot;userauth&quot; generieren, das das Token für die Benutzerauthentifizierung erstellt, das zum Protokollieren von Benutzern in Ihren Apps erforderlich ist.

In diesem Abschnitt wird beschrieben, wie Sie das JSON-Objekt &quot;userauth&quot; generieren, das das Token für die Benutzerauthentifizierung erstellt, das zum Protokollieren von Benutzern in Ihren Apps erforderlich ist.

Um das Token zu erstellen, verwenden Sie die bevorzugte Sprachbibliothek, um die folgenden Parameter zu übermitteln:

| Parameter | Typ | Beschreibung |
|---|---|---|
| Networkname | Zeichenfolge *erforderlich* | Der Name des Livefyre-Netzwerks (von Livefyre bereitgestellt). |
| Networkkey | Zeichenfolge *erforderlich* | Der geheime Schlüssel für dieses spezifische Netzwerk (von Livefyre bereitgestellt). |
| Userid | Zeichenfolge *erforderlich* | Die ID des Benutzers, der im Benutzerverwaltungssystem gespeichert ist (nur alphanumerische, Bindestrich, Unterstrich und Punktzeichen sind zulässig): [a-zA-Z 0-9_-.]). **Hinweis:** Die userid muss eindeutig sein. |
| läuft ab | Ganzzahl *erforderlich* | Wenn das Token ab sofort ablaufen sollte (in Sekunden). **Hinweis:** Dieser Wert kann auch als float weitergegeben werden. Das erzeugte JSON-Webtoken speichert diesen Wert in der UNIX-Epoche. |
| Displayname | Zeichenfolge *erforderlich* | Text, der diesen Benutzer in der Benutzeroberfläche und in den Kommentaren identifiziert. (Maximale Anzahl von Zeichen: 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## Nodejs {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>Netzwerkschlüssel werden für Livefyre-Demosite-Konten nicht freigegeben. Sie erhalten einen Netzwerkschlüssel, nachdem Livefyre eine Umgebung für Sie bereitgestellt hat. Dieser Schlüssel sollte privat sein.

