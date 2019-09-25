---
description: Positionieren Sie das Livefyre-Logo auf Ihrer Seite neu.
seo-description: Positionieren Sie das Livefyre-Logo auf Ihrer Seite neu.
seo-title: Das Livefyre-Logo verschieben
solution: Experience Manager
title: Das Livefyre-Logo verschieben
uuid: 807304ae-6070-4505-87db-169a925f714c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Das Livefyre-Logo verschieben{#move-the-livefyre-logo}

Positionieren Sie das Livefyre-Logo auf Ihrer Seite neu.

Wenn Ihr Vertrag mit Livefyre dies zulässt, können Sie das Livefyre-Logo von der Oberseite des Inhaltsstreams nach unten verschieben.

Fügen Sie Ihrer Seite beispielsweise unmittelbar nach dem Element mit der Livefyre-App den folgenden HTML-Code hinzu:

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

Fügen Sie dann dem Stylesheet Ihrer Seite Folgendes hinzu:

```
/* Hide the top logo */ 
.fyre-widget .fyre-logo-drop, .fyre-widget .fyre-logo-help, .fyre-widget .fyre-help { 
    display:none !important; 
} 
  
/* Style the bottom logo */ 
#powered_by_livefyre_new a {    background: url(https://cdn.livefyre.com/libs/fyre.conv/v3.0.0/images/poweredbylivefyre.png) no-repeat left top; 
    display: block; 
    height: 24px; 
    font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
} 
#powered_by_livefyre_new a:hover { 
    text-decoration: underline; 
}
```

