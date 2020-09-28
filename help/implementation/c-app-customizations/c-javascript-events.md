---
description: Die verfügbaren Ereignisse, an die Sie JavaScript für Konversations-Apps binden können (z. B. Kommentare, Chat, Live-Blog, Bewertungen und Anmerkungen).
seo-description: Die verfügbaren Ereignisse, an die Sie JavaScript für Konversations-Apps binden können (z. B. Kommentare, Chat, Live-Blog, Bewertungen und Anmerkungen).
seo-title: Definitionen und Beispiele zu JavaScript-Ereignissen
solution: Experience Manager
title: Definitionen und Beispiele zu JavaScript-Ereignissen
uuid: 61da2e2e-8fcd-482d-93df-c946f0475277
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Definitionen und Beispiele zu JavaScript-Ereignissen{#javascript-events-definitions-and-examples}

Die verfügbaren Ereignisse, an die Sie JavaScript für Konversations-Apps binden können (z. B. Kommentare, Chat, Live-Blog, Bewertungen und Anmerkungen).

Livefyre bietet JavaScript-Ereignisse zur Verfolgung von Benutzeraktivitäten in Ihren Livefyre-Apps. Beispielsweise können Sie die Seite aktualisieren, wenn Benutzer Inhalte auf Twitter oder Facebook teilen oder wenn neue Inhalte veröffentlicht werden.

Mit Livefyre können Sie außerdem Ereignisse zu Analytics-Integrationen von Drittanbietern (Adobe Analytics JS, Google Analytics, dynamisches Tag-Management usw.) hinzufügen, um App-Ereignisse zu verfolgen. Weitere Informationen erhalten Sie, wenn Sie mit Ihrem Integrationsmanager eines Drittanbieters die richtigen Ereignisse bereitstellen.

Fügen Sie der Seite den folgenden Code hinzu, wenn Sie Ihre App auf einer Seite instanziieren, um sie an diese Ereignisse zu binden. Ersetzen Sie den Ereignisnamen für `{eventName}`:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>Datenobjekte werden für alle Ereignishandler bereitgestellt. Für jedes Ereignis folgen Beispieldatenobjekte.

## commentPosted {#section_qfr_51p_xz}

Ein Benutzer hat einen Kommentar veröffentlicht.

* Ein übergeordnetes Element von null ist ein neuer Kommentar.
* Ein übergeordnetes Element von "Keine"ist ein Kommentar, der bearbeitet wurde.
* Eine Zahl für übergeordnete Elemente ist die übergeordnete ID der Antwort.

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## commentGekennzeichnet {#section_szy_s1p_xz}

Ein Benutzer hat einen Kommentar markiert.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

Einem Benutzer gefiel ein Kommentar.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

Ein Benutzer hat einen Kommentar aus dem Stream freigegeben. (Dieses Ereignis wird nicht ausgelöst, wenn Benutzer im Kommentareditor freigeben.) Dieses Ereignis wird ausgelöst, wenn auf die Schaltfläche "Freigeben"geklickt wird.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdated {#section_qdq_f1p_xz}

Die Gesamtzahl der sichtbaren Kommentare in dieser Unterhaltung hat sich geändert (inkrementiert oder dekrementiert).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

Ein Benutzer hat sich angemeldet.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## userLoggedOut {#section_tsg_5z4_xz}

Ein Benutzer hat sich abgemeldet.

nicht definiert ist.

## socialMention {#section_a1w_tz4_xz}

Ein Benutzer hat in einem Kommentar eine @Erwähnung hinzugefügt. Gibt ein Array der folgenden Elemente zurück:

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeatured

Ein Moderator-Benutzer gab einen Kommentar heraus. Gibt ein Array der folgenden Elemente zurück:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

Der Kommentarstream wurde geladen und der ursprüngliche Inhaltssatz wurde vom Server abgerufen und dem Benutzer angezeigt.

nicht definiert ist.

## showMore {#section_pqg_nz4_xz}

Ein Benutzer klickte auf die **[!UICONTROL Show More]** Schaltfläche.

nicht definiert ist.

## userFollowed {#section_xxw_jz4_xz}

Gibt TRUE zurück, wenn ein Benutzer auf die **[!UICONTROL Follow]** Schaltfläche klickt, und FALSE, wenn Inhalte in den Stream gepostet werden.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnfollowed {#section_wm1_gz4_xz}

Gibt TRUE zurück, wenn ein Benutzer auf die Schaltfläche " **Unbefolgt** "klickt, und FALSE, wenn Inhalte in den Stream gepostet werden.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

