---
description: Kunden können Ihre Produktangebote bewerten und überprüfen.
seo-description: Kunden können Ihre Produktangebote bewerten und überprüfen.
seo-title: Reviews
solution: Experience Manager
title: Reviews
uuid: b 740 ee 28-f 6 f 9-4 ae 7-9 fe 7-61 a 5 cde 97 bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Reviews {#reviews}

Kunden können Ihre Produktangebote bewerten und überprüfen.

Mithilfe von Reviews können Mitglieder Ihrer Community Bewertungssterne und Qualitätsprüfungen für beliebige Produkte oder Dienstleistungen durchführen.

## Integration{#section_kk5_15b_c1b}

Um eine Review-App zu integrieren, befolgen Sie das Verfahren zur Integration einer Konversation-App. Siehe [Einbetten einer App](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Im Folgenden finden Sie ein Beispiel für eine eingebettete Review-App.

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

Wie im Abschnitt "Erstellen `CollectionMeta` « `CollectionMeta` angegeben, ist ein kodiertes JSON-Objekt. Im obigen Beispiel akzeptiert das JSON-Objekt das folgende Format, bevor es JWT-kodiert ist:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## Convconfig-Objekt {#section_pzv_ytb_c1b}

Wenn Sie den Abschnitt Erste Schritte bereits abgeschlossen haben, sollten Sie mit dem contconfig-Objekt vertraut sein. Um Reviews zu aktivieren, aktualisieren Sie das contconfig mit den folgenden Feldern:

* **Alwaysshoweditor** *optionaler* boolescher Wert: Der Review-Editor wird standardmäßig erst angezeigt, wenn der Benutzer die Schaltfläche "Lesen" drückt. Legen Sie diesen Parameter auf true fest, um den Editor immer anzuzeigen.

* **App** *erforderliche* Zeichenfolge: Der für Überprüfungen zu verwendende App-Name. Muss "reviews" lauten.

* **Defaultsoptionale**** Zeichenfolge: Ermöglicht die Auswahl der Standardsortieroption für Reviews. Mögliche Werte sind: Momentarelpful, highestrated, lowestrated, newest und älteste.

* **Disabletitle** *optionaler* boolescher Wert: Deaktiviert und blendet das Titelfeld im Editor für Überprüfungen aus, das standardmäßig erforderlich und sichtbar ist. Der Standardwert ist "true" .

* **Enablehalfrating** *optionaler* Boolescher Wert: Wird verwendet, um die Hälfte am Standard-Star-Auswahlmodul zu aktivieren. Der Standardwert ist "true" .

* **Hideshowreviewbutton** *optionaler* boolescher Wert: Steuert, ob die [!UICONTROL Show My Review] Schaltfläche angezeigt wird. Legen Sie "true" fest, damit Ihre Benutzer auswählen können, ob ihre eigenen Überprüfungen angezeigt oder angezeigt werden sollen.

* **Optionale** ** integer-Ganzzahl Verwendet, um die Anzahl der Sterne festzulegen, die im Standard-Stern-Auswahlmodul angezeigt werden. Der Standardwert ist 5. Dies kann bis zu 100 konfiguriert werden.

* **Variabsummaryenable** *optionaler* boolescher Wert: Wird verwendet, um die Übersicht über die Bewertungszusammenfassung über der Übersichts-App anzuzeigen. Dies muss für die Verwendung der variabsummarydelegate aktiviert werden. Der Standardwert ist "true" .

## Überprüfungsmetadaten überprüfen {#section_k1s_sqb_c1b}

* **type:***erforderliche* Zeichenfolge: Definiert den Sammlungstyp. `reviews`Muss sein.

* **Variabdimensions** *optionales* Array: Ein Array von Zeichenfolgen für jeden Dimensionstyp, den diese Sammlung verwendet. Wenn dies nicht angegeben ist, wird nur 1 Dimension zugelassen.

   Damit beispielsweise Benutzer Ihr Produkt unter "Design" ," Funktionen" und "Leistung" bewerten können, legen Sie das Array auf: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **Variabsubparts** *optionale* Ganzzahl: Anzahl der im Textfeld der Überprüfung anzuzeigenden Partitionen. Die Unterteilbeschriftungen werden wie unten dargestellt mit dem Parameter weitergegeben.

   >[!NOTE]
   >Sie müssen Beschriftungen für jeden Teilabschnitt definieren.

* **Variabsubpartsids** *optionales* Array: Ermöglicht es Ihnen, eine ID für jeden Teilabschnitt in Ihrer Ratings-Sammlung zu definieren, der verwendet werden kann, um diese Unterteilelemente in Ihrem CSS und javascript abzuzielen. Wenn Benutzer Überprüfungen beisteuern, wird jeweils `ratingSubpart` das Attribut " `data-lf-subpart-id`«enthalten, das mit dieser ID ausgefüllt wird.

>[!NOTE]
>
>Zur Verwendung `ratingSubpartsIds`muss der `ratingSubparts` Parameter ebenfalls definiert werden und die Länge der beiden Arrays muss übereinstimmen.

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
>Wenn Sie verwenden `ratingDimensions`, müssen SIE DIE, `ratingSelectionDelegate``ratingDisplayDelegate`UND ( `ratingSummaryDelegate` wenn Sie die Bewertungszusammenfassung anzeigen möchten) verwenden.

## Reviews anpassen {#section_khz_xmb_c1b}

### Konfigurieren von Stern-Bildern

Um das Bild für vollständige Sterne zu ändern, lautet `goog-ratings-star`die Klasse. Ändern Sie das Hintergrundbild in das gewünschte Bild. Standardmäßig sind Sterne 28 x 28 Pixel.

### Konfigurieren von Stern-Bildern mit Halbsterne

Bei Halbwertern gibt es zwei Klassen, eine für jede Seite des Stern. Die linke Seite des halben Stern ist und `fyre-rating-half-odd``fyre-rating-half-even`die rechte Seite. Standardmäßig sind die Halbsterne 28 x 14 Pixel.

### Quickinfo-Werte für Sterne konfigurieren

Zum Konfigurieren der quickinfo-Werte für die Sterne folgen Sie dem in der Zeichenfolgenanpassung beschriebenen benutzerdefinierten Text. Sobald Sie diese Einstellung eingerichtet haben, verwenden Sie den Schlüssel `ratingValues` und den Wert ein Array, das die quickinfo-Zeichenfolgen enthält. Wenn Sie über die Hälfte Sterne deaktiviert haben, muss die Anzahl der Elemente im Array mit `maxRating` dem Wert (oben) übereinstimmen. Wenn Sie die Hälfte der Sterne aktiviert haben, sollte die Anzahl der Elemente 2 x `maxRating`betragen. Das erste Element im Array entspricht dem Sternchen (oder halber Stern) und fährt von links nach rechts fort.

### Option "Meine Überprüfung anzeigen" aktivieren/deaktivieren

Um die [!UICONTROL Show My Review] Option ein- oder auszuschalten, wählen Sie den `hideShowReviewButton` Parameter in der App-Konfiguration aus.

### Texteditor standardmäßig anzeigen

Der Review-Editor wird erst angezeigt, wenn der Benutzer die [!UICONTROL write review] Schaltfläche drückt. Um dieses Formular standardmäßig anzuzeigen, wählen Sie den `alwaysShowEditor` Parameter in der App-Konfiguration aus.
