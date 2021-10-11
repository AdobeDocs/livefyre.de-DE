---
title: Livefyre-Analytics-Ereignisse
description: Livefyre-Analytics-Ereignisse
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
source-git-commit: 53aead87db517e6f68266a66115889509287a287
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# Livefyre-Analytics-Ereignisse

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

## Livefyre Analytics-Ereignisse und eVars {#section_u3k_tft_mcb}

Die folgenden Livefyre-Ereignisse werden benutzerdefinierten Ereignissen zugeordnet, die in Berichten mit dem Report Suite Manager verwendet werden. Weitere Informationen zu Report Suites in Adobe Analytics finden Sie unter [Report Suite Manager](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en). Weitere Informationen zur Verwendung von Livefyre-Ereignissen mit Report Suite Manager finden Sie unter [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Livefyre-Analytics-Ereignisse

| Ereignis | Beschreibung |
|---|---|
| Init | Wenn eine Seite geladen wird, die mindestens eine Livefyre-App enthält |
| Load | Jedes Mal, wenn eine App auf einer Seite geladen wurde, unabhängig von der Benutzeransicht |
| Ansicht | Wenn eine App zum ersten Mal in den Viewport gelangt ist. |
| Posten | Jedes Mal, wenn ein Benutzer einen Kommentar oder einen Inhalt veröffentlicht, einschließlich z. B.: Top-Level-Post, Antworten, Rezensionen, Medien-Pinnwände-Uploads |
| Gepostet | Wenn ein Beitrag erfolgreich war. |
| Twitter_Reply | Jedes Mal, wenn ein Benutzer auf Twitter antwortet |
| Twitter_like | Wo Inhalte für freigegeben wurden: Retweet |
| Livefyre_like | Jedes Mal, wenn die livefyre-like-Funktion in einer App verwendet wird |
| Livefyre_Unlike | Jedes Mal, wenn ein Benutzer eine &quot;livefyre&quot;-Einstellung wie |
| ShareOnPost | Jedes Mal, wenn ein Benutzer Inhalte veröffentlicht und die Funktion &quot;Auf Beitrag freigeben&quot;verwendet |
| ShareButtonClick | Jedes Mal, wenn ein Benutzer auf die Freigabe-Schaltfläche für einen Kommentar klickt |
| ShareTwitter | Wenn auf &quot;Mit Twitter teilen&quot;geklickt wird |
| ShareFacebook | Wenn auf &quot;Mit Facebook teilen&quot;geklickt wird |
| ShareURL | Wenn der Textbereich &quot;Mit URL teilen&quot;ausgewählt/kopiert wird. |
| ExpandReplies | Wenn ein Benutzer auf den Link + oder Erweitern klickt, um alle Antworten auf einem Beitrag der obersten Ebene anzuzeigen |
| CollapseReplies | Wenn ein Benutzer auf den Link - oder Reduzieren klickt, um alle Antworten auf einem Beitrag der obersten Ebene anzuzeigen |
| FlagClick | Jedes Mal, wenn ein Benutzer das Flag-Modal öffnet |
| FlagSpam | Wenn ein Benutzer Inhalte als Spam kennzeichnet |
| FlagDisagreb | Wenn ein Benutzer Inhalte als nicht einverstanden kennzeichnet |
| FlagOffensive | Wenn ein Benutzer Inhalte als anstößig markiert |
| FlagOffTopic | Wenn ein Benutzer Inhalte als Off-Thema markiert |
| FlagCancel | Jedes Mal, wenn ein Benutzer beim Senden einer Markierung auf X oder &quot;Abbrechen&quot;klickt |
| FollowCollection | Jedes Mal, wenn ein Gespräch verfolgt wird (&quot;Ich bin interessiert&quot; in Reviews) |
| UnfollowCollection | Wenn eine Konversation nicht verfolgt wird |
| RequestMore | Jedes Mal, wenn ein Benutzer mehr Inhalt in eine App geladen hat (auch bei hoher Geschwindigkeit erforderlich) |
| ModalView | Jedes Mal, wenn ein Benutzer klickt, um Inhalte in einem Modal anzuzeigen |
| TwitterRetweetClick | Wo Inhalte für freigegeben wurden: Retweet |
| PostButtonClick | Wenn ein Benutzer auf den Beitrag klickt (&quot;Was ist für Sie von Bedeutung?&quot;) button |
| Anmelden | Jedes Mal, wenn sich ein Benutzer anmeldet |
| Abmeldung | Jedes Mal, wenn sich ein Benutzer abmeldet |

Im Folgenden finden Sie eine Liste der Konversionsvariablen (eVars), die Livefyre bereitstellt.

## Konversionsvariablen - eVars

| Ereignis | Beschreibung |
|--- |--- |
| Netzwerkkennung | Netzwerk-ID/Name in Livefyre |
| App-ID | Die URN der App |
| Kontext-ID | Inhalts-ID in Livefyre |
| App-Typ | Livefyre-App-Typ. Optionen: <br><ul><li>Live-Blog  </li><li> Funktionskarte</li><li>Karussell</li><li>Chat </li><li>Kommentare</li><li>Filmstreifen</li><li>Landkarte</li><li>Mosaik</li><li>Media Wall</li><li>Trends</li><li>Hochladen-Schaltfläche</li></ul> |
| Content-Typ | Instagram, Twitter, Facebook, LiveFyre, YouTube usw. |

## Mehr Info {#section_b3d_4yl_pdb}

Weitere Informationen zu den auf dieser Seite behandelten Themen finden Sie unter:

* [Report Suite ](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)[ManagerDTM](https://experienceleague.adobe.com/docs/livefyre/using/apps/filmstrip/c-filmstrip-app.html?lang=en)

* [Regeln](https://experienceleague.adobe.com/docs/dtm/using/resources/rules/create-rules.html?lang=en)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
