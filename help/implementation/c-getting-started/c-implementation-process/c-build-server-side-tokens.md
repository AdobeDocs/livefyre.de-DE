---
description: Eine Anleitung zum Erstellen von collectionMeta- und Authentifizierungstoken.
seo-description: Eine Anleitung zum Erstellen von collectionMeta- und Authentifizierungstoken.
seo-title: Serverseitige Tokens erstellen
solution: Experience Manager
title: Serverseitige Tokens erstellen
uuid: 8313f26e-5ceb-414e-a61a-480bb7a8ba66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Serverseitige Tokens erstellen{#build-server-side-tokens}

Eine Anleitung zum Erstellen von collectionMeta- und Authentifizierungstoken.

Das Erstellen der Token, die Livefyre zur Überprüfung von Anforderungen verwendet, stellt sicher, dass nur Sie Aktualisierungen an Ihrem Livefyre-Netzwerk vornehmen können.

## CollectionMeta-Token

Erfahren Sie, wie Sie ein Token erstellen, um neue Konversationen zu erstellen und vorhandene anzuzeigen.

## Auth-Token

Erfahren Sie, wie Sie ein Token für die Authentifizierung von Benutzern erstellen. Dies ist ein notwendiger Schritt im Integrationsprozess, wenn Sie Janrain Capture nicht für die Benutzerverwaltung verwenden.

## Auth-Token des Benutzers {#section_l5l_hwt_bbb}

In diesem Abschnitt wird beschrieben, wie Sie das UserAuth JSON-Objekt generieren, das das Benutzerauthentifizierungstoken erstellt, das zum Anmelden von Benutzern in Ihren Apps erforderlich ist.

Verwenden Sie zum Erstellen des Tokens Ihre bevorzugte Sprachbibliothek, um die folgenden Parameter einzugeben:

| Parameter | Typ | Beschreibung |
|---|---|---|
| networkName | Zeichenfolge *erforderlich* | Der Name des Livefyre-Netzwerks (bereitgestellt von Livefyre). |
| networkKey | Zeichenfolge *erforderlich* | Der geheime Schlüssel für dieses spezifische Netzwerk (bereitgestellt von Livefyre). |
| userId | Zeichenfolge *erforderlich* | Die ID des Benutzers, der sich anmeldet, wie in Ihrem Benutzerverwaltungssystem gespeichert (nur alphanumerische Zeichen, Bindestriche, Unterstriche und Punktzeichen sind zulässig: `[a-zA-Z0-9_-.]`). **** Hinweis: Die userId muss eindeutig sein. |
| expires | Ganzzahl *erforderlich* | Wenn das Token von jetzt an ablaufen soll (in Sekunden). **** Hinweis: Dieser Wert kann auch als Float übergeben werden. Der erzeugte JSON-Webtoken speichert diesen Wert in UNIX Epochenzeit. |
| displayName | Zeichenfolge *erforderlich* | Text zur Identifizierung dieses Benutzers in der Benutzeroberfläche und in Kommentaren. (Höchstanzahl Zeichen: 50.) |

