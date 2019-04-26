---
description: Positionieren Sie das Livefyre-Logo auf Ihrer Seite.
seo-description: Positionieren Sie das Livefyre-Logo auf Ihrer Seite.
seo-title: Verschieben des Livefyre-Logos
solution: Experience Manager
title: Verschieben des Livefyre-Logos
uuid: 807304 ae -6070-4505-87 db -169 a 925 f 714 c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Verschieben des Livefyre-Logos{#move-the-livefyre-logo}

Positionieren Sie das Livefyre-Logo auf Ihrer Seite.

Wenn Ihr Einverständnis mit Livefyre gestattet ist, können Sie das Livefyre-Logo von oben nach unten verschieben.

Fügen Sie beispielsweise unmittelbar hinter dem Element, das die Livefyre-App enthält, die folgende HTML zu Ihrer Seite hinzu:

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

Fügen Sie dann Folgendes dem Stylesheet Ihrer Seite hinzu:

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

