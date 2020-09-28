---
description: Verwenden Sie JavaScript-Ereignisse, um auf Ereignisse zu warten, die in einer Medienmanschette auftreten, und diese an das Analysetool Ihrer Wahl zu senden.
seo-description: Verwenden Sie JavaScript-Ereignisse, um auf Ereignisse zu warten, die in einer Medienmanschette auftreten, und diese an das Analysetool Ihrer Wahl zu senden.
seo-title: JavaScript-Ereignisse für Medienwall
solution: Experience Manager
title: JavaScript-Ereignisse für Medienwall
uuid: 8afc0529-4640-476a-b207-91b2c70101f0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# JavaScript-Ereignisse für Medienwall{#javascript-events-for-media-wall}

Verwenden Sie JavaScript-Ereignisse, um auf Ereignisse zu warten, die in einer Medienmanschette auftreten, und diese an das Analysetool Ihrer Wahl zu senden.

Livefyre bietet JavaScript-Ereignisse zur Verfolgung von Benutzeraktivitäten in Ihren Livefyre-Apps. Beispielsweise können Sie die Seite aktualisieren, wenn Benutzer Inhalte auf Twitter oder Facebook teilen oder wenn neue Inhalte veröffentlicht werden.

Hier ist ein Beispiel, wie die Ereignisse empfangen werden. Ersetzen Sie `console.log` durch Ihren Code, um das Ereignis Ihrer Analytics-Integration zuzuordnen und zu senden (dynamisches Tag-Management, Adobe Analytics JS, Google Analytics usw.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Liste der unterstützten Media Wall-Ereignisse:

## Medienwall-Ereignisse

| Ereignis | Definition |
|---|---|
| `Init` | Wenn eine Medienwall auf einer Seite enthalten ist. |
| `Load` | Wenn die Medienmanagerseite unabhängig von der Position auf einer Seite geladen wurde. |
| `PostButtonClick` | Wenn ein Benutzer auf eine Schaltfläche "Hochladen"auf einer Medienplatine klickt. |
| `RequestMore` | Wenn der Benutzer mehr Inhalte in eine Medienmanagerei lädt. |
| `TwitterReplyClick` | Wenn ein Benutzer auf die Schaltfläche "Twitter-Antwort"von der Medienmanagerfläche klickt. |
| `TwitterRetweetClick` | Wenn ein Benutzer auf die Schaltfläche "Twitter-Retweet"von der Medienkonsole klickt. |
| `TwitterLikeClick` | Wenn ein Benutzer auf die Schaltfläche "Gefällt mir"-Klicks/Favoriten in Twitter von der Medienkonsole aus klickt. |
| `ModalView` | Wenn der Benutzer klickt, um Media Pinnwand-Inhalte in einem größeren modalen Fenster anzuzeigen. |
| `Like` | Wenn ein Benutzer auf der Medienmanagerseite auf die Schaltfläche "Gefällt mir"klickt. |
| `ShareButtonClick` | Jedes Mal, wenn ein Benutzer auf die Schaltfläche "Freigeben"auf einer Medienwall-Karte klickt. |
| `ShareURL` | Wenn der Textbereich "Mit URL teilen"ausgewählt/aus der Medienmauer kopiert wird. |
| `ShareFacebook` | Wenn auf "Auf Facebook teilen"aus der Medienmauer geklickt wird. |
| `ShareTwitter` | Wenn auf "Mit Twitter teilen"von der Medienmauer aus geklickt wird. |
