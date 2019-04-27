---
description: Fügen Sie Anzeigen in Ihren Kommentarstream ein.
seo-description: Fügen Sie Anzeigen in Ihren Kommentarstream ein.
seo-title: Anzeigen in Kommentaren
solution: Experience Manager
title: Anzeigen in Kommentaren
uuid: f 8 d 6372 f -4468-4884-a 384-116180 b 4 c 748
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Anzeigen in Kommentaren{#ads-in-comments}

Fügen Sie Anzeigen in Ihren Kommentarstream ein.

## Anzeigen in Kommentaren {#topic_CDD2ACF16AED4DE782725EE90089C04E}

Fügen Sie Anzeigen in Ihren Kommentarstream ein.

Mit der Funktion &quot;Livefyre-Anzeigen in Kommentaren&quot; können Sie Anzeigen in Ihren Kommentarstream einfügen, die Häufigkeit festlegen, mit der die Anzeigen im Stream erscheinen, und sowohl synchrone als auch asynchrone Injizierungsupperten erstellen.

Livefyre stellt mithilfe Ihres Anzeigenverwaltungsanbieters den Container bereit, über den Sie eine Anzeige einbringen können.

Um eine Anzeige einzufügen, übergeben Sie Livefyre zwei Werte:

* Häufigkeit der Injizierung der Ankündigung in den Kommentarstream
* Eine Funktion, die die entsprechende Ankündigung bereitstellt.

>[!NOTE]
>
>Anzeigen werden nur gerendert, wenn sich die Anzeigenplatzierung im Viewport befindet. Anzeigen werden nur nach übergeordneten Kommentaren angezeigt (nicht in Threads), und Benutzer können diese Werbung nicht kommentieren. Diese API ermöglicht es Ihnen nicht, die Größe des Elements anzugeben, in dem Ihre Anzeigen platziert werden sollen.

## Integration{#concept_C99029E618EC49779E3117D2C303E4F1}

Um diese Funktion zu verwenden, erstellen Sie ein div-Element auf der Seite, in das die Anzeigen platziert werden sollen, und geben Sie dann den HTML-Code von Ihrem Anzeigenanbieter an.

Livefyre bietet zwei Anzeigenplatzierungstypen: synchron und asynchron. Beide Typen laden Ihre Anzeigen nur dann hoch, wenn der Benutzer die Seite so blättert, dass die Position der Anzeige in Sicht ist. Beide müssen auch ein DOM-Element (iframe oder div) zurückgeben.

Um die Anzeige zu erhalten, werden die synchronen Methodenaufrufe einem lokalen Repository, während asynchrone Aufrufe an einen externen Dienst gesendet werden.

### Synchron

Um eine synchrone Platzierung zu erstellen, schließen Sie die Anzeige in die Delegate ein und geben Sie das Anzeigenelement selbst zurück. Die synchronen Methodenaufrufe in einem lokalen Repository ermöglichen es Ihnen, Ihre eigene Anzeigengenerierung zu verarbeiten.

### Asynchron

Die asynchrone Methode erfordert, dass das Element in das DOM eingefügt wird, bevor Sie den Anzeigenanbieter aufrufen. Ihr Anbieter bestimmt dann, welche Anzeige gesendet werden soll, und gibt ihn zurück.

Um asynchrone Anzeigen zu implementieren, erstellen Sie einen Stellvertreter, der ein Element zurückgibt, in dem die Anzeige platziert wird, und einen Rückruf, der die Platzierung der Anzeige ausführt. Das im Delegate zurückgegebene Element muss über eine eindeutige ID für die Anzeige verfügen, die als Ziel dient. Der Rückruf fügt die Anzeige in das von der eindeutigen ID bereitgestellte Element ein.

>[!NOTE]
>
>Je nach Anzeigenanbieter verhalten sich Rückrufe unterschiedlich.

Wenn die Seite geladen wird, greift Anzeigen in Kommentaren auf den Stellvertreter zu, initiiert das Element und ruft dann den Rückruf auf, der das (zuvor definierte) Element mit der Anzeige aktualisiert.

## Parameter {#concept_D7E27B0C21EF405C8EB826083DBB53EC}

Die folgenden Parameter sind für diesen Aufruf verfügbar.

Für das Anzeigenobjekt:

* **delay:****(optional) Ganzzahl** : Legt die Anzahl der Kommentare fest, nach denen die erste Anzeige angezeigt wird. Der Standardwert ist 10.
* **frequency: (optional) Integer** : Legt die Anzahl der Kommentare fest, nach denen jede nachfolgende Anzeige angezeigt wird. Beispiel: Geben Sie 2 ein, um eine Anzeige als jeden dritten Kommentar anzuzeigen. Der Standardwert ist 10.
* **delegate:*****erforderliche*Funktion** - Die Funktion, die aufgerufen wird, um Anzeigen in den Kommentarstream einzufügen.

Das Delegationsobjekt unterstützt sowohl synchrone als auch asynchrone Anzeigenaufrufe. Der Parameter, der der Stellvertreterfunktion, Daten zugewiesen wird, enthält Folgendes:

* **title:****string** - Der Titel der Sammlung.
* **Tags:****array** - Eine Liste der mit der Sammlung verknüpften Tags.
* **id:****string** - Die Artikelkennung der Sammlung.
* **url:****string** - Die URL der Sammlung.
* **Networkid:****string** - Die Netzwerk-ID für die Sammlung.
* **Siteid:****int** - Die Site-ID für die Sammlung.

Diese Elemente werden über das Kontextconfig-Objekt in unserem Beispiel weitergegeben und im [Abschnitt &quot;Erste Schritte&quot;](/help/implementation/c-app-integrations/c-comments-integration/c-comments-integration.md#section_656AAC97903F485084650269A6C7EBCE) detailliert erläutert.

### Synchron

Der Delegate gibt ein Objekt zurück, das Folgendes enthält:

* **Element:*****required*DOM-Element** : Das Element, das die in die App einzufügende Anzeige enthält.

**Asynchron**: Der Delegate gibt ein Objekt zurück, das Folgendes enthält: Der Delegate gibt ein Objekt zurück, das zwei Eigenschaften enthält: Element und Rückruf:

* **Element:*****required*DOM-Element** : Das Element, das die in die App einzufügende Anzeige enthält.
* **callback:*****erforderliche*Funktion** : Der Rückruf, der die Einfügung der Anzeige in das oben aufgeführte DOM-Element behandelt.

Für das `Conv` Objekt können Sie eine Zeichenfolge übergeben, um den Titel für den Anzeigenabschnitt anzugeben:

* **Zeichenfolgen:****(Optional)** - Dient zum Anpassen des Kopfzeilentextes für Ihre Anzeigen. Standardmäßig gesponsert.

## Synchrones Beispiel {#concept_E733E4431D9948638B8102ADE398735F}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```

## Asynchrones Beispiel {#concept_16B798C7EB20423DAA53ACCC71540051}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  function insertSlot(slotName) { 
    var adElem = document.createElement("img"); 
    var ad = "https://your-ad-here.com/great-ad-image.image"; 
    adElem.setAttribute("src", ad); 
    document.getElementById(slotName).appendChild(adElem); 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem, 
              callback: function() { 
                insertSlot(elem.id); 
              } 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```
