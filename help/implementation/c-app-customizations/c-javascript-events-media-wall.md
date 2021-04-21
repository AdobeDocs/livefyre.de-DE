---
description: Verwenden Sie JavaScript-Ereignis, um auf Ereignis zu warten, die in einer Medienmanschette auftreten, und diese an das Analysetool Ihrer Wahl zu senden.
title: JavaScript-Ereignisse für Media Wall
exl-id: 3fe76467-65e2-4f8b-bd75-5a2ffc3e7e15
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# JavaScript-Ereignis für Media Wall{#javascript-events-for-media-wall}

Verwenden Sie JavaScript-Ereignis, um auf Ereignis zu warten, die in einer Medienmanschette auftreten, und diese an das Analysetool Ihrer Wahl zu senden.

Livefyre bietet JavaScript-Ereignisse zur Verfolgung der Aktivität von Benutzern in Ihren Livefyre-Apps. Beispielsweise können Sie die Seite aktualisieren, wenn Benutzer Inhalte mit &quot;Gefällt mir&quot;oder &quot;Teilen&quot;für Twitter oder Facebook oder wenn neue Inhalte veröffentlicht werden.

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
| `TwitterReplyClick` | Wenn ein Benutzer auf die Schaltfläche &quot;Twitter-Antwort&quot;von der Medienmanschette klickt. |
| `TwitterRetweetClick` | Wenn ein Benutzer auf der Medienmanagerseite auf die Schaltfläche &quot;Twitter Retweet&quot;klickt. |
| `TwitterLikeClick` | Wenn ein Benutzer auf der Medienmanagerseite auf die Schaltfläche &quot;Twitter gefällt mir/Favorit&quot;klickt. |
| `ModalView` | Wenn der Benutzer in einem größeren modalen Fenster auf die Ansicht von Media Pinnwänden klickt. |
| `Like` | Wenn ein Benutzer auf der Medienmanagerseite auf die Schaltfläche &quot;Gefällt mir&quot;klickt. |
| `ShareButtonClick` | Jedes Mal, wenn ein Benutzer auf die Schaltfläche &quot;Freigeben&quot;auf einer Medienwall-Karte klickt. |
| `ShareURL` | Wenn der Textbereich &quot;Mit URL teilen&quot;ausgewählt/aus der Medienmauer kopiert wird. |
| `ShareFacebook` | Wenn auf &quot;Mit Facebook teilen&quot;von der Medienmauer aus geklickt wird. |
| `ShareTwitter` | Wenn auf &quot;Mit Twitter teilen&quot;von der Medienmauer aus geklickt wird. |
