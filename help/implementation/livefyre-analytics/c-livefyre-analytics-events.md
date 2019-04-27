---
description: 'null '
seo-description: 'null '
seo-title: Livefyre-Analytics-Ereignisse
solution: Experience Manager
title: Livefyre-Analytics-Ereignisse
uuid: 4 eb 5 a 196-ca 33-40 f 8-a 96 d-ed 46469223 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre-Analytics-Ereignisse {#livefyre-analytics-events}

## Ereignisobjektdefinition {#section_dh1_yhn_pdb}

Der folgende Code definiert die Felder im Ereignisobjekt, die vom Analytics-Handler auf einer Seite empfangen werden.

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Livefyre-Analytics-Ereignisse und -evars {#section_u3k_tft_mcb}

Die folgenden Livefyre-Ereignisse, die benutzerspezifischen Ereignissen zugeordnet werden sollen, die in Berichten mithilfe des Report Suite Manager verwendet werden sollen. Weitere Informationen zu Report Suites in Adobe Analytics finden Sie unter [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html). Weitere Informationen zur Verwendung von Livefyre-Ereignissen mit Report Suite Manager [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)finden Sie unter.

## Livefyre-Analytics-Ereignisse

| Ereignis | Beschreibung |
|---|---|
| Init | Wenn eine Seite mit mindestens einer Livefyre-App geladen wird |
| Laden | Immer wenn eine App auf einer Seite geladen wurde, unabhängig von der Benutzeransicht |
| Ansicht | Wenn eine App zum ersten Mal in den Viewport eingegeben wurde. |
| Beitrag | Jedes Mal, wenn ein Benutzer einen Kommentar oder einen Inhaltsbereich mitteilt, einschließlich ex: Beitrag auf oberster Ebene, Antworten, Überprüfungen, Medien-Pinnwände |
| Gepostet | Wenn ein Beitrag abgesendet wurde. |
| Twitter_ Reply | Jedes Mal, wenn ein Benutzer auf Twitter antwortet |
| Twitter_ Gefällt mir | Bei Freigabe von Inhalten an: Retweet |
| Livefyre_ Like | Immer wenn die Funktion &quot;livefyre&quot; in einer App verwendet wird |
| Livefyre_ Unlike | Jedes Mal, wenn ein Benutzer einen Livefyre aufhebt wie |
| Shareonpost | Jedes Mal, wenn ein Benutzer Inhalte veröffentlicht und die Freigabe auf Beitragsfunktion verwendet |
| Sharebuttonclick | Jedes Mal, wenn ein Benutzer auf die Schaltfläche &quot;Freigeben&quot; in einem Kommentar klickt |
| Sharetwitter | Wenn auf Twitter freigeben geklickt wird |
| Sharefacebook | Wenn auf Facebook freigeben geklickt wird |
| Shareurl | Wenn der Textbereich &quot;Auf URL teilen&quot; aktiviert/kopiert ist. |
| Expandanswers | Wenn ein Benutzer auf den Link + oder Erweitern klickt, um alle Antworten auf einem Top-Level-Beitrag anzuzeigen |
| Collapsereplies | Wenn ein Benutzer auf den Link &quot; - oder reduzieren&quot; klickt, um alle Antworten auf einem Beitrag auf oberster Ebene anzuzeigen |
| Flagclick | Jedes Mal, wenn ein Benutzer das Flag &quot;Flag&quot; öffnet |
| Flagspam | Wenn ein Benutzer Inhalte als Spam kennzeichnet |
| Flagdisagree | Wenn ein Benutzer Inhalte als nicht zustimmen kennzeichnet |
| Flagpress | Wenn ein Benutzer Inhalte als beleidigend kennzeichnet |
| Flagofftopic | Ein Benutzer kennzeichnet den Inhalt als aus dem Thema heraus |
| Flagcancel | Jedes Mal, wenn ein Benutzer beim Senden einer Markierung auf &quot;X&quot; oder&quot; Abbrechen&quot; klickt |
| Followcollection | Jedes Mal, wenn eine Unterhaltung folgt (&quot;Ich bin interessiert&quot; in Reviews) |
| Unfollowcollection | Wenn eine Unterhaltung nicht befolgt wird |
| Requestmore | Jedes Mal, wenn ein Benutzer mehr Inhalte in einer App geladen hat (muss auch für hohe Geschwindigkeit sein) |
| Modalview | Jedes Mal, wenn ein Benutzer klickt, um Inhalte in einem Modal anzuzeigen |
| Twitterretweetclick | Bei Freigabe von Inhalten an: Retweet |
| Postbuttonclick | Wenn ein Benutzer auf den Beitrag klickt (&quot;Gefällt mir? &quot;) Schaltfläche |
| Anmeldung | Jedes Mal, wenn sich ein Benutzer angemeldet hat |
| Abmelden | Bei jeder Abmeldung eines Benutzers |

Im Folgenden finden Sie eine Liste der Konversionsvariablen (evars), die von Livefyre bereitgestellt werden.

## Konversionsvariablen - evars

| Ereignis | Beschreibung |
|--- |--- |
| Netzwerk-ID | Netzwerk-ID/Name in Livefyre |
| App-ID | URN der App |
| Kontext-ID | Inhalts-ID in Livefyre |
| App-Typ | Livefyre-App-Typ. Optionen: <br><ul><li>Live-Blog  </li><li> Feature Card</li><li>Karussell</li><li>Chat </li><li>Kommentare</li><li>Filmstreifen</li><li>Map</li><li>Mosaik</li><li>Medienpinnwand</li><li>Trends</li><li>Hochladen-Schaltfläche</li></ul> |
| Inhaltstyp | Instagram, Twitter, Facebook, livefyre, youtube usw. |

## Mehr Info {#section_b3d_4yl_pdb}

Weitere Informationen zu den auf dieser Seite behandelten Themen finden Sie unter:

* [Report Suite managerdtm](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [Regeln](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre. js](/help/implementation/c-livefyre.js.md)