---
description: Entfernen Sie die standardmäßigen Livefyre-App-Komponenten aus Ihrer App.
title: App-Elemente ausblenden
exl-id: f8bbed2c-d009-41b8-927d-8d6ac4a63571
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# App-Elemente ausblenden{#hide-app-elements}

Entfernen Sie die standardmäßigen Livefyre-App-Komponenten aus Ihrer App.

Verwenden Sie CSS, um standardmäßige Livefyre-App-Elemente auf Ihrer Seite auszublenden, sodass Sie die Benutzererfahrung an Ihre Anforderungen anpassen können.

Um Elemente aus der App auszublenden, setzen Sie die Anzeige auf &quot;Ohne&quot;.

Beispiele:

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```
