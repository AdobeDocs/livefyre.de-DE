---
description: Ein Handbuch zum Erstellen von collectionmeta und Auth-Token.
seo-description: Ein Handbuch zum Erstellen von collectionmeta und Auth-Token.
seo-title: Serverseitige Tokens erstellen
solution: Experience Manager
title: Serverseitige Tokens erstellen
uuid: 8313 f 26 e -5 ceb -414 e-a 61 a -480 bb 7 a 8 ba 66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Serverseitige Tokens erstellen{#build-server-side-tokens}

Ein Handbuch zum Erstellen von collectionmeta und Auth-Token.

Durch Erstellen der Tokens, die von Livefyre zur Überprüfung von Anforderungen verwendet werden, wird sichergestellt, dass nur Sie Änderungen an Ihrem Livefyre-Netzwerk vornehmen können.

## Collectionmeta Token

Erfahren Sie, wie Sie ein Token erstellen, um neue Unterhaltungen zu erstellen und anzuzeigen.

## Auth Token

Hier erfahren Sie, wie Sie ein Token zur Authentifizierung von Benutzern erstellen, ein notwendiger Schritt im Integrationsprozess, wenn Sie Janrain Capture nicht für die Benutzerverwaltung verwenden.

## Benutzerauthentifizierungstoken {#section_l5l_hwt_bbb}

In diesem Abschnitt wird beschrieben, wie Sie das JSON-Objekt &quot;userauth&quot; generieren, das das Token für die Benutzerauthentifizierung erstellt, das zum Protokollieren von Benutzern in Ihren Apps erforderlich ist.

Um das Token zu erstellen, verwenden Sie die bevorzugte Sprachbibliothek, um die folgenden Parameter zu übermitteln:

| Parameter | Typ | Beschreibung |
|---|---|---|
| Networkname | Zeichenfolge *erforderlich* | Der Name des Livefyre-Netzwerks (von Livefyre bereitgestellt). |
| Networkkey | Zeichenfolge *erforderlich* | Der geheime Schlüssel für dieses spezifische Netzwerk (von Livefyre bereitgestellt). |
| Userid | Zeichenfolge *erforderlich* | Die ID des Benutzers, der im Benutzerverwaltungssystem gespeichert ist (nur alphanumerische, Bindestrich, Unterstrich und Punktzeichen sind zulässig): `[a-zA-Z0-9_-.]`). **Hinweis:** Die userid muss eindeutig sein. |
| läuft ab | Ganzzahl *erforderlich* | Wenn das Token ab sofort ablaufen sollte (in Sekunden). **Hinweis:** Dieser Wert kann auch als float weitergegeben werden. Das erzeugte JSON-Webtoken speichert diesen Wert in der UNIX-Epoche. |
| Displayname | Zeichenfolge *erforderlich* | Text, der diesen Benutzer in der Benutzeroberfläche und in den Kommentaren identifiziert. (Maximale Anzahl von Zeichen: 50.) |

