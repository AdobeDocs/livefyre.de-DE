---
description: Ermöglichen Sie Kunden, Ihre Produktangebote zu bewerten und zu überprüfen.
title: Reviews
exl-id: 2f10646e-59c4-459c-ae1b-749f951a06d2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Reviews {#reviews}

Ermöglichen Sie Kunden, Ihre Produktangebote zu bewerten und zu überprüfen.

Reviews ermöglichen es Mitgliedern Ihrer Community, Sternbewertungen und qualitative Rezensionen für jedes Produkt oder jede Dienstleistung beizutragen.

## Integration {#section_kk5_15b_c1b}

Gehen Sie zum Integrieren einer Reviews-App wie folgt vor, um eine Konversations-App zu integrieren. Siehe [Eine App](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md) einbetten. Im Folgenden finden Sie ein Beispiel für eine eingebettete Reviews-App.

### Beispiel 

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

Wie im Abschnitt Erstellen `CollectionMeta` angegeben, ist `CollectionMeta` ein kodiertes JSON-Objekt. Im obigen Beispiel nimmt das JSON-Objekt das folgende Format vor, bevor es JWT-kodiert wird:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## convConfig-Objekt {#section_pzv_ytb_c1b}

Wenn Sie den Abschnitt &quot;Erste Schritte&quot;bereits abgeschlossen haben, sollten Sie mit dem convConfig-Objekt vertraut sein. Um Reviews zu aktivieren, aktualisieren Sie convConfig mit den folgenden Feldern:

* **** ** alwaysShowEditoroptionalboolean: Standardmäßig wird der Überprüfungs-Editor nur angezeigt, wenn der Benutzer auf die Schaltfläche &quot;Überprüfung schreiben&quot;klickt. Setzen Sie diesen Parameter auf &quot;true&quot;, um den Editor immer anzuzeigen.

* **apprequirements-** ** Zeichenfolge: Der App-Name, der für Reviews verwendet wird. Muss &quot;Reviews&quot; sein.

* **defaultSortoptionalstring:** **  Ermöglicht die Auswahl der Standardsortierungsoption für Reviews. Mögliche Werte sind: mostHelpful, maximumRated, niedrigsteRated, neueste und älteste.

* **** ** disableTitleoptionalboolean: Deaktiviert und blendet das Titelfeld im Überprüfungs-Editor aus, was standardmäßig erforderlich und sichtbar ist. Der Standardwert ist &quot;true&quot;.

* **** ** enableHalfRating optionalboolean: Dient zum Aktivieren von Halbwerten im Standardauswahlmodul für Stern. Der Standardwert ist &quot;true&quot;.

* **** ** hideShowReviewButtonoptionalboolean: Steuert, ob die  [!UICONTROL Show My Review] Schaltfläche angezeigt wird. Auf &quot;true&quot;setzen, damit Ihre Benutzer auswählen können, ob sie eigene Reviews anzeigen oder anzeigen möchten.

* **** ** maxRating optionalinteger Wird verwendet, um die Anzahl der Sterne festzulegen, die im Standard-Stern-Auswahlmodul angezeigt werden. Standardwert ist 5. Diese kann bis zu 100 konfiguriert werden.

* **** ** ratingSummaryEnabledoptionalboolean: Wird verwendet, um die Ansicht der Bewertungszusammenfassung über der Reviews-App anzuzeigen. Dies muss aktiviert sein, damit ratingSummaryDelegate verwendet werden kann. Der Standardwert ist &quot;true&quot;.

## Sammlungsmetadaten {#section_k1s_sqb_c1b} überprüfen

* **type:** ** required string: Definiert den Sammlungstyp. Muss `reviews` sein.

* **Optionales** ** RatingDimensions-Array: Ein Zeichenfolgen-Array für jeden Dimensionstyp, den diese Sammlung verwenden wird. Wenn dies nicht angegeben wird, ist nur 1 Dimension zulässig.

   Damit Benutzer Ihr Produkt z. B. nach &quot;Design&quot;, &quot;Funktionen&quot;und &quot;Leistung&quot;bewerten können, setzen Sie das Array auf: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** ratingSubpartsoptionalinteger: Anzahl der im Textfeld des Reviews anzuzeigenden Partitionen. Die Teilteilbezeichnungen werden mit dem Parameter wie unten dargestellt weitergegeben.

   >[!NOTE]
   >Sie müssen für jeden Unterabschnitt Bezeichnungen definieren.

* **ratingSubpartsIdsoptionalarray:** **  Ermöglicht Ihnen die Definition einer ID für jeden Unterteil in Ihrer Ratings-Sammlung, die zur Zielgruppe dieser Unterteilelemente in Ihrer CSS und JavaScript verwendet werden kann. Wenn Benutzer Reviews posten, enthält jedes `ratingSubpart` das Attribut &quot;`data-lf-subpart-id`&quot;mit dieser ID.

>[!NOTE]
>
>Um `ratingSubpartsIds` verwenden zu können, muss auch der Parameter `ratingSubparts` definiert werden und die Länge der beiden Arrays muss übereinstimmen.

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>Wenn Sie `ratingDimensions` verwenden, MÜSSEN Sie `ratingSelectionDelegate`, `ratingDisplayDelegate` und `ratingSummaryDelegate` verwenden (wenn Sie die Bewertungszusammenfassung anzeigen möchten).

## Reviews Customization {#section_khz_xmb_c1b}

### Star-Bilder konfigurieren

Um das Bild für volle Sterne zu ändern, ist die Klasse `goog-ratings-star`. Ändern Sie das Hintergrundbild in das gewünschte Bild. Standardmäßig sind die Sterne 28 x 28 Pixel groß.

### Konfigurieren von Star-Bildern mit Half-Sternen

Mit halben Sternen gibt es zwei Klassen, eine für jede Seite des Sterns. Die linke Seite des Halbsterns ist `fyre-rating-half-odd` und die rechte Seite ist `fyre-rating-half-even`. Standardmäßig sind halbe Sterne 28 x 14 Pixel groß.

### QuickInfo-Werte für Sterne konfigurieren

Um die QuickInfo-Werte für die Sterne zu konfigurieren, folgen Sie dem unter Zeichenfolgenanpassung beschriebenen benutzerdefinierten Text. Verwenden Sie nach der Einrichtung den Schlüssel `ratingValues` und den Wert eines Arrays, das die QuickInfo-Zeichenfolgen enthält. Wenn Halbsterne deaktiviert sind, sollte die Anzahl der Elemente im Array mit `maxRating` (oben) identisch sein. Wenn Sie Halbsterne aktiviert haben, sollte die Anzahl der Elemente 2x `maxRating` betragen. Das erste Element im Array entspricht dem Element mit dem linken Stern (oder dem halben Stern) und fährt von links nach rechts fort.

### Die Option &quot;Überprüfung anzeigen&quot;aktivieren/deaktivieren

Um die Option [!UICONTROL Show My Review] ein- oder auszuschalten, müssen Sie den Parameter `hideShowReviewButton` in der App-Konfiguration Zielgruppe haben.

### Texteditor standardmäßig anzeigen

Der Überprüfungs-Editor wird nur angezeigt, wenn der Benutzer die Schaltfläche [!UICONTROL write review] drückt. Zielgruppe des Parameters `alwaysShowEditor` in der App-Konfiguration, um dieses Formular standardmäßig anzuzeigen.
