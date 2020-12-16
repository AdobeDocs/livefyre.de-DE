---
description: Erstellen Sie eine Medienwall mit Content-Streaming in Echtzeit.
seo-description: Erstellen Sie eine Medienwall mit Content-Streaming in Echtzeit.
seo-title: Medienwall
solution: Experience Manager
title: Medienwall
uuid: c6087c80-a35b-44d2-9dd4-ba9cd471172d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---


# Medienwall{#media-wall}

Erstellen Sie eine Medienwall mit Content-Streaming in Echtzeit.

Mit Media Wall können Sie eine Social-Wand in Echtzeit für Ihre Site erstellen. Verwenden Sie das Livefyre JavaScript SDK&#39;s streamub-wallpackage, um Livefyre-Social-Feeds als eine visuell ansprechende, geteilte Inhaltserfahrung im Vollbildformat anzuzeigen, die sich hervorragend eignet, um Live-Ereignisse zu bedienen, Fotowettbewerbe zu hosten und Social-Bereiche Ihrer Website zu aktivieren.

## Integration {#section_jfm_bwb_c1b}

Die schnellste Möglichkeit, eine Media Pinnwand hinzuzufügen, besteht darin, die auf Livefyres CDN gehostete Version zu verwenden.

Fügen Sie zunächst [Livefyre.js](https://github.com/Livefyre/Livefyre.js) zu Ihrer Site hinzu.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

Positionieren Sie dann das Element, in dem die Medienmauer angezeigt wird.

```
<div id="wall"></div>
```

Verwenden Sie zum Schluss `Livefyre.require`, um die Komponente zu erstellen.

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

Du hast jetzt eine Mauer! Sehen Sie dies alles in Aktion in [diesem Beispiel](https://codepen.io/gobengo/pen/dFwDL).

**Hit einen Fehler?** Überprüfen Sie, ob Sie den richtigen Parameter für die Umgebung übergeben. Zu den Optionen gehören `livefyre.com` (Produktion) oder `t402.livefyre.com` (UAT).

>[!NOTE]
>
>Jede Stilanpassung von Tweets, die von Ihrer Media Wall App gerendert werden, muss gemäß den [Anzeigeanforderungen](https://dev.twitter.com/terms/display-requirements) von Twitter erfolgen.

## Konfigurationsoptionen {#section_ucv_qvb_c1b}

`columns`

Ermöglicht Ihnen, die Anzahl der Spalten für Ihre Medienmauer beim Erstellen Ihrer Wand zu definieren. Wenn diese Option aktiviert ist, passt sich die Spaltenbreite automatisch an die Container-Größe der Medienmauer an, wobei die angegebene Spaltenanzahl beibehalten wird.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

Die Anzahl der Inhaltselemente, die beim Laden der Seite gerendert werden. Der Standardwert ist 50.

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

Damit können Sie die minimale Pixelbreite für jede Spalte im Container-Element der Medienmauer festlegen. (Ihre Medienmauer wählt automatisch eine passende Spaltenanzahl aus, je nach der Breite des Container-Elements. Standardmäßig bestimmt die Breite der Medienmauer geteilt durch die minimale Inhaltsbreite (300 px, falls nicht definiert) die Anzahl der Spalten.)

>[!NOTE]
>
>Verwenden Sie diese Option nicht zusammen mit der Spaltenoption.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

Wenn für einen Inhalt Anlagen vorhanden sind, zeigt Media Walls standardmäßig eine klickbare Miniaturansicht an. Wenn Sie darauf klicken, öffnet die App ein Modell, in dem die Foto-/Videoanlage vollständig angezeigt wird. Um diese Option zu deaktivieren, setzen Sie modal auf false.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

Definiert die Schaltfläche [!UICONTROL Post Content], die auf Ihrer Pinnwand angezeigt werden soll. Für diese Option müssen Sie `opts.collection` einreichen und der Seite eine Livefyre.js Auth-Integration hinzufügen.

`postButton` Parameter:

* `false` (Standard): Die Schaltfläche &quot;Inhalt des Beitrags&quot;darf nicht angezeigt werden. (Erstellt eine schreibgeschützte Medienwall.)
* `true` oder  `LiveMediaWall.postButtons.contentWithPhotos`) Fügen Sie eine Schaltfläche hinzu, über die Benutzer Textinhalte mit angehängten Fotos hinzufügen können.

* `LiveMediaWall.postButtons.content`: Fügen Sie eine Schaltfläche hinzu, über die Benutzer Textinhalte hinzufügen können, aber keine Fotos anhängen können.
* `LiveMediaWall.postButtons.photo`: Fügen Sie eine Schaltfläche hinzu, über die Benutzer ein Foto, jedoch keinen Text hinzufügen können.

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

Definiert die Anzahl der Inhaltselemente, die der Pinnwand hinzugefügt werden sollen, wenn auf die Schaltfläche [!UICONTROL Show More] geklickt wird.

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## Stilkonfigurationsoptionen {#section_ztv_dvb_c1b}

Media Wall Angebot außerdem verschiedene Konfigurationsoptionen, mit denen Sie Textfarbe, -stil und -größe anpassen können. Verwenden Sie zur Implementierung dieser Optionen die folgende Syntax:

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

Eine gültige Eingabe finden Sie in den W3C-Standards für die Eigenschaften CSS [Schriftfamilie](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family), [Schriftgröße](https://www.w3.org/TR/CSS2/fonts.html#font-size-props), [Zeilenhöhe,](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height) und [Farbe](https://www.w3.org/TR/css3-color/#colorunits).

* **bodyFontSize** *(CSS Font Size String)* Die Schriftgröße für den Textkörper des Inhalts.

* **bodyLineHeight** *(CSS-Zeilenhöhenzeichenfolge)* Die Zeilenhöhe für den Textkörper des Inhalts.

* **buttonActiveBackgroundColor** *(CSS-Farbzeichenfolge)** Die Farbe für den Schaltflächenhintergrund bei aktiver Ausführung.

* **buttonBorderColor** *(CSS-Farbzeichenfolge)** Die Farbe für Schaltflächenränder.

* **buttonHoverBackgroundColor** *(CSS-Farbzeichenfolge)* Die Farbe für den Schaltflächenhintergrund beim Bewegen des Mauszeigers.

* **buttonTextColor** *(CSS-Farbzeichenfolge)* Die Farbe für die Schaltflächenbeschriftungen.

* **cardBackgroundColor** *(CSS Color String)* Die Hintergrundfarbe für Inhaltskarten in der Medienwand.

* **displayNameColor** *(CSS-Farbzeichenfolge)* Die Farbe für Anzeigenamen in der Zeile.

* **fontFamily** *(CSS Font Family String)* Die Schriftfamilie für den Texttext.

* **footerTextColor** *(CSS-Farbzeichenfolge)* Die Farbe für Sekundärtext (z. B. Fußzeilentext und Benutzername in der Zeile).

* **linkAttachmentBackgroundColor** *(CSS-Farbzeichenfolge)* Die Hintergrundfarbe für Link-Anlagen (gestapelte Anlagen).

* **linkAttachmentBorderColor** *(CSS-Farbzeichenfolge)* Die Rahmenfarbe für Link-Anlagen (gestapelte Anlagen).

* **linkAttachmentTextColor** *(CSS-Farbzeichenfolge)* Die Farbe für den Text des Link-Anhangs.

* **linkColor** *(CSS-Farbzeichenfolge)* Die Farbe für Hyperlinks (wie z. B. Links im Textkörper und Links zu Anzeigenamen).

* **textColor** *(CSS-Farbzeichenfolge)* Die Farbe des Textes.

* **titleFontSize** *(CSS Font Size String)* Die Schriftgröße für Inhaltstitel.

* **titleLineHeight** *(CSS-Zeilenhöhenzeichenfolge)* Die Zeilenhöhe für Inhaltstitel.

* **sourceLogoColor** *(CSS-Farbzeichenfolge)* Die Farbe für das Quelllogo.

* **usernameColor** *(CSS-Farbzeichenfolge)* Die Farbe für die Benutzernamen in der Zeile.
