---
description: Die verfügbaren Ereignisse, an die Sie JavaScript für Konversations-Apps binden können (z. B. Kommentare, Chat, Live-Blog, Bewertungen und Anmerkungen).
seo-description: Die verfügbaren Ereignisse, an die Sie JavaScript für Konversations-Apps binden können (z. B. Kommentare, Chat, Live-Blog, Bewertungen und Anmerkungen).
seo-title: Javascript-Ereignisdefinitionen und Beispiele
solution: Experience Manager
title: Javascript-Ereignisdefinitionen und Beispiele
uuid: 61 da 2 e 2 e -8 fcd -482 d -93 df-c 946 f 0475277
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Javascript-Ereignisdefinitionen und Beispiele{#javascript-events-definitions-and-examples}

Die verfügbaren Ereignisse, an die Sie JavaScript für Konversations-Apps binden können (z. B. Kommentare, Chat, Live-Blog, Bewertungen und Anmerkungen).

Livefyre stellt javascript-Ereignisse zur Verfolgung von Benutzeraktivitäten in Ihren Livefyre-Apps bereit. Beispielsweise möchten Sie die Seite aktualisieren, wenn Benutzer Inhalte für Twitter oder Facebook verwenden oder wenn neue Inhalte veröffentlicht werden.

Livefyre ermöglicht Ihnen außerdem, Ereignisse zu Analytics-Integrationen von Drittanbietern (Adobe Analytics JS, Google Analytics, Dynamisches Tag-Management etc.) zur Verfolgung von App-Ereignissen hinzuzufügen. Für weitere Informationen wenden Sie sich an Ihren Integrationsmanager von Drittanbietern, um die richtigen Ereignisse bereitzustellen.

Um an diese Ereignisse zu binden, fügen Sie der Seite den folgenden Code hinzu, wenn Sie Ihre App auf einer Seite instanziieren. Ersetzen Sie den Ereignisnamen `{eventName}`für:

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
>Datenobjekte werden für alle Ereignishandler bereitgestellt. Beispiel-Datenobjekte folgen jedem Ereignis.

## Commentpublished {#section_qfr_51p_xz}

Ein Benutzer hat einen Kommentar gepostet.

* Ein übergeordnetes Element von null ist ein neuer Kommentar.
* Ein übergeordnetes Element von &quot;None&quot; ist ein Kommentar, der bearbeitet wurde.
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

## Commentflag {#section_szy_s1p_xz}

Ein Benutzer hat einen Kommentar gekennzeichnet.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## Commentliked {#section_vc1_r1p_xz}

Ein Benutzer hat einen Kommentar gelistet.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## Commentshared {#section_nqb_31p_xz}

Ein Benutzer hat einen Kommentar aus dem Stream freigegeben. (Dieses Ereignis wird nicht ausgelöst, wenn Benutzer im Kommentar-Editor freigeben.) Dieses Ereignis wird ausgelöst, wenn auf die Schaltfläche &quot;Freigeben&quot; geklickt wird.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## Commentcountupdated {#section_qdq_f1p_xz}

Die Gesamtzahl der sichtbaren Kommentare in dieser Konversation wurde geändert (entweder inkrementiert oder dekrementiert).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## Userloggedin {#section_yjt_vz4_xz}

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

## Userloggedout {#section_tsg_5z4_xz}

Ein Benutzer hat sich abgemeldet.

nicht definiert.

## Socialmention {#section_a1w_tz4_xz}

Ein Benutzer enthielt einen @ mention in einem Kommentar. Gibt ein Array der folgenden Werte zurück:

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## Commentfeatworth

Ein Moderator hat einen Kommentar angegeben. Gibt ein Array der folgenden Werte zurück:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## Initialrendercomplete {#section_odc_4z4_xz}

Der Kommentarstream wurde geladen und der erste Satz von Inhalten wurde vom Server abgerufen und dem Benutzer angezeigt.

nicht definiert.

## Showmore {#section_pqg_nz4_xz}

Ein Benutzer hat auf die **[!UICONTROL Show More]** Schaltfläche geklickt.

nicht definiert.

## Userfollowed {#section_xxw_jz4_xz}

Gibt &quot;true&quot; zurück, wenn ein Benutzer auf die **[!UICONTROL Follow]** Schaltfläche klickt, und false, wenn der Inhalt im Stream gepostet wird.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## Userunfollowed {#section_wm1_gz4_xz}

Gibt &quot;true&quot; zurück, wenn ein Benutzer **auf** die Schaltfläche&quot; Nicht folgen&quot; klickt, und false, wenn der Inhalt im Stream gepostet wird.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

