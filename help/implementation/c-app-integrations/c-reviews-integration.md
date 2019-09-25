---
description: Ermöglichen Sie Kunden, Ihre Produktangebote zu bewerten und zu überprüfen.
seo-description: Ermöglichen Sie Kunden, Ihre Produktangebote zu bewerten und zu überprüfen.
seo-title: Reviews
solution: Experience Manager
title: Reviews
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Reviews {#reviews}

Ermöglichen Sie Kunden, Ihre Produktangebote zu bewerten und zu überprüfen.

Reviews ermöglichen es Mitgliedern Ihrer Community, Sternbewertungen und qualitative Rezensionen für jedes Produkt oder jede Dienstleistung beizutragen.

## Integration {#section_kk5_15b_c1b}

Gehen Sie zum Integrieren einer Reviews-App wie folgt vor, um eine Konversations-App zu integrieren. Siehe [Einbetten einer App](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Im Folgenden finden Sie ein Beispiel für eine eingebettete Reviews-App.

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

Wie im `CollectionMeta` Abschnitt "Erstellen"angegeben, `CollectionMeta` ist ein kodiertes JSON-Objekt. Im obigen Beispiel nimmt das JSON-Objekt das folgende Format vor, bevor es JWT-kodiert wird:

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

Wenn Sie den Abschnitt "Erste Schritte"bereits abgeschlossen haben, sollten Sie mit dem convConfig-Objekt vertraut sein. Um Reviews zu aktivieren, aktualisieren Sie convConfig mit den folgenden Feldern:

* **alwaysShowEditor** *optional* boolean: Standardmäßig wird der Überprüfungs-Editor nur angezeigt, wenn der Benutzer auf die Schaltfläche "Überprüfung schreiben"klickt. Setzen Sie diesen Parameter auf true, um den Editor immer anzuzeigen.

* **App** - *erforderliche* Zeichenfolge: Der App-Name, der für Reviews verwendet wird. Muss "Reviews" sein.

* **defaultSort** *optional* string: Ermöglicht die Auswahl der Standardsortierungsoption für Reviews. Mögliche Werte sind: mostHelpful, maximumRated, niedrigsteRated, neueste und älteste.

* **disableTitle** *optional* boolean: Deaktiviert und blendet das Titelfeld im Überprüfungseditor aus, was standardmäßig erforderlich und sichtbar ist. Der Standardwert ist "true".

* **enableHalfRating** *optional* boolean: Dient zum Aktivieren von Halbwerten im Standardauswahlmodul für Stern. Der Standardwert ist "true".

* **hideShowReviewButton** *optional* boolean: Steuert, ob die [!UICONTROL Show My Review] Schaltfläche angezeigt wird. Auf "true"setzen, damit Ihre Benutzer auswählen können, ob sie eigene Reviews anzeigen oder anzeigen möchten.

* **maxRating** *optional* integer Wird verwendet, um die Anzahl der Sterne festzulegen, die im Standard-Stern-Auswahlmodul angezeigt werden. Standardwert ist 5. Diese kann bis zu 100 konfiguriert werden.

* **ratingSummaryEnabled** *optional* boolean: Wird verwendet, um die Ansicht der Bewertungszusammenfassung über der Reviews-App anzuzeigen. Dies muss aktiviert sein, damit ratingSummaryDelegate verwendet werden kann. Der Standardwert ist "true".

## Sammlungsmetadaten überprüfen {#section_k1s_sqb_c1b}

* **** type: *erforderliche* Zeichenfolge: Definiert den Sammlungstyp. Muss `reviews`sein.

* **ratingDimensions** *optional* array: Ein Zeichenfolgen-Array für jeden Dimensionstyp, den diese Sammlung verwenden wird. Wenn dies nicht angegeben ist, ist nur 1 Dimension zulässig.

   Damit Benutzer Ihr Produkt z. B. nach "Design", "Funktionen"und "Leistung"bewerten können, setzen Sie das Array auf: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **ratingSubparts** *optional* integer: Anzahl der im Textfeld des Reviews anzuzeigenden Partitionen. Die Teilteilbezeichnungen werden mit dem Parameter wie unten dargestellt weitergegeben.

   >[!NOTE]
   >Sie müssen für jeden Unterabschnitt Bezeichnungen definieren.

* **ratingSubpartsIds** *optional* array: Ermöglicht Ihnen die Definition einer ID für jeden Unterteil in Ihrer Ratings-Sammlung, der verwendet werden kann, um diese Unterteilelemente in Ihrer CSS und JavaScript als Ziel festzulegen. Wenn Benutzer Reviews posten, `ratingSubpart` wird auf jedem das Attribut " `data-lf-subpart-id`"mit dieser ID gefüllt.

>[!NOTE]
>
>Zur Verwendung `ratingSubpartsIds`muss auch der `ratingSubparts` Parameter definiert werden und die Länge der beiden Arrays muss übereinstimmen.

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
>Wenn Sie `ratingDimensions`die Bewertungszusammenfassung verwenden, MÜSSEN Sie die `ratingSelectionDelegate`, `ratingDisplayDelegate`und verwenden `ratingSummaryDelegate` (wenn Sie die Bewertungszusammenfassung anzeigen möchten).

## Korrekturanpassung {#section_khz_xmb_c1b}

### Star-Bilder konfigurieren

Um das Bild für volle Sterne zu ändern, ist die Klasse `goog-ratings-star`. Ändern Sie das Hintergrundbild in das gewünschte Bild. Standardmäßig sind die Sterne 28 x 28 Pixel groß.

### Konfigurieren von Star-Bildern mit Half-Sternen

Mit halben Sternen gibt es zwei Klassen, eine für jede Seite des Sterns. Die linke Seite des Halbsterns ist `fyre-rating-half-odd` und die rechte Seite ist `fyre-rating-half-even`. Standardmäßig sind halbe Sterne 28 x 14 Pixel groß.

### QuickInfo-Werte für Sterne konfigurieren

Um die QuickInfo-Werte für die Sterne zu konfigurieren, folgen Sie dem unter Zeichenfolgenanpassung beschriebenen benutzerdefinierten Text. Verwenden Sie nach der Einrichtung den Schlüssel `ratingValues` und den Wert eines Arrays, das die QuickInfo-Zeichenfolgen enthält. Wenn Halbsterne deaktiviert sind, sollte die Anzahl der Elemente im Array mit der `maxRating` (oben) identisch sein. Wenn Halbsterne aktiviert sind, sollte die Anzahl der Elemente 2x `maxRating`betragen. Das erste Element im Array entspricht dem Element mit dem linken Stern (oder dem halben Stern) und fährt von links nach rechts fort.

### Die Option "Überprüfung anzeigen"aktivieren/deaktivieren

Um die [!UICONTROL Show My Review] Option ein- oder auszuschalten, wählen Sie den `hideShowReviewButton` Parameter in der App-Konfiguration aus.

### Texteditor standardmäßig anzeigen

Der Überprüfungs-Editor wird nur angezeigt, wenn der Benutzer auf die [!UICONTROL write review] Schaltfläche klickt. Um dieses Formular standardmäßig anzuzeigen, wählen Sie den `alwaysShowEditor` Parameter in der App-Konfiguration aus.
