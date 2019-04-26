---
description: Hinzufügen von Live-Chat zu Ihrer Seite.
seo-description: Hinzufügen von Live-Chat zu Ihrer Seite.
seo-title: Chat
solution: Experience Manager
title: Chat
uuid: d 6761 a 69-efa 5-4 ad 3-abaf -1 ba 8 e 6 c 17 f 94
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Chat{#chat}

Hinzufügen von Live-Chat zu Ihrer Seite.

Chat ermöglicht es Ihren Zielgruppen, in Echtzeit zu unterhaltungen mit Live-Ereignissen zu interagieren. Der Inhalt wird als fortlaufender Stream angezeigt und fördert einen schnellen Beitrag im Dialogfeld zum Ausklappen.

Aktuelle Version: Chat verwendet `fyre.conv v3.0.0.`

## Integration{#concept_0A99792A7E89403F95D082D52D600F17}

Das Einbetten der Chat-App folgt dem Vorgang zum Einbetten einer Core-App, die unter Erste Schritte > [Einbetten einer App beschrieben](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps)wird.

Beispiel:

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(chatWidget) {}); 
        auth.delegate({ 
          login: function (callback) { 
            callback(null,{livefyre:'<userauthtoken>'}); 
          }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

Wie im [collectionmeta-Token](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) -Abschnitt vermerkt, ist collectionmeta ein kodiertes JSON-Objekt. Im obigen Beispiel akzeptiert das JSON-Objekt das folgende Format vor dem JWT-Codiert:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## Networkconfig-Objekt {#c-networkconfig-object}

Das `NetworkConfig` Objekt ist ein JSON-Objekt, das das Authentifizierungssystem für Netzwerkbenutzer anpasst.

`NetworkConfig` Das Objekt ist ein JSON-Objekt mit den folgenden Parametern:

| Parameter | Typ | Beschreibung |
|---|---|---|
| Authdelegate | *Erforderliches* Objekt | Dient zum Anpassen des Authentifizierungssystems für benutzerdefinierte Netzwerkbenutzer. |
| Netzwerk | *erforderliche* Zeichenfolge | Ein von Livefyre bereitgestellter Netzwerkname. Beispiel: *yourname. fyre. co.* |
| Attachmentdelegate | Objekt | Wird verwendet, um die im App-Stream sichtbaren Medienanlagen anzugeben. Weitere Informationen finden Sie unter [Medieneinschränkung](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| Zeichenfolgen | *Optionales* Objekt | Dient zum Anpassen von Textzeichenfolgen der HTML-Elemente in einem der Livefyre-Core-Apps. Weitere Informationen finden Sie unter [Zeichenfolgenanpassungen](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## Convconfig-Objekt {#c-convconfig-object}

Das `convConfig` Objekt ist ein JSON-Objekt, mit dem der Inhalt angegeben wird, den die Livefyre-App auf der Seite wiedergibt.

>[!NOTE]
>
>Die hier aufgeführten `convConfig` Objektparameter gelten nicht für die Review-App. Informationen zur Integration der App-App mit dem `convConfig` Objekt finden Sie unter Review-Integration.

Das `ConvConfig` Objekt enthält die folgenden erforderlichen Parameter:

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| Articleid | *erforderliche* Zeichenfolge | Identifiziert eindeutig eine Sammlung innerhalb Ihrer Site. Normalerweise entspricht dies einem primären Schlüssel oder einer Post-ID in Ihrem CMS. Beispiel: " post -42" . Max. 255 Zeichen. Hinweis: Wenn Sie die Artikel-URL als ihleid verwenden, stellen Sie sicher, dass die Zeichenfolge MD 5 oder SHA -1 kodiert ist. |
| Collectionmeta | *erforderliche* Zeichenfolge | JWT-kodierte Metadaten zur Sammlung. Weitere Informationen finden Sie unter [collectionmeta-Objekt](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent) . |
| el | *erforderliche* Zeichenfolge | Die ID eines DOM-Elements, an das der Inhaltsstream gerendert wird. |
| Siteid | *erforderliche* Zeichenfolge | Die von Livefyre bereitgestellte ID für die Website oder Anwendung, zu der die Sammlung gehört. Beispiel: " 303617" . |

>[!NOTE]
>
>Der `app` Parameter ist für die Implementierung einer Kommentar-App nicht erforderlich.

Das `ConvConfig` Objekt kann auch die folgenden optionalen Parameter enthalten:

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| Actionbuttons | *Optionales* Array | Ein Array von benutzerdefinierten Aktionsschaltflächen, die einem Inhaltselement neben den Schaltflächen "Freigeben" und" Markieren" hinzugefügt werden können. Weitere Informationen finden Sie unter Hinzufügen benutzerdefinierter Schaltflächen. |
| Animationen | *Optionales* Boolesches Zeichen | Definiert, ob Animationen in der Livefyre-App ausgeführt werden. Legen Sie "false" fest, um Animationen zu deaktivieren. Der Standardwert ist "true" . |
| Anonymousflaggingenabled | *Optionales* Boolesches Zeichen | Definiert, ob Gastbenutzer über die Option zum Kennzeichnen von Inhalten verfügen. Der Standardwert ist "true" . |
| Browsertype | *optionale* Zeichenfolge | Definiert das Gerät, für das Inhalte angezeigt werden sollen. Dies führt dazu, dass die CSS und einige Funktionen an den Eingabegerätetyp angepasst werden. Die Optionen sind Desktop, Mobilgerät oder Tablet. (Falls leer, wird standardmäßig die Google Agent-Bestimmung für das Anzeigeformat verwendet.) |
| checksum | *Empfohlene* Zeichenfolge (empfohlen) | Gibt den aktuellen Status der collectionmeta an. Wenn Sie diesen Wert ändern, aktualisiert Livefyre die Daten auf dem Server mit den neuen Werten in collectionmeta. |
| Datetimeformat | *optionale* Zeichenfolgenobjekt Funktion | Gibt das Datums-Uhrzeitformat für gestreamte Inhalte an. Weitere Informationen finden Sie unter Datum und Uhrzeitstempel anpassen. |
| Disableavatars | *Optionales* Boolesches Zeichen | Verhindert, dass Avatare im App-Stream wiedergegeben werden, wodurch die Anzahl der in den Browser geladenen Elemente verringert wird. Der Standardwert ist "false" . |
| disableIE8Shim | *Optionales* Boolesches Zeichen | Deaktiviert den standardmäßigen Shiv, der von Livefyre verwendet wird, um Internet Explorer 8 zu füllen, damit HTML 5-Elemente unterstützt werden. Livefyre verwendet das folgende Projekt: [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv). Der Standardwert ist "false" . Hinweis: Wenn dieser Wert false ist, muss die Polyfüllung einiger Sortiervorgänge verwendet werden, bevor Livefyre Chat für den Internet Explorer 8-Support aufgerufen wird. |
| Disablethirdpartyanalytics | *optionales* bboolean | Deaktiviert Analytics-Systeme (Quantserve und Google Analytics) von Drittanbietern, die von Livefyre für interne Messungen verwendet werden können. Der Standardwert ist "false" . |
| Editorcss | *Optionales* Objekt | Wird verwendet, um den Stil des Kommentareditors anzupassen. Sie können die Hintergrundfarbe des Editors sowie die Schriftfarbe, -größe und -familie im Editor gestalten. Beispiel: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| Initialnumvisible | *optionale* Ganzzahl | Hiermit können Sie die Standardmäßige Anzahl der in Ihrer App sichtbaren Kommentare beim Laden festlegen. Dies kann eine Ganzzahl von 1 bis 50 sein. |
| Initialnumvisiblelegacy | *optionale* Ganzzahl | Hiermit können Sie die Standardanzahl älterer Inhaltselemente, die in Ihrer App angezeigt werden, beim Laden festlegen. Dies kann eine Ganzzahl von 1 bis 50 sein. Wenn dieser Parameter nicht angegeben ist, ist der Standardwert initialnumvisible. Beispiel: Wenn Ihre Sammlung 100 aktive und 100 Legacy-Kommentare enthält, legen Sie initalnumvisible fest: 10 und initialnumvisiblelegacy: 5, um 10 aktive Kommentare (mit der Schaltfläche "Mehr anzeigen" ) + 5 Archivkommentare (mit der Schaltfläche" Mehr anzeigen" ) anzuzeigen. |
| Maxvisible | *optionale* Ganzzahl | Legt die maximale Anzahl an sichtbaren Elementen der obersten Ebene in der Chat-App fest. Wenn neue Elemente des Inhalts in enthalten sind, werden Inhalte am unteren Rand des Streams aus der Seite entfernt. Wenn die Schaltfläche Mehr… angeklickt wird, wird der Parameter ignoriert und der Benutzer kann so viele Inhalte wie gewünscht anzeigen. (Mit diesem Parameter steuern Sie die Anzahl der Elemente, die auf der Seite in hohen Geschwindigkeitsstreams angezeigt werden.) |
| Posttobuttons | *Optionales* Array | Wird verwendet, um zu konfigurieren, welche Anbieter beim Einbetten der Live Blog-App angezeigt werden. Verfügbare Optionen sind tw (Twitter), fb (Facebook) und li (linkedin). Standard ist [ tw, fb ]. |
| Readonly | *Optionales* Boolesches Zeichen | Deaktiviert alle Interaktivität für die Sammlung. Wenn "true" , können Benutzer sich nicht im Stream anmelden und können Inhalt nicht posten, bearbeiten, auf Antworten oder" Gefällt mir" klicken. Wenn "true" , können Benutzer Inhalte kennzeichnen und freigeben. Der Standardwert ist "false" . |
| Stream | *Optionales* Objekt | Enthält Optionen zum Konfigurieren der App. |
| stream. catchup | *optionale* Ganzzahl | Gibt an, wie viele Sekunden vor dem aktuellen Zeitpunkt der Stream geladen werden soll. Standardmäßig lädt Livefyre 50 Inhaltselemente und lädt dann alle zwischen diesen und der aktuellen Zeit gesendeten Inhalte. In sehr schnellen Anwendungsfällen kann der Inhalt zu schnell gepostet werden, damit die App auf die vorhandene Weise abfängt. Verwenden Sie diese Einstellung, um die Anzahl der Sekunden zu definieren, für die Inhalte veröffentlicht werden (nach dem anfänglichen Ladevorgang für Inhalte). |
| stream. delay | *optionale* Ganzzahl | Gibt die Anzahl der Sekunden zwischen den Streaming-Anforderungen an. Verwenden Sie diesen Parameter, um den Inhaltsfluss zu steuern und zu verzögern, wie oft das DOM aktualisiert wird. Hinweis: Wenn der Stream zu groß ist, kann er hinter den Erwartungen zurückbleiben. |


>[!NOTE]
>
>Sie können ein oder mehrere `convConfig` Objekte während der App-Initialisierung übergeben, um mehrere Apps auf derselben Seite anzuzeigen. Beachten Sie, dass zusätzliche Apps Browserressourcen verwenden und die Leistung beim Anstieg möglicherweise beeinträchtigt wird.

## Collectionmeta-Objekt {#c-collectionmeta-object}

`CollectionMeta` Das Objekt ist ein JSON-Objekt, das Metadaten angibt, die in der Sammlung gespeichert werden sollen.

`CollectionMeta` immer kodiert wird, bevor sie an Livefyre zur Sicherheit übergeben werden. Der kodierte Wert wird an das oben aufgeführte `ConvConfig` Objekt übergeben.

>[!NOTE]
>
>Sie müssen serverseitigen Code hinzufügen, um das `CollectionMeta` JSON-Objekt zu kodieren. Weitere Informationen finden Sie unter Erstellen serverseitiger Token.

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| Articleid | *erforderliche* Zeichenfolge | Eine eindeutige ID für die Sammlung. |
| Titel | *erforderliche* Zeichenfolge | Der Titel, den Sie auf die Sammlung anwenden möchten. Dies entspricht häufig dem Titel der Seite, auf der die App angezeigt wird. Beispiel: " Integration ist so viel Spaß! » Hinweis: Die maximale Zeichenlänge für den Titel beträgt 255 Zeichen. Das Titelfeld unterstützt keine HTML-Entitäten. Bitte Sonderzeichen mit UTF -8 kodieren. |
| url | *erforderliche* Zeichenfolge | Die kanonische absolute URL, die an diese Sammlung angehängt werden soll. Diese URL wird verwendet, um Links aus Inhalten, die auf Facebook und Twitter, E-Email-Benachrichtigungen und Livefyre Studio freigegeben wurden, wiederherzustellen. Hinweis: Livefyre erfordert die Verwendung eines vollständig qualifizierten Domänennamens; die Anschlussnummer oder ein Rückruf zur Auflösung der lokalen Einrichtung nicht erforderlich ist. Sollten Sie lokal testen, sollten Sie sicher sein, eine gültige Basis-URL-Domäne zu verwenden. (Beispiel: `https://customer.com` ist gültig, `https://localhost:5995` aber nicht.) Nachdem Sie einen lokalen Webserver eingerichtet haben, um einen vollständig qualifizierten Domänennamen zu akzeptieren, sind keine Rückrufe oder Auflösungen erforderlich und die lokale Entwicklung kann wie erwartet fortgesetzt werden. |
| type | *erforderliche* Zeichenfolge | Der Sammlungstyp. Muss Livechat sein. |

Das `CollectionMeta` Objekt kann auch den folgenden optionalen Parameter enthalten:

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| Tags | *optionale* Zeichenfolge | Eine kommagetrennte Liste mit einzelnen Suchbegriffen oder -phrasen. Suchen Sie Sammlungen nach Tags in Studio oder mit der Such-API. Hinweis: Während Tags, die über Studio hinzugefügt wurden, Leerzeichen enthalten können, können Tags, die über die API eingegeben wurden, nicht verwendet werden. Verwenden Sie Unterstriche, um Tags zu definieren, die in der Benutzeroberfläche Leerzeichen anzeigen. (Beispiel: use Monday_ Quarterback to Display Monday Quarterback in Studio.) |

## Hinzufügen eines Ereignishandlers {#concept_E7C17EFB43F24F1A8572E60C69176C6D}

Um Ereignishandler zu registrieren, verwenden Sie den Aufruf widget. on innerhalb der Callback-Funktion der App.

Beispiel:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

Weitere Informationen und eine Liste der verfügbaren Ereignisse finden Sie unter [Javascript-Ereignisse](../c-app-customizations/c-javascript-events.md#c_javascript_events).
