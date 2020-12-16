---
description: Verwenden Sie JavaScript-Ereignis, um auf Ereignis zu warten, die in einer Medienmanschette auftreten, und diese an das Analysetool Ihrer Wahl zu senden.
seo-description: Verwenden Sie JavaScript-Ereignis, um auf Ereignis zu warten, die in einer Medienmanschette auftreten, und diese an das Analysetool Ihrer Wahl zu senden.
seo-title: JavaScript-Ereignisse für Media Wall
solution: Experience Manager
title: JavaScript-Ereignisse für Media Wall
uuid: 8afc0529-4640-476a-b207-91b2c70101f0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# JavaScript-Ereignis für Media Wall{#javascript-events-for-media-wall}

Verwenden Sie JavaScript-Ereignis, um auf Ereignis zu warten, die in einer Medienmanschette auftreten, und diese an das Analysetool Ihrer Wahl zu senden.

Livefyre bietet JavaScript-Ereignisse zur Verfolgung der Aktivität von Benutzern in Ihren Livefyre-Apps. Beispielsweise können Sie die Seite aktualisieren, wenn Benutzer Inhalte auf Twitter oder Facebook teilen oder wenn neue Inhalte veröffentlicht werden.

Hier ist ein Beispiel, wie man die Ereignis erhält. Ersetzen Sie `console.log` durch Ihren Code, um das Ereignis Ihrer Analytics-Integration (dynamisches Tag-Management, Adobe Analytics JS, Google Analytics usw.) zuzuordnen und zu senden:

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Liste unterstützter Media Wall-Ereignis:

## Media Wall-Ereignisse

| Ereignis | Definition |
|---|---|
| `Init` | Wenn eine Medienwall auf einer Seite enthalten ist. |
| `Load` | Wenn die Medienmanagerseite unabhängig von der Position auf einer Seite geladen wurde. |
| `PostButtonClick` | Wenn ein Benutzer auf eine Schaltfläche &quot;Hochladen&quot;auf einer Medienplatine klickt. |
| `RequestMore` | Wenn der Benutzer mehr Inhalte in eine Medienmanagerei lädt. |
| `TwitterReplyClick` | Wenn ein Benutzer auf die Schaltfläche &quot;Twitter-Antwort&quot;von der Medienmanagerfläche klickt. |
| `TwitterRetweetClick` | Wenn ein Benutzer auf die Schaltfläche &quot;Twitter-Retweet&quot;von der Medienkonsole aus klickt. |
| `TwitterLikeClick` | Wenn ein Benutzer auf die Schaltfläche &quot;Gefällt mir&quot;-Klicks/Favoriten in Twitter von der Medienkonsole aus klickt. |
| `ModalView` | Wenn der Benutzer in einem größeren modalen Fenster auf die Ansicht von Media Pinnwänden klickt. |
| `Like` | Wenn ein Benutzer auf der Medienmanagerseite auf die Schaltfläche &quot;Gefällt mir&quot;klickt. |
| `ShareButtonClick` | Jedes Mal, wenn ein Benutzer auf die Schaltfläche &quot;Freigeben&quot;auf einer Medienwall-Karte klickt. |
| `ShareURL` | Wenn der Textbereich &quot;Mit URL teilen&quot;ausgewählt/aus der Medienmauer kopiert wird. |
| `ShareFacebook` | Wenn auf &quot;Auf Facebook teilen&quot;aus der Medienmauer geklickt wird. |
| `ShareTwitter` | Wenn auf &quot;Mit Twitter teilen&quot;von der Medienmauer aus geklickt wird. |
