---
description: Richten Sie Adobe Analytics und den Dynamic Tag Manager (DTM) ein, um Daten für Livefyre-Apps zu erfassen.
title: Verwenden von Livefyre mit Adobe Analytics und Dynamic Tag Manager (DTM)
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
source-git-commit: cbe23e8c253f1531418f18424e180d1adc16e426
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 1%

---

# Verwenden von Livefyre mit Adobe Analytics und Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Richten Sie Adobe Analytics und den Dynamic Tag Manager (DTM) ein, um Daten für Livefyre-Apps zu erfassen.

## Schritt 1: Einrichten von Ereignissen in Adobe Analytics {#section_iks_kgd_4cb}

Ordnen Sie Livefyre-Ereignisse einem oder mehreren benutzerdefinierten Erfolgsereignissen in Adobe Analytics Report Suite Manager zu.

Weitere Informationen zu Report Suite Manager finden Sie unter [Report Suite Manager](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html).

1. Melden Sie sich bei Adobe Analytics als Administrator-Benutzer an.
1. Öffnen Sie Adobe Analytics Admin Report Suite Manager.
1. Erstellen Sie eine neue Report Suite oder wählen Sie eine vorhandene aus.
1. Bearbeiten Sie die Report Suite, indem Sie auf die zu ändernde Report Suite klicken, und navigieren Sie dann zu **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Ordnen Sie die Livefyre-Ereignisse einem oder mehreren benutzerspezifischen Erfolgsereignissen zu.

## Schritt 2: Einrichten von Konversionsvariablen

Ordnen Sie die Livefyre-Konversionsvariablen (eVars) den Konversionsvariablen in Adobe Analytics Admin Report Suite Manager zu. Konversionsvariablen funktionieren wie Sortierfunktionen, um zu bestimmen, wie Sie aus Livefyre-Ereignissen erfasste Daten identifizieren möchten.

1. Klicken Sie im Report Suite Manager auf **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**.
1. Wählen Sie die zu verwendenden benutzerspezifischen Konversionsvariablen (eVars) aus und ordnen Sie sie den Livefyre-Konversionsvariablen zu. So ordnen Sie eine Livefyre-Konversionsvariable einer benutzerdefinierten Konversionsvariablen zu:
* Konversionsvariable aktivieren
* Benennen Sie die Konversionsvariable.
* Konversionsvariable einen Typ geben
1. Speichern Sie die benutzerdefinierten Konversionsvariablen.

## Schritt 3: Verwenden von DTM zum Hinzufügen Ihrer Report Suite zu Livefyre-Ereignissen {#section_t15_2hd_4cb}

Fügen Sie Adobe Analytics zu DTM hinzu, damit Analytics funktioniert. Erstellen Sie dazu eine neue Eigenschaft und ein neues Tool und fügen Sie die neue Report Suite mit Livefyre-Ereignissen zur Eigenschaft hinzu. Weitere Informationen zu DTM finden Sie unter [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).

Sie müssen diesen Schritt nicht ausführen, wenn Sie bereits eine Eigenschaft oder ein Tool für die Report Suite eingerichtet haben, die Sie mit Livefyre-Ereignissen eingerichtet haben.

1. Erstellen oder bearbeiten Sie in DTM eine vorhandene Eigenschaft.
1. Erstellen oder bearbeiten Sie ein vorhandenes Adobe Analytics-Tool.
1. Wenn kein vorhandenes Adobe Analytics-Tool vorhanden ist, klicken Sie auf die Schaltfläche **[!UICONTROL Add a Tool]** .
Legen Sie die folgenden Parameter für das Tool fest:

   * Setzen Sie **[!UICONTROL Tool Type]** auf **[!UICONTROL Adobe Analytics]**.
   * Aktivieren **[!UICONTROL Automatic Configuration]**.
   * Aktivieren **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Fügen Sie dem Feld **[!UICONTROL Report Suites]** den Namen der Report Suite mit Livefyre-Ereignissen hinzu oder bestätigen Sie ihn.

## Schritt 4: Einrichten einer Seitenladeregel zum Einrichten der Analytics-Verarbeitung {#section_jfj_j3d_4cb}

Richten Sie eine Seitenladeregel ein, um alle Daten abzurufen. Mit der Seitenladeregel können Sie benutzerdefiniertes JavaScript in die Regel einfügen, die das Ereignis beim Laden der Seite aufzeichnet.

>[!NOTE]
>
>Verwenden Sie keine ereignisbasierten Regeln oder Direktaufrufregeln.

1. Wählen Sie in DTM die Registerkarte **[!UICONTROL Rules]** aus.
1. Klicken **[!UICONTROL Page Load Rules]**.
1. Klicken Sie auf die Schaltfläche **[!UICONTROL Create New Rule]** .
1. Öffnen Sie den Abschnitt **[!UICONTROL Conditions]** , indem Sie auf die Schaltfläche **[!UICONTROL Plus]** klicken.
1. Trigger der Regel. Wählen Sie die Typen **[!UICONTROL DOM Ready]** oder **[!UICONTROL Onload]** für Trigger aus, wenn Sie die Regel asynchron verzögern oder implementieren möchten.
1. (Optional) Fügen Sie zusätzliche Parameter hinzu, um die Seiten zu beschränken, auf denen Livefyre-Apps angezeigt werden. Weitere Informationen zu zusätzlichen Konfigurationsoptionen finden Sie unter [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html).
1. Klicken Sie unter **[!UICONTROL Javascript/ Third Party Tags]** auf die Registerkarte **[!UICONTROL Non-sequential]** und klicken Sie dann auf **[!UICONTROL Add New Script]**.
1. Wählen Sie **[!UICONTROL Sequential HTML]** als Skripttyp aus.
1. Fügen Sie das folgende Skript zum Code-Editor hinzu und klicken Sie auf **[!UICONTROL Save Code]**.

   Das folgende Skript ruft die Direktaufrufregel `livefyre_analytics` auf, nachdem das Livefyre-JavaScript geladen wurde. Im folgenden Skriptbeispiel wird alle 400 ms überprüft, ob `livefyre.analytics` auf der Seite angezeigt wird. Nachdem die Seite geladen wurde, sendet livefyre.analytics Tracking-Informationen.

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

1. Klicken **[!UICONTROL Save Code]**.
1. Klicken **[!UICONTROL Save Rule]**.

## Schritt 5: Erstellen einer Direktaufrufregel zum Erstellen der Adobe Analytics-Zuordnungskonfiguration für Livefyre {#section_gvp_b1g_pdb}

Es gibt andere Möglichkeiten, Livefyre mithilfe von benutzerdefinierten Ereignissen, Adobe Analytics-UI-Feldern in DTM und Datenelementen in DTM zu implementieren. In diesem Dokument wird benutzerdefiniertes JavaScript verwendet, um denselben Effekt zu erzielen.

1. Wählen Sie in DTM die Registerkarte **Regeln** und klicken Sie dann auf **Regeln für Direktaufrufe**.
1. Klicken Sie auf die Schaltfläche **Neue Regel erstellen** .
1. Nennen Sie die neue Regel **Livefyre Analytics**.
1. Erweitern Sie den Konfigurationsbereich **Bedingungen** .
1. Geben Sie im Feld **String** `livefyre_analytics` ein.
1. Erweitern Sie den Abschnitt JavaScript/Drittanbieter-Tag und klicken Sie auf die Schaltfläche **Neues Skript hinzufügen** .
1. Geben Sie **Livefyre Analytics-Konfiguration** in das Eingabefeld **Tag-Name** ein.
1. Wählen Sie **Nicht sequenzielles JavaScript** aus.
1. Geben Sie den folgenden Livefyre-Konfigurationscode in den Code-Editor ein und klicken Sie auf die Schaltfläche **Code speichern**.

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

   * Fügt einen Analytics-Handler für alle Analytics-Ereignisse von Livefyre hinzu. Für jedes Ereignis legt es die Daten für ein globales Objekt fest und sendet dann das Ereignis.

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

1. Klicken Sie auf **Regel speichern**.

## Schritt 6: Genehmigen von Änderungen für die Seitenladeregel {#section_pxc_11t_ycb}

1. Gehen Sie zur Registerkarte **[!UICONTROL Approvals]** .
1. Klicken **[!UICONTROL Approve]**.
1. Klicken Sie auf **[!UICONTROL Yes, approve]**, um Ihre Genehmigung zu bestätigen.
1. Gehe zu **[!UICONTROL Overview > Publish Queue]**.
1. Wählen Sie die zu veröffentlichende Regel aus.
1. Klicken **[!UICONTROL Publish Selected]**.
1. Klicken Sie auf **[!UICONTROL Publish]** , um zu bestätigen, dass Sie veröffentlichen möchten.

## Skript {#section_xkb_vft_mcb}

Der folgende Beispielcode ordnet die spezifischen eVars den verfügbaren Livefyre-eVars zu. Der Name der Livefyre-Konversionsvariablen ( `eVar`) (z. B. `appId`) wird dem Namen zugeordnet, den Sie im Report Suite Manager eingerichtet haben (z. B. `eVar81`). Ändern Sie die `eVar`-Namen in diesem Skript in die benutzerdefinierten Konversionsvariablen.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

Der folgende Beispielcode ordnet die spezifischen Ereignisse, die Sie im Report Suite Manager einrichten, den verfügbaren Livefyre-Ereignissen zu. In diesem Beispiel wird `event82` als jedes Benutzerinteraktionsereignis eingerichtet, ohne zu unterscheiden, welche Art von Benutzerinteraktionsereignis (z. B. &quot;Gefällt mir&quot;-Klicks oder das Teilen von Inhalten) ausgelöst wird. Dies ist eine effiziente Methode, alle Benutzerinteraktionsinformationen in einem Block aufzuzeichnen. Sie können die Ereignisse in der DTM Analytics-Benutzeroberfläche auch mit Datenelementverweisen verknüpfen.

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

Im folgenden Beispiel wird angegeben, dass, wenn kein Ereignis in dieser Liste vorhanden ist, keine Aktionen ausgeführt werden. Sie müssen diesen Codeabschnitt nicht ändern.

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

Der folgende Code unterscheidet die Ereignistypen, die `event82` aufzeichnet. Die Konversionsvariable `eVar83` zeichnet den Typ der Benutzerinteraktion auf und das Skript richtet `eVar83` ein, um die Benutzerinteraktionsdaten nach Typ zu trennen. `eVar83` ermöglicht es Ihnen also, die aufgezeichneten Daten in bestimmte Arten von Benutzerinteraktionen zu unterteilen.

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

Im folgenden Codebeispiel wird ein -Handler hinzugefügt, der alle auftretenden Ereignisse überwacht. Dabei wird die Seitenladeregel beim Laden verwendet, auf das Vorhandensein von Ereignissen gewartet, dann der Handler für alle Ereignisse aus der App eingerichtet und verfolgt. Sie müssen diesen Code nicht ändern.

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

* [Report Suite Manager](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)
* [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)
* [Regeln](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
