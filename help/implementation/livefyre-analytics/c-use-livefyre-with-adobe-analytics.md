---
description: 'null '
seo-description: 'null '
seo-title: Verwenden von Livefyre mit Adobe Analytics und Dynamischem Tag-Manager (DTM) lk xavvn vefyre mit Adobe Analytics und Dynamischer Tag-Manager (DTM)
uuid: 9 a 1 c 25 c 0-c 474-46 ff -82 ac-e 89357007 c 7 f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

---


# Verwenden von Livefyre mit Adobe Analytics und dynamischem Tag-Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Richten Sie Adobe Analytics und Dynamisches Tag-Manager (DTM) ein, um Daten für Livefyre-Apps zu erfassen.

## Schritt 1: Einrichten von Ereignissen in Adobe Analytics {#section_iks_kgd_4cb}

Ordnen Sie Livefyre-Ereignisse einem oder mehreren benutzerspezifischen Erfolgsereignissen im Adobe Analytics Report Suite Manager zu.

Weitere Informationen zu Report Suite Manager finden Sie unter [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html).

1. Melden Sie sich bei Adobe Analytics als Administrator an.
1. Öffnen Sie Adobe Analytics Admin Report Suite Manager.
1. Erstellen Sie eine neue Report Suite oder wählen Sie eine vorhandene Report Suite aus.
1. Bearbeiten Sie die Report Suite, indem Sie auf die Report Suite klicken, um sie zu ändern, und navigieren **[!UICONTROL Edit Settings > Conversion > Success Events]** Sie zu dem Bericht.
1. Ordnen Sie die Livefyre-Ereignisse einem oder mehreren benutzerspezifischen Erfolgsereignissen zu.

## Schritt 2: Konversion-Variablen einrichten

Ordnen Sie Livefyre-Konversionsvariablen (evars) Konversionsvariablen in Adobe Analytics Admin Report Suite Manager zu. Konversionsvariablen funktionieren wie eine Sortierfunktion, um zu bestimmen, wie Sie die von Livefyre-Ereignissen erfassten Daten identifizieren möchten.

1. Klicken **[!UICONTROL Edit Settings > Conversion > Conversion Variables]** Sie im Report Suite Manager auf.
1. Wählen Sie die benutzerdefinierten Konversionsvariablen (evars) aus, die Sie verwenden möchten, und ordnen Sie sie den Livefyre-Konversionsvariablen zu. So ordnen Sie eine Livefyre-Konversionsvariable einer benutzerdefinierten Konversionsvariablen zu:
* Konversionsvariable aktivieren
* Benennen Sie die Konversionsvariable.
* Geben Sie der Konversionsvariablen einen Typ
1. Speichern Sie die benutzerdefinierten Konversionsvariablen.

## Schritt 3: DTM zum Hinzufügen Ihrer Report Suite mit Livefyre-Ereignissen verwenden {#section_t15_2hd_4cb}

Fügen Sie Adobe Analytics zu DTM hinzu, um Analytics zu erhalten. Erstellen Sie hierfür eine neue Eigenschaft und ein neues Tool und fügen Sie die neue Report Suite mit Livefyre-Ereignissen für die Eigenschaft hinzu. Weitere Informationen zu DTM finden Sie unter [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

Sie müssen diesen Schritt nicht ausführen, wenn bereits eine Eigenschaft oder ein Tool für die Report Suite eingerichtet ist, die Sie mit Livefyre-Ereignissen eingerichtet haben.

1. Erstellen oder bearbeiten Sie in DTM eine vorhandene Eigenschaft.
1. Erstellen oder bearbeiten Sie ein vorhandenes Adobe Analytics-Tool.
1. Wenn ein vorhandenes Adobe Analytics-Tool nicht vorhanden ist, klicken Sie auf die **[!UICONTROL Add a Tool]** Schaltfläche.
Legen Sie die folgenden Parameter für das Tool fest:
* Auf **[!UICONTROL Tool Type]****[!UICONTROL Adobe Analytics]**.
* Enable **[!UICONTROL Automatic Configuration]**.
* Enable **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Fügen Sie dem **[!UICONTROL Report Suites]** Feld den Namen der Report Suite mit Livefyre-Ereignissen hinzu oder bestätigen Sie ihn.

## Schritt 4: Einrichten einer Seitenladeregel zum Einrichten der Analytics-Bearbeitung {#section_jfj_j3d_4cb}

Richten Sie eine Seitenladeregel ein, um alle Daten abzurufen. Mit der Seitenladeregel können Sie benutzerdefinierte javascript in die Regel einfügen, die das Ereignis beim Laden der Seite aufzeichnet.

>[!NOTE]
>
>Verwenden Sie keine ereignisbasierten Regeln oder Regeln für Direktaufrufe.

1. Wählen Sie in DTM **[!UICONTROL Rules]** die Registerkarte.
1. Klicken **[!UICONTROL Page Load Rules]** Sie auf.
1. Klicken **[!UICONTROL Create New Rule]** Sie auf die Schaltfläche.
1. Öffnen Sie den **[!UICONTROL Conditions]** Abschnitt, indem Sie auf die **[!UICONTROL Plus]** Schaltfläche klicken.
1. Auslösen Sie die Regel. Wählen oder **[!UICONTROL DOM Ready]****[!UICONTROL Onload]** lösen Sie Typen aus, wenn Sie die Regel asynchron verzögern oder implementieren möchten.
1. (Optional) Fügen Sie zusätzliche Parameter hinzu, um die Seiten zu beschränken, die Livefyre-Apps anzeigen. Weitere Informationen zu weiteren Konfigurationsoptionen finden Sie unter [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. Klicken **[!UICONTROL Javascript/ Third Party Tags]** Sie unter, klicken Sie auf die **[!UICONTROL Non-sequential]** Registerkarte **[!UICONTROL Add New Script]** und klicken Sie dann auf.
1. Wählen **[!UICONTROL Sequential HTML]** Sie als Skripttyp.
1. Fügen Sie dem Code-Editor das folgende Skript hinzu und klicken **[!UICONTROL Save Code]**Sie auf.
Das folgende Skript ruft die `livefyre_analytics` Direktaufrufregel auf, nachdem das Livefyre javascript geladen wurde. Das folgende Skript-Beispiel überprüft alle 400 ms, um zu sehen, ob `livefyre.analytics` sich die Seite auf der Seite befindet. Nach dem Laden der Seite sendet livefyre. analytics die Verfolgungsinformationen.

```
/** 
* Poll for Livefyre.analytics object to exist since it gets loaded via the 
* Livefyre.js JavaScript file. Depending on the timing, this could already 
* exist or need a little time. 
*/ 
function pollForAnalytics() {  
 if (Livefyre.analytics) { 
   _satellite.track('livefyre_analytics'); 
     return true; 
   } 
   setTimeout(pollForAnalytics, 400); 
} 
  
setTimeout(pollForAnalytics, 400);
```

1. Klicken **[!UICONTROL Save Code]** Sie auf.
1. Klicken **[!UICONTROL Save Rule]** Sie auf.

## Schritt 5: Erstellen einer Direktaufrufregel zum Erstellen der Adobe Analytics-Zuordnungskonfiguration für Livefyre {#section_gvp_b1g_pdb}

Es gibt andere Möglichkeiten, Livefyre mit DTM zu implementieren, indem Sie benutzerdefinierte Ereignisse, die Benutzeroberfläche von Adobe Analytics innerhalb von DTM und Datenelemente verwenden. Dieses Dokument verwendet benutzerdefiniertes Javascript, um denselben Effekt zu erzielen.

1. Wählen Sie in DTM die **Registerkarte Regeln** und klicken Sie dann auf **Regeln für Direktaufrufe**.
1. Klicken Sie auf **die Schaltfläche Neue Regel** erstellen.
1. Benennen Sie die neue Regel **Livefyre Analytics**.
1. Erweitern Sie den **Konfigurationsbereich für Bedingungen** .
1. Geben Sie in das **Feld String** `livefyre_analytics`Folgendes ein.
1. Erweitern Sie den Abschnitt &quot;Javascript-/Drittanbieter-Tag&quot; und klicken Sie auf die Schaltfläche&quot; Neuen **Skript** hinzufügen&quot; .
1. Geben Sie **in** das Eingabefeld **&quot;Tag-Name** &quot; die Livefyre Analytics-Konfiguration ein.
1. Wählen **Sie Nicht sequenzielles Javascript**.
1. Geben Sie den folgenden Livefyre-Konfigurationscode in den Code-Editor ein und klicken Sie auf **&quot;Code** speichern&quot; .

   ```
   var s = _satellite.getToolsByType('sc')[0].getS(); 
   
   var evarMap = {  
     appId: 'eVar81',  
     appType: 'eVar82' 
   }; 
   
   var eventMap = { 
     FlagCancel: 'event82',  
     FlagClick: 'event82',  
     FlagDisagree: 'event82',  
     FlagOffensive: 'event82',  
     FlagOffTopic: 'event82',  
     FlagSpam: 'event82',  
     Like: 'event82', 
     Load: 'event81',  
     RequestMore: 'event82',  
     ShareButtonClick: 'event82',  
     ShareFacebook: 'event82',  
     ShareOnPostClick: 'event82',  
     ShareTwitter: 'event82',  
     ShareURL: 'event82',  
     SortStream: 'event82',  
     TwitterLikeClick: 'event82', 
     TwitterReplyClick: 'event82',  
     TwitterRetweetClick: 'event82',  
     TwitterUserFollow: 'event82' 
   }; 
   
    function trackLivefyreEvent(data) {  
     var event = eventMap[data.type]; 
     console.log('Track:', data.type, event); 
   
     if (!event) { 
       console.warn(data.type, 'is not mapped   to an event in AA');  
       return; 
     } 
     var vars = ['events'];  
     switch (event) { 
       case 'event82': s.eVar83 = data.type;  
         vars.push('eVar83');  
         break; 
       default: 
     } 
       ['generator', 'evars'].forEach(function (type) {  
       var obj = data[type]; 
       for (var d in obj) { 
         if (obj.hasOwnProperty(d) && evarMap[d]) {  
           s[evarMap[d]] = obj[d];  
           vars.push(evarMap[d]); 
         } 
       } 
     }); 
     s.linkTrackVars = vars.join(',');  
     s.linkTrackEvents = event;  
     s.events = event; 
   
     console.log('linkTrackVars:',  s.linkTrackVars);  
     console.log('linkTrackEvents:',  s.linkTrackEvents);  
     console.log('events:', s.events); 
     s.tl(); 
    } 
   ]
   
   /** 
   ```

* Fügt einen Analytics-Handler für alle Analyseereignisse von Livefyre hinzu. Für jedes Ereignis werden die Daten auf ein globales Objekt gesetzt und anschließend das Ereignis ausgelöst.

   ```
   */ 
    function addAnalyticsHandler() {  
      Livefyre.analytics.addHandler(function (events) { 
        (events || []).forEach(function (data) {  
          console.log('Event handled:', data.type);  
          trackLivefyreEvent(data); 
        }); 
      }); 
    } 
    addAnalyticsHandler(); 
   
```
1. Click on **Save Rule**.

## Step 6: Approve changes for Page Load Rule {#section_pxc_11t_ycb}

1. Go to **[!UICONTROL Approvals]** tab.
1. Click **[!UICONTROL Approve]**.
1. Click **[!UICONTROL Yes, approve]** to confirm your approval.
1. Go to **[!UICONTROL Overview > Publish Queue]**.
1. Select the Rule to publish.
1. Click **[!UICONTROL Publish Selected]**.
1. Click **[!UICONTROL Publish]** to confirm that you want to publish.

## Script {#section_xkb_vft_mcb}

The following sample code maps the specific eVars to available Livefyre eVars. The Livefyre conversion variable ( `eVar`) name (for example, `appId`) maps to the name you set up in the Report Suite Manager (for example, `eVar81`). Change the `eVar` names in this script to the custom conversion variables.
```

var s =_ satellite. gettoolsbytype`('sc')[0]`. getS ();
var evarmap = {appid: &#39; Evar 81 &#39;,
apptype: &#39; Evar 82 &#39;};

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventmap = {Flag
FlagCancel: &#39; event 82 &#39;,\
Flagclick: &#39; event 82 &#39;,\
Kennzeichnung: &#39; event 82 &#39;,\
Flagpression: &#39; event 82 &#39;,\
Flagofftopic: &#39; event 82 &#39;,\
Flagspam: &#39; event 82 &#39;,\
Gefällt mir: &#39; event 82 &#39;,
Load: &#39; event 81 &#39;,\
Requestmore: &#39; event 82 &#39;,\
Sharebuttonclick: &#39; event 82 &#39;,\
Sharefacebook: &#39; event 82 &#39;,\
Shareonpostclick: &#39; event 82 &#39;,\
Sharetwitter: &#39; event 82 &#39;,\
Shareurl: &#39; event 82 &#39;,\
Sortstream: &#39; event 82 &#39;,\
Twitterlikeclick: &#39; event 82 &#39;,
twitterreplyclick: &#39; event 82 &#39;,\
Twitterretweetclick: &#39; event 82 &#39;,\
Twitterusvariablow: &#39; event 82 &#39;};

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function tracklivefyreevent (data) {\
var event = eventmapdata[. type];
console. log (&#39; Track: &#39;, data. type, event);

if (! event) {console.
warn (data. type, &quot;is not mapped to a event in AA &#39;);\
return;}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars = [&#39; events &#39;];\
switch (event) {case&#39;event
82 &#39;: s. evar 83 = data. type;\
vars. push (&#39; evar 83 &#39;);\
break;
Standard:}

[&#39; generator &#39;,&#39; evars &#39;]. foreach (function (type) {\
var obj = datatype[];
for (var d in obj) {if
(obj. hasownproperty (d) &amp; &amp; evarmapd[]) {\
s [evarmapd[]] = objd[];\
vars. push (evarmapd[]);}}});

s. linktrackvars = vars. join (&#39;,&#39;);\
s. linktrackevents = event;\
s. events = event;

console. log (&#39; linktrackvars: &#39;, s. linktrackvars);\
console. log (&#39; linktrackevents: &#39;, s. linktrackevents);\
console. log (&#39; events: &#39;, s. events);

s. tl ();}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* Fügt einen Analytics-Handler für alle Analyseereignisse von Livefyre hinzu. Für jedes Ereignis werden die Daten auf ein globales Objekt gesetzt und anschließend das Ereignis ausgelöst.

*/function
addanalyticshandler () {Livefyre.
analytics. addhandler (function (events) {(events || []). Foreach (function (data) {console.
log (&#39; Event handling: &#39;, data. type);
Tracklivefyreevent (data);});});});}

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

