---
description: Verfolgen Sie Klicks vom Verweisverkehr zurück zu Ihrer Seite.
seo-description: Verfolgen Sie Klicks vom Verweisverkehr zurück zu Ihrer Seite.
seo-title: Verweisverfolgung
solution: Experience Manager
title: Verweisverfolgung
uuid: 7daf615d-0c07-49d1-adb2-1ac67ea563e7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# Verweisverfolgung{#referral-tracking}

Verfolgen Sie Klicks vom Verweisverkehr zurück zu Ihrer Seite.

Livefyre hängt eine Verweisvariable an die URL an, wenn ein Kommentar veröffentlicht oder in einem sozialen Netzwerk freigegeben wird, sowie für Permalinks, die in Livefyre-E-Mails enthalten sind. Verwenden Sie diese Variable, um den Verweistraffic von Livefyre-Apps auf Ihre sozialen oder eigenen Eigenschaften zu verfolgen.

Mit Livefyre-Apps können Sie Datenströme verfolgen, die aus dem Verweistraffic resultieren, und so den Traffic Ihrer Site analysieren.

## Verfolgen des Livefyre-Verweisdatenverkehrs {#section_nsy_qp4_xz}

Livefyre-Verweisverkehr aus sozialen Netzwerken und E-Mails kann verfolgt werden, indem die Seitenzeichenfolgenparameter in den URLs Ihrer Abfragen überprüft und Code auf Ihrer Seite implementiert werden, um dies über Ihren Analytics-Provider zu verfolgen. Livefyre fügt einen Verweislink an die URL an, wenn ein Kommentar veröffentlicht oder in einem sozialen Netzwerk freigegeben wird, und für Permalinks, die in Livefyre-E-Mails enthalten sind.

## Implementierungsbeispiel {#section_xvs_x44_xz}

Wenn der Traffic aus einer StreamHub-basierten Benachrichtigung stammt, gibt es einen String-Parameter für die HubRefSrc-Abfrage mit dem Wert &quot;email&quot;, &quot;facebook&quot;, &quot;twitter&quot;, &quot;linkedin&quot;oder &quot;permalink&quot;. Der Parametername &quot;ubRefSrc&quot;kann auf Netzwerkebene von Ihrem Livefyre-Versand-Team konfiguriert werden.

Zur Integration in eine Analytics-Plattform muss Ihre Seite beim Laden nach dem &quot;HubRefSrc&quot;suchen und den Traffic aufzeichnen, wenn dieser vorhanden ist.

Beispiel:

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```



Apps, die diese Funktion verwenden:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reviews](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sir](../c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)

