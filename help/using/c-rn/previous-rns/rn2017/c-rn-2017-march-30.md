---
description: Versionshinweise für die Version vom 30. März 2017.
seo-description: Versionshinweise für die Version vom 30. März 2017.
seo-title: 30. März 2017
title: 30. März 2017
uuid: 2adf04a9-6c52-4fa1-a0c9-b2d3886305e9
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# March 30, 2017{#march}

Versionshinweise für die Version vom 30. März 2017.

## Produktionsversion

| Art des Problems | Komponente | Versionshinweise |
|---|---|---|
| Fehler | Social-Suche | Es wurde ein Fehler behoben, durch den in Social Search gespeicherte YouTube-Assets nicht veröffentlicht werden konnten. |
| Verbesserung | Social-Synchronisierung | Veraltete Twitter Social-Synchronisierung. |
| Verbesserung | Storify 2 | Es wurde eine Verbesserung hinzugefügt, um die Meldung "Keine Ergebnisse gefunden"bei der Suche nach Facebook-Themen anzuzeigen, wenn keine Ergebnisse gefunden wurden. |
| Verbesserung | Streams | Zusammenfassungsregeln für SAFE-Regeln wurden am Ende einer Twitter-Stream-Seite hinzugefügt. |
| Fehler | Streams | Es wurde eine Verbesserung hinzugefügt, um das Kontrollkästchen "verifizierter Benutzer"in Twitter-Stream-Regeln sichtbar zu deaktivieren, wenn ausgeschlossene Autoren bereitgestellt werden. |
| Fehler | Streams | Es wurde ein Fehler behoben, durch den die Verwendung von UNDing-Suchbegriffen und ein Standortfilter in einer Twitter-Regel zugelassen wurden. |
| Fehler | Studio | Es wurde ein Fehler behoben, der verhinderte, dass das "Feature-Tag" bei Anwendung korrekt gespeichert wurde. |

## UAT-Version

| Art des Problems | Komponente | Versionshinweise |
|---|---|---|
| Fehler | App-Inhalt | Das Verhalten von "Mehr Info"wurde dahingehend geändert, dass das früheste Ereignis immer angezeigt wird, wenn mehrere anonyme Flag-Ereignisse für einen bestimmten Inhalt vorhanden sind. |
| Fehler | Bibliothek | Es wurde ein Fehler behoben, durch den Bibliothekssuchen mit Hashtags gelegentlich fehlschlugen. |
| Fehler | Karten | Es wurde ein Fehler in "Maps"behoben, durch den eine große Anzahl von Inhalten in Clustern auf iOS-Geräten unterstützt wurde. |
| Verbesserung | Mosaik | Es wurde die Möglichkeit hinzugefügt, Mosaic-Apps so zu konfigurieren, dass sie an einer beliebigen Stelle auf einer Inhaltskarte klicken, um das Modell nach Animationstyp `none` in Designer zu öffnen und `cardAnimation: 'off'`wenn es über das SDK instanziiert wird. |
| Fehler | Mosaik | Es wurde ein Fehler behoben, durch den Benutzer erfolgreich Änderungen an Mosaic-Apps in Designer vornehmen konnten. |
| Verbesserung | Berechtigungsanforderung | Es wurde ein neuer Anforderungsstatus mit der Bezeichnung "Anforderung fehlgeschlagen"hinzugefügt, der markiert, wenn Anforderungsmeldungen für Rechte nicht gesendet werden können. |
| Verbesserung | Einstellungen | Kunden können nun Spam-Moderationsregeln in den Einstellungen erstellen. |
| Verbesserung | Social-Suche | Es wurde ein Fehler behoben, durch den VK.com-Beiträge nicht über URL Social-Suchen angezeigt wurden. |
| Verbesserung | Social-Suche | Wenn die Suche nach Instagram-Inhalten aus Studio aufgrund eines abgelaufenen Instagram API-Tokens erfolgt, wird die Fehlermeldung jetzt als solche angezeigt. |
| Fehler | Streams | Es wurde ein Fehler behoben, der dazu führte, dass das Banner "App akzeptiert keinen neuen Inhalt"fälschlicherweise auf den Stream-Regelseiten angezeigt wurde. |
| Verbesserung | Streams | Die Standardeinstellung neu erstellter Stream-Regeln wurde dahingehend geändert, dass SAFE-Regeln angewendet werden, wenn zutreffend. |
| Verbesserung | Streams (zuvor kuratiert) | Die Option "Nur Reben"wurde aus den Twitter-Stream-/Kuratierungsregeln entfernt, da Reben jetzt als Twitter-Videos angezeigt werden. |
| Fehler | Studio-Shell | Es wurde ein Fehler behoben, durch den Livefyre Studio geladen wird, wenn https:// explizit der URL vorangestellt wurde. |

