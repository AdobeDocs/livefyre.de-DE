---
description: Verfolgen Sie Klicks von verweisender Stelle zurück zu Ihrer Seite.
seo-description: Verfolgen Sie Klicks von verweisender Stelle zurück zu Ihrer Seite.
seo-title: Verweisverfolgung
solution: Experience Manager
title: Verweisverfolgung
uuid: 5206 cc 16-9671-4 b 3 d-a 013-be 1 a 3 e 8 c 029 d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Verweisverfolgung{#referral-tracking}

Verfolgen Sie Klicks von verweisender Stelle zurück zu Ihrer Seite.

Livefyre hängt eine Verweisende Variable an die URL an, wenn ein Kommentar für ein soziales Netzwerk veröffentlicht oder freigegeben wird und für Permalinks in Livefyre-E-Emails verwendet wird. Verwenden Sie diese Variable, um den Referrer-Traffic von Livefyre-Apps auf Ihre sozialen oder eigenen Eigenschaften zu verfolgen.

Mit Livefyre-Apps können Sie Datenstreams nachverfolgen, die sich aus dem verweisenden Traffic ergeben, sodass Sie den Traffic Ihrer Site analysieren können.

## Tracking von Livefyre-Verweisenden Traffic {#section_nsy_qp4_xz}

Der Livefyre-Referrer-Traffic aus sozialen Netzwerken und E-Emails kann rückverfolgt werden, indem die Abfragezeichenfolgenparameter in den urls Ihrer Seiten überprüft und Code auf Ihrer Seite implementiert wird, um dies über Ihren Analyseanbieter zu verfolgen. Livefyre hängt einen Verweislink zu der URL an, wenn ein Kommentar für ein soziales Netzwerk veröffentlicht oder freigegeben wird und für Permalinks in Livefyre-E-Emails verwendet wird.

## Implementierungsbeispiel {#section_xvs_x44_xz}

Wenn der Traffic aus einer streamhub-basierten Benachrichtigung erfolgte, gibt es einen hubrefsrc-Abfragezeichenfolgenparameter mit einem Wert von E-Email, Facebook, Twitter, Linkedin oder Permalink. Der hubrefsrc-Parametername kann von Ihrem Livefyre-Bereitstellungsteam auf Netzwerkebene konfiguriert werden.

Zur Integration mit einer Analyse-Plattform muss Ihre Seite nach dem Laden des hubrefsrc suchen und den Traffic aufzeichnen, wenn er vorhanden ist.

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

* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Zielgruppen](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)