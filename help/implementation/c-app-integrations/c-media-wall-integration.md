---
description: Erstellen Sie eine Medienpinnwand mit dem Inhaltsstreaming in Echtzeit.
seo-description: Erstellen Sie eine Medienpinnwand mit dem Inhaltsstreaming in Echtzeit.
seo-title: Medienpinnwand
solution: Experience Manager
title: Medienpinnwand
uuid: c 6087 c 80-a 35 b -44 d 2-9 dd 4-ba 9 cd 471172 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Medienpinnwand{#media-wall}

Erstellen Sie eine Medienpinnwand mit dem Inhaltsstreaming in Echtzeit.

Mit der Medienpinnwand können Sie eine Echtzeit-Social-Wand für Ihre Site erstellen. Verwenden Sie das streamhub-wallpaket von Livefyre javascript SDK, um Livefyre-Social-Feeds als visuell ansprechende, Vollbildanzeige anzuzeigen, die für das Behandeln von Live-Ereignissen, Hosting von Fotowettbewerben und leistungsstarken Social-Abschnitte Ihrer Website geeignet ist.

## Integration{#section_jfm_bwb_c1b}

Die schnellste Möglichkeit zum Hinzufügen einer Medienwall besteht darin, die erstellte Version auf dem CDN von Livefyre zu verwenden.

Fügen Sie [zunächst Livefyre. js](https://github.com/Livefyre/Livefyre.js) zu Ihrer Site hinzu.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Positionieren Sie dann das Element, in dem die Medienpinnwand angezeigt wird.

```
<div id="wall"></div>
```

Zum Erstellen `Livefyre.require` der Komponente verwenden.

```
<script> 
Livefyre.require([ 
    'streamhub-wall#5' 
], function(MediaWall) {     
    var wall = window.wall = new MediaWall({ 
        el: document.getElementById("wall"), 
        collection: { 
            "network": "client-solutions.fyre.co", 
            "siteId": "364309", 
            "articleId": "answers-mediawall" 
        } 
    }); 
}); 
</script>
```

Sie haben jetzt eine Pinnwand! Sehen Sie sich dies in diesem [Beispiel alles](https://codepen.io/gobengo/pen/dFwDL)an.

**Einen Fehler erreichen?** Stellen Sie sicher, dass Sie den richtigen Umgebungsparameter übergeben. Zu den Optionen gehören `livefyre.com` (Produktion) oder `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Jede Formatierung von Tweets, die von Ihrer Medienwall-App gerendert werden, muss gemäß den [Anzeigeanforderungen von Twitter vorgenommen](https://dev.twitter.com/terms/display-requirements)werden.

## Konfigurationsoptionen {#section_ucv_qvb_c1b}

`columns`

Hiermit können Sie die Anzahl der Spalten für Ihre Medienpinnwand beim Erstellen Ihrer Pinnwand definieren. Wenn diese Option festgelegt ist, wird die Breite der einzelnen Spalten automatisch an die Containergröße der Medienpinnwand angepasst und dabei die angegebene Spaltenanzahl beibehalten.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

Die Anzahl der Inhaltselemente, die beim Laden der Seite gerendert werden sollen. Der Standardwert ist 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Hiermit können Sie die minimale Breite (Pixel) für jede Spalte innerhalb des Elements der Medienpinnwand festlegen. (Ihre Medienpinnwand wählt je nach Breite des Containerelements automatisch eine entsprechende Spaltenanzahl aus. Standardmäßig bestimmt die Breite der Medienpinnwand dividiert durch die minimale Inhaltsbreite (300 px, falls nicht definiert) die Spaltenanzahl.)

>[!NOTE]
>
>Verwenden Sie diese Option nicht in Kombination mit den Spalten.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Wenn Anlagen für ein Inhaltselement vorhanden sind, zeigt Medienwalls standardmäßig eine anklickbare Miniaturansicht an. Wenn Sie auf die App klicken, öffnet die App einen modalen Anzeigebereich des Foto-/Videoanhangs. Um diese Option zu deaktivieren, setzen Sie die modale Einstellung auf false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Definiert die [!UICONTROL Post Content] Schaltfläche, die auf Ihrer Pinnwand angezeigt werden soll. Diese Option erfordert die Weitergabe `opts.collection`und fügen eine Livefyre. js-Authentifizierung auf der Seite hinzu.

`postButton` Parameter:

* `false` (Standard): Zeigen Sie keine Schaltfläche "Beitragsinhalt" an. (Erstellt eine schreibgeschützte Medienwall.)
* `true` (oder `LiveMediaWall.postButtons.contentWithPhotos`): Schließen Sie eine Schaltfläche ein, mit der Benutzer Textinhalte mit angehängten Fotos hinzufügen können.

* `LiveMediaWall.postButtons.content`: Schließen Sie eine Schaltfläche ein, mit der Benutzer Textinhalte hinzufügen, jedoch keine Fotos anhängen können.
* `LiveMediaWall.postButtons.photo`: Schließen Sie eine Schaltfläche ein, mit der Benutzer ein Foto, aber keinen Text hinzufügen können.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Definiert die Anzahl der Inhaltselemente, die der Pinnwand hinzugefügt werden sollen, wenn auf die [!UICONTROL Show More] Schaltfläche geklickt wird.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Stilkonfigurationsoptionen {#section_ztv_dvb_c1b}

Die Medienpinnwand bietet außerdem verschiedene Konfigurationsoptionen, mit denen Sie Textfarbe, Stil und Größe anpassen können. Verwenden Sie die folgende Syntax, um diese Optionen zu implementieren:

```
var wall2 = window.wall2 = new MediaWall({ 
   el: document.getElementById("listView1"), 
   collection: collection, 
   cardBackgroundColor: '#333', 
   textColor: 'magenta', 
   linkColor: 'orange', 
   footerTextColor: 'lime', 
   displayNameColor: 'cyan', 
   usernameColor: 'red', 
   fontFamily: 'Helvetica, Arial', 
   linkAttachmentBackgroundColor: '#555', 
   linkAttachmentBorderColor: '#888' 
}); 
```

Eine gültige Eingabe finden Sie in den W 3 C-Standards für die CSS [-Schriftfamilie](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Schriftgröße](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Zeilenhöhe und](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) [Farbeigenschaften](https://www.w3.org/TR/css3-color/#colorunits) .

* **Bodyfontsize** *(CSS Font Size String)* Die Schriftgröße für den content body text.

* **Bodylineheight** *(CSS Line Height String)* Die Zeilenhöhe für den Textzeichentext.

* **Buttonactivebackgroundcolor** *(CSS Color String)** Die Farbe für den Schaltflächenhintergrund aktiviert.

* **Buttonbordercolor** *(CSS Color String)** Die Farbe für Schaltflächenbegrenzungen.

* **Buttonhoverbackgroundcolor** *(CSS Color String)* Die Farbe für den Schaltflächenhintergrund beim Maushover.

* **Buttontextcolor** *(CSS Color String)* Die Farbe für die Schaltflächenbeschriftungen.

* **Cardbackgroundcolor** *(CSS-Farbzeichenfolge)* Die Hintergrundfarbe für Inhaltskarten in der Medienpinnwand.

* **Displaynamecolor** *(CSS-Farbzeichenfolge)* Die Farbe für Anzeigenamen in der Autorenzeile.

* **Fontfamily** *(CSS Font Family String)* Die Schriftfamilie für body text.

* **Footertextcolor** *(CSS Color String)* Die Farbe für Sekundärtext (wie Fußzeilentext und Benutzername in der Autorenzeile).

* **Linkattachmentbackgroundcolor** *(CSS-Farbzeichenfolge)* Die Hintergrundfarbe für Link-Anlagen (gestapelte Anlagen).

* **Linkattachmentbordercolor** *(CSS Color String)* Die Rahmenfarbe für Link-Anlagen (gestapelte Anlagen).

* **Linkattachmenttextcolor** *(CSS Color String)* Die Farbe für den Link-Anlagentext.

* **Linkcolor** *(CSS-Farbzeichenfolge)* Die Farbe für Hyperlinks (wie Links im Textkörper und Links für Anzeigenamen).

* **Textcolor** *(CSS-Farbzeichenfolge)* Die Farbe für Textkörper.

* **Titlefontsize** *(CSS Font Size String)* Die Schriftgröße für Inhaltstitel.

* **Titlelineheight** *(CSS-Zeilenhöhenzeichenfolge)* Die Zeilenhöhe für Inhaltstitel.

* **Sourcelogocolor** *(CSS Color String)* Die Farbe für das Quelllogo.

* **Usernamecolor** *(CSS Color String)* Die Farbe für die Benutzernamen in der Autorenzeile.
