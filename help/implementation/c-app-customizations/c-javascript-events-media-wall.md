---
description: Verwenden Sie Javascript-Ereignisse, um auf Ereignisse zu achten, die auf einer Medienpinnwand auftreten, und diese an das Analysetool Ihrer Wahl zu senden.
seo-description: Verwenden Sie Javascript-Ereignisse, um auf Ereignisse zu achten, die auf einer Medienpinnwand auftreten, und diese an das Analysetool Ihrer Wahl zu senden.
seo-title: Javascript-Ereignisse für Medienpinnwand
solution: Experience Manager
title: Javascript-Ereignisse für Medienpinnwand
uuid: 8 afc 0529-4640-476 a-b 207-91 b 2 c 70101 f 0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Javascript-Ereignisse für Medienpinnwand{#javascript-events-for-media-wall}

Verwenden Sie Javascript-Ereignisse, um auf Ereignisse zu achten, die auf einer Medienpinnwand auftreten, und diese an das Analysetool Ihrer Wahl zu senden.

Livefyre stellt javascript-Ereignisse zur Verfolgung von Benutzeraktivitäten in Ihren Livefyre-Apps bereit. Beispielsweise möchten Sie die Seite aktualisieren, wenn Benutzer Inhalte für Twitter oder Facebook verwenden oder wenn neue Inhalte veröffentlicht werden.

Hier sehen Sie ein Beispiel für das Empfangen der Ereignisse. Sie können `console.log` das Ereignis durch Ihren Code ersetzen und an Ihre Analytics-Integration senden (dynamisches Tag-Management, Adobe Analytics JS, Google Analytics usw.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Liste unterstützter Medienpinnwandereignisse:

## Medienpinnwandereignisse

| Ereignis | Definition |
|---|---|
| `Init` | Wenn eine Medienpinnwand auf einer Seite enthalten ist. |
| `Load` | Wenn die Medienpinnwand unabhängig von der Position auf einer Seite geladen wurde. |
| `PostButtonClick` | Wenn ein Benutzer auf eine &quot;Hochladen&quot; -Schaltfläche auf einer Medienpinnwand klickt. |
| `RequestMore` | Wenn der Benutzer mehr Inhalte in eine Medienpinnwand lädt. |
| `TwitterReplyClick` | Ein Benutzer klickt auf die Schaltfläche &quot;Twitter-Antwort&quot; von der Medienpinnwand. |
| `TwitterRetweetClick` | Ein Benutzer klickt auf die Schaltfläche &quot;Twitter Retweet&quot; von der Medienpinnwand. |
| `TwitterLikeClick` | Ein Benutzer klickt auf die Schaltfläche &quot;Gefällt mir&quot; /&quot; Favorit&quot; von der Medienpinnwand. |
| `ModalView` | Wenn Benutzer klicken, um Medien-Wall-Inhalte in einem größeren modalen Fenster anzuzeigen. |
| `Like` | Ein Benutzer klickt auf der Medienpinnwand auf die Schaltfläche &quot;Gefällt mir&quot; . |
| `ShareButtonClick` | Jedes Mal, wenn ein Benutzer auf einer Medienpinnwand auf die Schaltfläche &quot;Freigeben&quot; klickt. |
| `ShareURL` | Wenn der Textbereich &quot;Auf URL teilen&quot; ausgewählt/aus der Medienpinnwand kopiert wird. |
| `ShareFacebook` | Wenn auf Facebook teilen von der Medienpinnwand geklickt wird. |
| `ShareTwitter` | Wenn auf Twitter freigeben von der Medienpinnwand geklickt wird. |
