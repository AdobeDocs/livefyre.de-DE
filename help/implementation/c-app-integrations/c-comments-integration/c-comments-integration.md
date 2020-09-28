---
description: Aktivieren Sie Live-Kommentare auf Ihrer Seite.
seo-description: Aktivieren Sie Live-Kommentare auf Ihrer Seite.
seo-title: Kommentare
solution: Experience Manager
title: Kommentare
uuid: decad9b0-2074-4748-bd77-914008817bfa
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Kommentare{#comments}

Aktivieren Sie Live-Kommentare auf Ihrer Seite. Mit Kommentaren können Sie Ihr Standard-Kommentarsystem durch Echtzeitkonversationen auf Ihrer Seite ersetzen.

## Integration {#concept_4093E8BAA96A464BA74D263DA031C0B0}

Das Einbetten der Kommentaranwendung erfolgt nach dem Einbetten einer Core-App, wie unter Erste Schritte &gt; Einbetten einer App beschrieben.

### Beispiel 

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
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

Wie im Abschnitt zum Erstellen von CollectionMeta angegeben, ist CollectionMeta ein kodiertes JSON-Objekt. Im obigen Beispiel nimmt das JSON-Objekt das folgende Format vor, bevor es JWT-kodiert wird:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

## NetworkConfig-Objekt {#c-networkconfig-object}

Das `NetworkConfig` Objekt ist ein JSON-Objekt, das das Authentifizierungssystem für Netzwerkbenutzer angepasst.
Das `NetworkConfig` Objekt ist ein JSON-Objekt, das die folgenden Parameter enthält:

| Parameter | Typ | Beschreibung |
|---|---|---|
| **authDelegate** | *erforderliches* Objekt | Dient zum Anpassen des Authentifizierungssystems für benutzerdefinierte Netzwerkbenutzer. |
| **network** | Zeichenfolge *erforderlich* | Ein von Livefyre bereitgestellter Netzwerkname. Beispiel: *yourname.fyre.co.* |
| **attachmentDelegate** | *optionales* Objekt | Dient zum Festlegen der Arten von Medienanlagen, die im App-Stream sichtbar sind. Weitere Informationen finden Sie unter [Eingrenzen von Medien](/help/implementation/c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **Strings** | *optionales* Objekt | Dient zum Anpassen von Textzeichenfolgen der HTML-Elemente in allen Livefyre-Core-Apps. Weitere Informationen finden Sie unter [Zeichenfolgenanpassung](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## ConvConfig-Objekt {#c-convconfig-object}

Das `convConfig` Objekt ist ein JSON-Objekt, mit dem der Inhalt, den die Livefyre-App auf der Seite wiedergibt, angegeben wird.

>[!NOTE]
>
>Die hier aufgeführten `convConfig` Objektparameter gelten nicht für die Reviews-App. Integrationsinformationen zur Reviews-App mit dem `convConfig` Objekt finden Sie unter Integration von Reviews.

Das `ConvConfig` Objekt enthält die folgenden erforderlichen Parameter:

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| **articleId** | *erforderliche* Zeichenfolge | Identifiziert eine Sammlung innerhalb Ihrer Site eindeutig. Normalerweise entspricht dies einem primären Datenbankschlüssel oder einer Post-ID in Ihrem CMS. Beispiel: "post-42". Längenbeschränkung von 255 Zeichen.  Hinweis:  Wenn Sie die Artikel-URL als articleId verwenden, stellen Sie sicher, dass die Zeichenfolge MD5- oder SHA-1-kodiert ist. |
| **authPageReload** | *optional* boolesch | Gilt für Kommentar-App: Damit können Sie steuern, ob der Kommentar eines Benutzers während des Authentifizierungsprozesses lokal gespeichert wird. Wenn "true"(wahr), wenn ein Benutzer einen Kommentar eingibt und sich dann bei der App anmeldet, wird der Kommentar lokal gespeichert und nach der Anmeldung und Aktualisierung der Seite erneut in das Inhaltsfeld eingegeben. Wenn "false", werden die eingegebenen Inhalte während des Anmeldeprozesses gelöscht und müssen erneut eingegeben werden. |
| **collectionMeta** | *erforderliche* Zeichenfolge | JWT-kodierte Metadaten zur Sammlung. Weitere Informationen finden Sie unter [CollectionMeta](#c_collectionmeta_object) -Objekt. |
| **el** | *erforderliche* Zeichenfolge | Die ID eines DOM-Elements, an das der Inhaltsstream gerendert wird. |
| **siteId** | *erforderliche* Zeichenfolge | Die von Livefyre bereitgestellte ID für die Website oder Anwendung, zu der die Sammlung gehört. Beispiel: "303617". |

>[!NOTE]
>
>Der `app` Parameter ist für eine Comments App-Implementierung nicht erforderlich.

Das `ConvConfig` Objekt kann auch die folgenden optionalen Parameter enthalten:

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| **actionButtons** | *optionales* Array | Ein Array mit benutzerdefinierten Aktionsschaltflächen, die einem Inhaltselement neben den Schaltflächen "Freigeben"und "Flag"hinzugefügt werden. Weitere Informationen finden Sie unter Hinzufügen benutzerdefinierter Schaltflächen. |
| **Animationen** | *optional* boolesch | Definiert, ob Animationen innerhalb der Livefyre-App ausgeführt werden. Auf "false"setzen, um Animationen zu deaktivieren. Der Standardwert ist true. |
| **anonymousFlaggingEnabled** | *optional* boolesch | Definiert, ob Gastbenutzer die Möglichkeit haben, Inhalte zu kennzeichnen. Der Standardwert ist "true". |
| **browserType** | *optionale* Zeichenfolge | Definiert das Gerät, für das Anzeigeninhalte generiert werden sollen. Dies führt dazu, dass sich das CSS und einige Funktionen an den Gerätetyp anpassen. Die Optionen sind Desktop, Mobil oder Tablet. (Wenn das Feld leer gelassen wird, wird standardmäßig die Google Agent-Bestimmung für das Anzeigeformat verwendet.) |
| **checksum** | *Empfohlene* Zeichenfolge | Gibt den aktuellen Status von CollectionMeta an. Wenn Sie diesen Wert ändern, aktualisiert Livefyre die Daten auf dem Server mit den neuen Werten in CollectionMeta. |
| **datetimeFormat** | *Optionale* Zeichenfolgenobjektfunktion | Gibt das Datumsformat des Streaminhalts an. Weitere Informationen finden Sie unter Anpassen von Datums- und Uhrzeitstempeln. |
| **disableAvatars** | *optional* boolesch | Verhindert, dass Avatare im App-Stream wiedergegeben werden, und verringert so die Anzahl der Elemente, die in den Browser geladen werden. Standard ist „false“. |
| **disableIE8Shim** | *optional* boolesch | Deaktiviert die standardmäßige Shiv-Datei, die von Livefyre zum Polyfill von Internet Explorer 8 verwendet wird, sodass HTML5-Elemente unterstützt werden. Livefyre verwendet das folgende Projekt:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . Standard ist „false“.  Hinweis:  Wenn dieser Wert "false"ist, muss eine Art von Polyfill verwendet werden, bevor Livefyre Chat für die Unterstützung von Internet Explorer 8 aufgerufen wird. |
| **disableThirdPartyAnalytics** | *optional* boolesch | Deaktiviert Analysesysteme von Drittanbietern (Quantserve und Google Analytics), die Livefyre für interne Messungen verwenden kann. Standard ist „false“. |
| **editorCss** | *optionales* Objekt | Dient zum Anpassen der Formatierung des Kommentareditors. Sie können die Hintergrundfarbe des Editors sowie die Schriftfarbe, -größe und -familie des Textes im Editor gestalten.  Beispiel: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| **initialNumVisible** | *optional* ganze | Damit können Sie die Standardanzahl der Kommentare festlegen, die beim Laden in Ihrer App angezeigt werden. Dies kann eine Ganzzahl von 1 bis 50 sein. |
| **initialNumVisibleLegacy** | *optional* ganze | Ermöglicht Ihnen, die Standardanzahl der Elemente aus alten Inhalten festzulegen, die beim Laden in Ihrer App sichtbar sind. Dies kann eine Ganzzahl von 1 bis 50 sein. Wenn dieser Parameter nicht angegeben ist, wird standardmäßig initialNumVisible verwendet.  Beispiel: Wenn Ihre Sammlung 100 aktive und 100 ältere Kommentare enthält, stellen Sie initalNumVisible:10 und initialNumVisibleLegacy:5 ein, um 10 aktive Kommentare (mit der Schaltfläche "Mehr anzeigen") und 5 Archivkommentare (mit der Schaltfläche "Mehr anzeigen") anzuzeigen. |
| **maxVisible** | *optional* ganze | Legt die maximale Anzahl sichtbarer Inhalte der obersten Ebene in der Chat-App fest. Wenn neue Inhaltselemente in den Stream eindringen, werden Inhalte am unteren Rand des Streams von der Seite entfernt. Wenn auf die Schaltfläche Mehr... anzeigen geklickt wird, wird der Parameter ignoriert und der Benutzer kann so viele Inhalte wie gewünscht anzeigen. (Verwenden Sie diesen Parameter, um die Anzahl der Elemente zu steuern, die in Hochgeschwindigkeits-Streams auf der Seite angezeigt werden.) |
| **postToButtons** | *optionales* Array | Dient zum Konfigurieren der Anbieter, die beim Einbetten der Live-Blog-App angezeigt werden. Verfügbare Optionen sind zwei (Twitter), fb (Facebook) und li (LinkedIn). Die Standardeinstellung ist [ tw , fb ]. |
| **readOnly** | *optional* boolesch | Deaktiviert alle Interaktivität für die Sammlung. Wenn "true", können sich Benutzer nicht beim Stream anmelden und können keine Inhalte posten, bearbeiten, beantworten oder "Gefällt mir"-Klicks verwenden. Wenn "true", können Benutzer Inhalte kennzeichnen und freigeben. Standard ist „false“. |
| **stream** | *optionales* Objekt | Enthält Optionen zum Konfigurieren des Streaming der App. |
| **stream.catchup** | *optional* ganze | Gibt an, wie viele Sekunden vor dem aktuellen Moment der Stream geladen werden soll. Standardmäßig lädt Livefyre 50 Inhaltselemente und lädt dann alle zwischen diesen und der aktuellen Zeit gesendeten Inhalte. In sehr schnellen Anwendungsfällen können Inhalte zu schnell veröffentlicht werden, um der App eine "Aufholung"zu ermöglichen. Verwenden Sie diese Einstellung, um die Anzahl der Sekunden vor dem ersten Laden festzulegen, für die Inhalte veröffentlicht werden (nach dem ersten Laden). |
| **stream.delay** | *optional* ganze | Gibt die Anzahl der Sekunden zwischen Streaming-Anforderungen an. Verwenden Sie diesen Parameter, um den Inhaltsfluss zu steuern und zu verzögern, wie oft das DOM aktualisiert wird.  Hinweis:  Wenn der Stream zu groß ist, kann er zurückfallen. |


>[!NOTE]
>
>Sie können ein oder mehrere `convConfig` Objekte während der App-Initialisierung übergeben, um mehrere Apps auf derselben Seite anzuzeigen. Beachten Sie, dass zusätzliche Apps Browser-Ressourcen verwenden und die Leistung abnehmen kann, wenn die Anzahl steigt.

## CollectionMeta-Objekt {#c-collectionmeta-object}

Das `CollectionMeta` Objekt ist ein JSON-Objekt, das die in der Sammlung zu speichernden Metadaten angibt.

`CollectionMeta` wird immer kodiert, bevor sie zur Sicherheit an Livefyre übergeben wird. Der kodierte Wert wird an das oben dargestellte `ConvConfig` Objekt übergeben.

>[!NOTE]
>
>Sie müssen serverseitigen Code hinzufügen, um das JSON- `CollectionMeta` Objekt zu kodieren. Weitere Informationen finden Sie unter Erstellen von serverseitigen Tokens.

| Parameter | Typ | Beschreibung |
|--- |--- |--- |
| **articleId** | *erforderliche* Zeichenfolge | Eine eindeutige ID für die Sammlung. |
| **Titel** | *erforderliche* Zeichenfolge | Der Titel, den Sie auf die Sammlung anwenden möchten. Dies entspricht oft dem Titel der Seite, auf der die App angezeigt wird.  Beispiel: "Integration macht so viel Spaß!" <br>**** Hinweis:  Die maximale Zeichenlänge für den Titel beträgt 255 Zeichen. Das Titelfeld unterstützt keine HTML-Entitäten. Bitte kodieren Sie Sonderzeichen mit UTF-8. |
| **url** | *erforderliche* Zeichenfolge | Die kanonische absolute URL, die Sie dieser Sammlung hinzufügen möchten. Diese URL wird verwendet, um aus Inhalten, die auf Facebook und Twitter freigegeben wurden, E-Mail-Benachrichtigungen und Livefyre Studio Links zur App zu generieren.  <br>**Beachten** Sie, dass Livefyre die Verwendung eines vollständig qualifizierten Domänennamens erfordert; die Anschlussnummer oder ein Rückruf zur Auflösung des lokalen Setups ist nicht erforderlich. Stellen Sie bei lokalen Tests sicher, dass eine gültige Basis-URL-Domäne verwendet wird. <br>Beispiel: ist gültig, `https://customer.com` `https://localhost:5995` nicht jedoch. Nachdem Sie Ihren lokalen Webserver so eingerichtet haben, dass er einen vollständig qualifizierten Domänennamen akzeptiert, sind keine Rückrufe oder Lösungen erforderlich und die lokale Entwicklung kann wie erwartet fortgesetzt werden. |
| **type** | *erforderliche* Zeichenfolge | Der Sammlungstyp. Muss `livechat`sein. |

Das `CollectionMeta` Objekt kann auch den folgenden optionalen Parameter enthalten:

| Parameter | Typ | Beschreibung |
|---|---|---|
| **Tags** | *optionale* Zeichenfolge | Eine kommagetrennte Liste mit einzelnen Suchbegriffen oder Ausdrücken. Suchen Sie Sammlungen nach Tags in Studio oder mit der Such-API. <br> **** Hinweis: Tags, die über Studio hinzugefügt werden, können zwar Leerzeichen enthalten, Tags, die über die API eingegeben wurden, können jedoch nicht verwendet werden. Verwenden Sie Unterstriche, um Tags zu definieren, die Leerzeichen in der Benutzeroberfläche anzeigen. (Beispiel: Verwenden Sie `Monday_Quarterback` diese Option, um "Montag Quarterback"in Studio anzuzeigen.) |

## Hinzufügen eines Ereignishandlers {#concept_06D8B811C98B4CC6B38C6340EBA176E5}

Um Ereignishandler zu registrieren, verwenden Sie den widget.on-Aufruf in der Rückruffunktion der App.

### Beispiel

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```
