---
description: Erlauben Sie Benutzern, durch Sammlungen aus einem einzelnen Seitenlayout
  und einer URL zu klicken.
seo-description: Erlauben Sie Benutzern, durch Sammlungen aus einem einzelnen Seitenlayout
  und einer URL zu klicken.
seo-title: Sammlung ändern
solution: Experience Manager
title: Sammlung ändern
uuid: 81 c 8 a 554-375 f -4659-9 e 25-5 b 3618824633
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sammlung ändern {#change-collection}

Erlauben Sie Benutzern, durch Sammlungen aus einem einzelnen Seitenlayout und einer URL zu klicken.

Verwenden Sie den Change Collection Delegate, um die auf einer Seite angezeigte Sammlung zu ändern, ohne die URL zu ändern, während eine Livefyre-App bereits geladen ist. Verwenden Sie diese Funktion, um Foto- oder Videogalerien oder andere Apps anzuzeigen, bei denen sich die angezeigte Sammlung nach einer Benutzeraktion ändern sollte.

Wenn Sie beispielsweise auf ein Video oder ein Foto in einer Galerie klicken, wird eine für diese Auswahl spezifische Sammlung geladen, während sich die URL der Seite nicht ändert.

So [laden Sie eine von drei Sammlungen von einer einzelnen Seite](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count)aus:

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```
