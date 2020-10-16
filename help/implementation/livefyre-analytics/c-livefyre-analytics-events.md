---
description: 'null '
seo-description: 'null '
seo-title: Livefyre Analytics-Ereignis
solution: Experience Manager
title: Livefyre Analytics-Ereignis
uuid: 4eb5a196-ca33-40f8-a96d-ed46469223de
translation-type: tm+mt
source-git-commit: 5dc11c42a9f8bf3fa088f3245e21b6942d4865fe
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 4%

---


# Livefyre Analytics-Ereignis

## Ereignis-Objektdefinition {#section_dh1_yhn_pdb}

Der folgende Code definiert die Felder im Ereignis-Objekt, die vom Analytics-Handler auf einer Seite empfangen werden.

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

## Livefyre Analytics-Ereignis und eVars {#section_u3k_tft_mcb}

Die folgenden Livefyre-Ereignis zur Zuordnung zu benutzerdefinierten Ereignissen, die in Berichten mit dem Report Suite Manager verwendet werden sollen. Weitere Informationen zu Report Suites in Adobe Analytics finden Sie unter [Report Suite Manager](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html). Weitere Informationen zur Verwendung von Livefyre-Ereignissen mit Report Suite Manager finden Sie unter [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Livefyre Analytics-Ereignis

| Ereignis | Beschreibung |
|---|---|
| Init | Wenn eine Seite mit mindestens einer Livefyre-App geladen wird |
| Load | Jedes Mal, wenn eine App auf eine Seite geladen wurde, unabhängig von der Ansicht des Benutzers |
| Ansicht | Wenn eine App zum ersten Mal in den Viewport kam. |
| Posten | Jedes Mal, wenn ein Benutzer einen Kommentar oder einen Inhaltsbeitrag veröffentlicht, einschließlich z. B.: Top-Level-Beitrag, Antworten, Rezensionen, Media-Pinnwände-Uploads |
| Gepostet | Wenn ein Beitrag erfolgreich war. |
| Twitter_Antwort | Jedes Mal, wenn ein Benutzer auf Twitter antwortet |
| Twitter_like | Wo Inhalte freigegeben wurden für: Retweet |
| Livefyre_like | Jedes Mal, wenn die livefyre like-Funktion in einer App verwendet wird |
| Livefyre_Unlike | Jedes Mal, wenn ein Benutzer einen Lebenslauf wie |
| ShareOnPost | Immer wenn ein Benutzer Inhalte veröffentlicht und die Funktion &quot;Teilen auf Beitrag&quot;verwendet |
| ShareButtonClick | Jedes Mal, wenn ein Benutzer auf die Schaltfläche &quot;Freigeben&quot;für einen Kommentar klickt |
| ShareTwitter | Beim Klicken auf Auf Twitter teilen |
| ShareFacebook | Beim Klicken auf Auf Facebook teilen |
| ShareURL | Wenn &quot;Mit URL teilen&quot;ausgewählt/kopiert wird. |
| ExpandReplies | Wenn ein Benutzer auf den Link + oder Erweitern klickt, um alle Antworten auf einem Beitrag der obersten Ebene Ansicht |
| ReduzierenAntworten | Wenn ein Benutzer auf den Link - oder Reduzieren klickt, um alle Antworten auf einem Beitrag der obersten Ebene Ansicht |
| FlagClick | Jedes Mal, wenn ein Benutzer das Flag-Modul öffnet |
| FlagSpam | Wenn ein Benutzer Inhalte als Spam kennzeichnet |
| FlagDismatch | Wenn ein Benutzer Inhalte als nicht einverstanden kennzeichnet |
| FlagOffensive | Wenn ein Benutzer Inhalte als anstößig kennzeichnet |
| FlagOffTopic | Wenn ein Benutzer Inhalte als off-topic kennzeichnet |
| FlagCancel | Jedes Mal, wenn ein Benutzer beim Senden einer Flag auf &quot;X&quot;oder &quot;Abbrechen&quot;klickt |
| FollowCollection | Jedes Mal, wenn ein Gespräch verfolgt wird (&quot;Ich bin interessiert&quot; in Reviews) |
| UnfollowCollection | Wenn eine Konversation nicht verfolgt wird |
| RequestMore | Jedes Mal, wenn ein Benutzer mehr Inhalte in einer App geladen hat (auch bei hoher Geschwindigkeit) |
| ModalView | Jedes Mal, wenn ein Benutzer auf die Ansicht von Inhalten in einem Modal klickt |
| TwitterRetweetClick | Wo Inhalte freigegeben wurden für: Retweet |
| PostButtonClick | Wenn ein Benutzer auf den Beitrag klickt (&quot;Was ist Ihnen am Herzen?&quot;) button |
| Anmelden | Bei jeder Anmeldung eines Benutzers |
| Abmeldung | Bei jedem Abmelden eines Benutzers |

Im Folgenden finden Sie eine Liste von Konversionsvariablen (eVars), die Livefyre bereitstellt.

## Konversionsvariablen - eVars

| Ereignis | Beschreibung |
|--- |--- |
| Netzwerk-ID | Netzwerk-ID/Name in Livefyre |
| App-ID | Der URN der App |
| Kontext-ID | Inhalts-ID in Livefyre |
| App-Typ | Livefyre-App-Typ. Optionen: <br><ul><li>Live-Blog  </li><li> Funktionskarte</li><li>Karussell</li><li>Chat </li><li>Kommentare</li><li>Filmstreifen</li><li>Landkarte</li><li>Mosaik</li><li>Medienwall</li><li>Trends</li><li>Hochladen-Schaltfläche</li></ul> |
| Content-Typ | Instagram, Twitter, Facebook, LiveFyre, YouTube usw. |

## Mehr Info {#section_b3d_4yl_pdb}

Weitere Informationen zu den auf dieser Seite behandelten Themen finden Sie unter:

* [Report Suite](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)[ManagerDTM](https://docs.adobe.com/content/help/en/livefyre/using/apps/filmstrip/c-filmstrip-app.html)

* [Regeln](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)