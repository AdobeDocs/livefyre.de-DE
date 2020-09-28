---
description: Ermöglicht Benutzern das Durchklicken von Sammlungen aus einem einseitigen Layout und einer URL.
seo-description: Ermöglicht Benutzern das Durchklicken von Sammlungen aus einem einseitigen Layout und einer URL.
seo-title: Sammlung ändern
solution: Experience Manager
title: Sammlung ändern
uuid: 81c8a554-375f-4659-9e25-5b3618824633
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Sammlung ändern {#change-collection}

Ermöglicht Benutzern das Durchklicken von Sammlungen aus einem einseitigen Layout und einer URL.

Verwenden Sie den Delegaten zum Ändern der Sammlung, um die auf einer Seite angezeigte Sammlung zu ändern, ohne die URL zu ändern, während bereits eine Livefyre-App geladen wurde. Verwenden Sie diese Funktion, um Foto- oder Videogalerien oder andere Apps anzuzeigen, in denen die angezeigte Sammlung nach einer Benutzeraktion geändert werden soll.

Wenn Sie beispielsweise auf ein Video oder Foto in einer Galerie klicken, wird eine für diese Auswahl spezifische Sammlung geladen, während sich die URL der Seite nicht ändert.

So [laden Sie eine von drei Sammlungen von einer Seite](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count):

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
