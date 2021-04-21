---
description: Versionshinweise für die Version vom 30. März 2017.
title: 30. März 2017
exl-id: 44c73ff9-8bc1-49c9-b720-aff425e5cd28
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 6%

---

# 30. März 2017{#march}

Versionshinweise für die Version vom 30. März 2017.

## Produktionsversion

| Art des Problems | Komponente | Versionshinweise |
|---|---|---|
| Fehler | Social-Suche | Es wurde ein Fehler behoben, durch den in Social Search gespeicherte YouTube-Assets nicht veröffentlicht werden konnten. |
| Verbesserung | Social-Synchronisierung | Die Twitter Social-Synchronisierung wurde eingestellt. |
| Verbesserung | Storify 2 | Es wurde eine Verbesserung hinzugefügt, um die Meldung &quot;Keine Ergebnisse gefunden&quot;bei der Facebook-Themensuche anzuzeigen, wenn keine Ergebnisse gefunden wurden. |
| Verbesserung | Streams | Zusammenfassungsregeln für SAFE-Regeln wurden am Ende einer Twitter-Stream-Seite hinzugefügt. |
| Fehler | Streams | Es wurde eine Verbesserung zur sichtbaren Deaktivierung des Kontrollkästchens &quot;Geprüfter Benutzer&quot;in den Twitter-Stream-Regeln hinzugefügt, wenn ausgeschlossene Autoren bereitgestellt werden. |
| Fehler | Streams | Es wurde ein Fehler behoben, durch den die Verwendung von ANDing-Suchbegriffen und ein Standortfilter in einer Twitter-Regel zugelassen werden konnte. |
| Fehler | Studio | Es wurde ein Fehler behoben, der verhinderte, dass das &quot;Feature-Tag&quot; bei Anwendung korrekt gespeichert wurde. |

## UAT-Version

| Art des Problems | Komponente | Versionshinweise |
|---|---|---|
| Fehler | App-Inhalt | Das Verhalten von &quot;Mehr Info&quot;wurde dahingehend geändert, dass das früheste Ereignis immer angezeigt wird, wenn mehrere anonyme Flag-Ereignis für einen bestimmten Inhalt vorhanden sind. |
| Fehler | Bibliothek | Es wurde ein Fehler behoben, durch den Bibliothekssuchen mit Hashtags gelegentlich fehlschlugen. |
| Fehler | Karten | Es wurde ein Fehler in &quot;Maps&quot;behoben, durch den eine große Anzahl von Inhalten in Clustern auf iOS-Geräten unterstützt wurde. |
| Verbesserung | Mosaik | Es wurde die Möglichkeit hinzugefügt, Mosaic-Apps so zu konfigurieren, dass sie an einer beliebigen Stelle auf einer Inhaltskarte klicken, um das Modell nach Animationstyp `none` in Designer und `cardAnimation: 'off'`zu öffnen, falls es über das SDK instanziiert wird. |
| Fehler | Mosaik | Es wurde ein Fehler behoben, durch den Benutzer erfolgreich Änderungen an Mosaic-Apps in Designer vornehmen konnten. |
| Verbesserung | Berechtigungsanforderung | Es wurde ein neuer Anforderungsstatus mit der Bezeichnung &quot;Anforderung fehlgeschlagen&quot;hinzugefügt, der markiert, wenn Anforderungsmeldungen für Rechte nicht gesendet werden können. |
| Verbesserung | Einstellungen | Kunden können nun Spam-Moderationsregeln in den Einstellungen erstellen. |
| Verbesserung | Social-Suche | Es wurde ein Fehler behoben, durch den VK.com-Beiträge nicht über URL Social-Suchen angezeigt wurden. |
| Verbesserung | Social-Suche | Wenn die Suche nach Instagram-Inhalten aus Studio aufgrund eines abgelaufenen Instagram API-Tokens erfolgt, wird die Fehlermeldung jetzt als solche angezeigt. |
| Fehler | Streams | Es wurde ein Fehler behoben, der dazu führte, dass das Banner &quot;App akzeptiert keinen neuen Inhalt&quot;fälschlicherweise auf den Stream-Regelseiten angezeigt wurde. |
| Verbesserung | Streams | Die Standardeinstellung neu erstellter Stream-Regeln wurde dahingehend geändert, dass SAFE-Regeln angewendet werden, wenn zutreffend. |
| Verbesserung | Streams (früher &quot;Kuratieren von Regeln&quot;) | Die Option &quot;Nur Reben&quot;wurde aus den Twitter-Stream-/Kuratierungsregeln entfernt, da Reben jetzt als Twitter-Videos angezeigt werden. |
| Fehler | Studio-Shell | Es wurde ein Fehler behoben, durch den Livefyre Studio geladen wird, wenn https:// explizit der URL vorangestellt wurde. |
