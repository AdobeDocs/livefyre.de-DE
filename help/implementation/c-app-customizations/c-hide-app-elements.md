---
description: Entfernen Sie die standardmäßigen Livefyre-App-Komponenten aus Ihrer App.
seo-description: Entfernen Sie die standardmäßigen Livefyre-App-Komponenten aus Ihrer App.
seo-title: App-Elemente ausblenden
solution: Experience Manager
title: App-Elemente ausblenden
uuid: ea090b6e-99f5-4bd7-aa9e-d39a4dff1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# App-Elemente ausblenden{#hide-app-elements}

Entfernen Sie die standardmäßigen Livefyre-App-Komponenten aus Ihrer App.

Verwenden Sie CSS, um standardmäßige Livefyre-App-Elemente auf Ihrer Seite auszublenden, sodass Sie die Benutzererfahrung an Ihre Anforderungen anpassen können.

Um Elemente aus der App auszublenden, setzen Sie die Anzeige auf "Ohne".

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

