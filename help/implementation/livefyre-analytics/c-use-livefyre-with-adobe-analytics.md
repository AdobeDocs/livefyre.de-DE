---
description: 'null '
seo-description: 'null '
seo-title: Verwenden Sie Livefyre mit Adobe Analytics und Dynamischem Tag-Manager (DTM) lk xavvn vefyre mit Adobe Analytics und Dynamischer Tag-Manager (DTM)
uuid: 9a1c25c0-c474-46ff-82ac-e89357007c7f
translation-type: tm+mt
source-git-commit: 987482066f1ca3c021a5c9f0fc0109edff616c0a

---


# Verwenden von Livefyre mit Adobe Analytics und dem dynamischen Tag-Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Richten Sie Adobe Analytics und Dynamischer Tag-Manager (DTM) ein, um Daten für Livefyre-Apps zu erfassen.

## Schritt 1: Einrichten von Ereignissen in Adobe Analytics {#section_iks_kgd_4cb}

Ordnen Sie Livefyre-Ereignisse einem oder mehreren benutzerspezifischen Erfolgsereignissen in Adobe Analytics Report Suite Manager zu.

Weitere Informationen zum Report Suite Manager finden Sie unter [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html).

1. Melden Sie sich bei Adobe Analytics als Administrator-Benutzer an.
1. Öffnen Sie Adobe Analytics Admin Report Suite Manager.
1. Erstellen Sie eine neue Report Suite oder wählen Sie eine vorhandene.
1. Bearbeiten Sie die Report Suite, indem Sie auf die zu ändernde Report Suite klicken und dann zu **[!UICONTROL Edit Settings > Conversion > Success Events]** navigieren.
1. Ordnen Sie die Livefyre-Ereignisse einem oder mehreren benutzerspezifischen Erfolgsereignissen zu.

## Schritt 2: Konversionsvariablen einrichten

Ordnen Sie den Konversionsvariablen in Adobe Analytics Admin Report Suite Manager Livefyre-Konversionsvariablen (eVars) zu. Konversionsvariablen fungieren wie eine Sortierfunktion, um zu bestimmen, wie Daten aus Livefyre-Ereignissen identifiziert werden sollen.

1. Klicken Sie im Report Suite Manager auf **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Wählen Sie die zu verwendenden benutzerspezifischen Konversionsvariablen (eVars) und ordnen Sie sie den Livefyre-Konversionsvariablen zu. Zuordnen einer Livefyre-Konversionsvariablen zu einer benutzerspezifischen Konversionsvariablen
* Konversionsvariable aktivieren
* Benennen der Konversionsvariable
* Geben Sie der Konversionsvariablen einen Typ
1. Speichern Sie die benutzerdefinierten Konversionsvariablen.

## Schritt 3: Verwenden Sie DTM, um Ihre Report Suite mit Livefyre-Ereignissen hinzuzufügen {#section_t15_2hd_4cb}

Fügen Sie Adobe Analytics zu DTM hinzu, damit Analytics funktioniert. Erstellen Sie dazu eine neue Eigenschaft und ein neues Tool und fügen Sie der Eigenschaft die neue Report Suite mit Livefyre-Ereignissen hinzu. Weitere Informationen zu DTM finden Sie unter [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).

Sie müssen diesen Schritt nicht ausführen, wenn Sie bereits eine Eigenschaft oder ein Tool für die Report Suite eingerichtet haben, die Sie mit Livefyre-Ereignissen eingerichtet haben.

1. Erstellen oder bearbeiten Sie in DTM eine vorhandene Eigenschaft.
1. Erstellen oder bearbeiten Sie ein vorhandenes Adobe Analytics-Tool.
1. Wenn kein vorhandenes Adobe Analytics-Tool vorhanden ist, klicken Sie auf die **[!UICONTROL Add a Tool]** Schaltfläche.
Legen Sie die folgenden Parameter für das Tool fest:

   * Set **[!UICONTROL Tool Type]** to **[!UICONTROL Adobe Analytics]**.
   * Enable **[!UICONTROL Automatic Configuration]**.
   * Enable **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Fügen Sie dem **[!UICONTROL Report Suites]** Feld den Namen der Report Suite mit Livefyre-Ereignissen hinzu oder bestätigen Sie ihn.

## Schritt 4: Einrichten einer Seitenladeregel zur Einrichtung der Analytics-Handhabung {#section_jfj_j3d_4cb}

Richten Sie eine Seitenladeregel ein, um alle Daten einzuziehen. Die Seitenladeregel ermöglicht es Ihnen, benutzerdefiniertes JavaScript in die Regel einzufügen, die das Ereignis beim Laden der Seite aufzeichnet.

>[!NOTE]
>
>Verwenden Sie keine ereignisbasierten Regeln oder Direktaufrufregeln.

1. Wählen Sie in DTM die **[!UICONTROL Rules]** Registerkarte.
1. Klicken Sie auf **[!UICONTROL Page Load Rules]**.
1. Klicken Sie auf die **[!UICONTROL Create New Rule]** Schaltfläche.
1. Öffnen Sie den **[!UICONTROL Conditions]** Abschnitt, indem Sie auf die **[!UICONTROL Plus]** Schaltfläche klicken.
1. Regel auslösen. Wählen Sie **[!UICONTROL DOM Ready]** oder **[!UICONTROL Onload]** lösen Sie Auslösetypen aus, wenn Sie die Regel asynchron verschieben oder implementieren möchten.
1. (Optional) Fügen Sie zusätzliche Parameter hinzu, um die Seiten zu beschränken, auf denen Livefyre-Apps angezeigt werden. Weitere Informationen zu zusätzlichen Konfigurationsoptionen finden Sie unter [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html).
1. Klicken Sie unter **[!UICONTROL Javascript/ Third Party Tags]** auf die **[!UICONTROL Non-sequential]** Registerkarte und dann auf **[!UICONTROL Add New Script]**.
1. Wählen Sie **[!UICONTROL Sequential HTML]** als Skripttyp aus.
1. Fügen Sie das folgende Skript zum Code-Editor hinzu und klicken Sie auf **[!UICONTROL Save Code]**.

   Das folgende Skript ruft die Regel für den `livefyre_analytics` Direktaufruf auf, nachdem Livefyre JavaScript geladen wurde. Im folgenden Skriptbeispiel wird alle 400 ms überprüft, ob sich die Seite `livefyre.analytics` befindet. Nach dem Laden der Seite sendet livefyre.analytics Verfolgungsinformationen.

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

1. Klicken Sie auf **[!UICONTROL Save Code]**.
1. Klicken Sie auf **[!UICONTROL Save Rule]**.

## Schritt 5: Erstellen einer Direktaufrufregel zum Erstellen der Adobe Analytics-Zuordnungskonfiguration für Livefyre {#section_gvp_b1g_pdb}

Es gibt andere Möglichkeiten, Livefyre mit DTM zu implementieren, indem benutzerdefinierte Ereignisse, Adobe Analytics-UI-Felder in DTM und Datenelemente verwendet werden. Dieses Dokument verwendet benutzerdefiniertes JavaScript, um denselben Effekt zu erzielen.

1. Wählen Sie in DTM die Registerkarte **Regeln** und klicken Sie dann auf **Direktaufrufregeln**.
1. Click on the **Create New Rule** button.
1. Benennen Sie die neue Regel **Livefyre Analytics**.
1. Erweitern Sie den Konfigurationsbereich **Bedingungen** .
1. Geben Sie im Feld **String** die Zeichenfolge ein `livefyre_analytics`.
1. Erweitern Sie den Abschnitt Javascript-/Drittanbieter-Tag und klicken Sie auf die Schaltfläche Neues Skript **hinzufügen** .
1. Geben Sie **Livefyre Analytics Config** in das Eingabefeld **Tag-Name** ein.
1. Wählen Sie **Nicht-sequenzielles JavaScript**.
1. Geben Sie den folgenden Livefyre-Konfigurationscode in den Code-Editor ein und klicken Sie auf die Schaltfläche Code **speichern** .

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

   * Fügt einen Analytics-Handler für alle Analyseereignisse aus Livefyre hinzu. Für jedes Ereignis werden die Daten für ein globales Objekt festgelegt und dann das Ereignis ausgelöst.

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

1. Klicken Sie auf Regel **speichern**.

## Schritt 6: Änderungen für Seitenladeregel genehmigen {#section_pxc_11t_ycb}

1. Wechseln Sie zur **[!UICONTROL Approvals]** Registerkarte.
1. Klicken Sie auf **[!UICONTROL Approve]**.
1. Klicken Sie auf **[!UICONTROL Yes, approve]** , um Ihre Genehmigung zu bestätigen.
1. Gehe zu **[!UICONTROL Overview > Publish Queue]**.
1. Wählen Sie die zu veröffentlichende Regel aus.
1. Klicken Sie auf **[!UICONTROL Publish Selected]**.
1. Klicken Sie auf **[!UICONTROL Publish]** , um die Veröffentlichung zu bestätigen.

## Skript {#section_xkb_vft_mcb}

Der folgende Beispielcode ordnet die spezifischen eVars den verfügbaren Livefyre-eVars zu. Der Name der Livefyre-Konversionsvariablen ( `eVar`) (z. B. `appId`) wird dem Namen zugeordnet, den Sie im Report Suite Manager eingerichtet haben (z. B. `eVar81`). Ändern Sie die `eVar` Namen in diesem Skript in die benutzerdefinierten Konversionsvariablen.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

Der folgende Beispielcode ordnet die spezifischen Ereignisse, die Sie im Report Suite Manager einrichten, den verfügbaren Livefyre-Ereignissen zu. In diesem Beispiel `event82` wird ein Benutzerinteraktionsereignis eingerichtet, ohne zu unterscheiden, welches Benutzerinteraktionsereignis (z. B. "Gefällt mir"-Klicks oder das Freigeben von Inhalten). Auf diese Weise können Sie alle Benutzerinteraktionsdaten in einem Block effizient aufzeichnen. Sie können die Ereignisse in der Benutzeroberfläche von DTM Analytics auch mit Datenelementverweisen verknüpfen.

```
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
```

Im folgenden Beispiel wird angegeben, dass, wenn kein Ereignis in dieser Liste vorhanden ist, keine Aktionen durchgeführt werden. Sie müssen diesen Codeabschnitt nicht ändern.

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

Der folgende Code unterscheidet die `event82` aufgezeichneten Ereignistypen. Die Konversionsvariable, `eVar83` zeichnet den Typ der Benutzerinteraktion auf und das Skript legt fest, dass die Benutzerinteraktionsdaten nach Typ getrennt `eVar83` werden. So `eVar83` können Sie die aufgezeichneten Daten in bestimmte Arten von Benutzerinteraktionen unterteilen.

```
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
   
  console.log('linkTrackVars:', s.linkTrackVars);  
  console.log('linkTrackEvents:', s.linkTrackEvents);  
  console.log('events:', s.events); 
   
  s.tl(); 
}
```

Im folgenden Codebeispiel wird ein Handler hinzugefügt, der alle vorkommenden Ereignisse überwacht. Es verwendet die Seitenladeregel beim Laden, wartet darauf, dass Ereignisse vorhanden sind, und richtet dann einen Handler für alle Ereignisse aus der App ein und verfolgt sie. Sie müssen diesen Code nicht ändern.

```
/** 
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event. 
*/ 
function addAnalyticsHandler() { 
  Livefyre.analytics.addHandler(function (events) { 
    (events || []).forEach(function (data) { 
      console.log('Event handled:', data.type); 
      trackLivefyreEvent(data); 
    }); 
  }); 
}
```

## Mehr Info

Weitere Informationen zu den auf dieser Seite behandelten Themen finden Sie unter:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Regeln](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
