---
description: In diesem Abschnitt wird beschrieben, wie Sie das UserAuth JSON-Objekt generieren, das das Benutzerauthentifizierungstoken erstellt, das zum Anmelden von Benutzern in Ihren Apps erforderlich ist.
title: Auth-Token des Benutzers
exl-id: 564144dd-6db4-447b-80ac-b743ecac833d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 2%

---

# Benutzerautom.-Token{#user-auth-token}

In diesem Abschnitt wird beschrieben, wie Sie das UserAuth JSON-Objekt generieren, das das Benutzerauthentifizierungstoken erstellt, das zum Anmelden von Benutzern in Ihren Apps erforderlich ist.

In diesem Abschnitt wird beschrieben, wie Sie das UserAuth JSON-Objekt generieren, das das Benutzerauthentifizierungstoken erstellt, das zum Anmelden von Benutzern in Ihren Apps erforderlich ist.

Verwenden Sie zum Erstellen des Tokens Ihre bevorzugte Sprachbibliothek, um die folgenden Parameter einzugeben:

| Parameter | Typ | Beschreibung |
|---|---|---|
| networkName | Zeichenfolge *erforderlich* | Der Name des Livefyre-Netzwerks (bereitgestellt von Livefyre). |
| networkKey | Zeichenfolge *erforderlich* | Der geheime Schlüssel für dieses spezifische Netzwerk (bereitgestellt von Livefyre). |
| userId | Zeichenfolge *erforderlich* | Die ID des Benutzers, der sich anmeldet, wie in Ihrem Benutzerverwaltungssystem gespeichert (nur alphanumerische Zeichen, Bindestriche, Unterstriche und Punktzeichen sind zulässig: [a-zA-Z0-9_-.]). **Hinweis:** Die userId muss eindeutig sein. |
| expires | Integer *required* | Wenn das Token von jetzt an ablaufen soll (in Sekunden). **Hinweis:** Dieser Wert kann auch als Fließkomma übergeben werden. Der erzeugte JSON-Webtoken speichert diesen Wert in UNIX Epochenzeit. |
| displayName | Zeichenfolge *erforderlich* | Text zur Identifizierung dieses Benutzers in der Benutzeroberfläche und in Kommentaren. (Höchstanzahl Zeichen: 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

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
>Netzwerkschlüssel werden für Livefyre-Demosite-Konten nicht freigegeben. Sie erhalten einen Netzwerkschlüssel, sobald Livefyre eine Umgebung für Sie bereitgestellt hat. Dieser Schlüssel sollte privat aufbewahrt werden.
