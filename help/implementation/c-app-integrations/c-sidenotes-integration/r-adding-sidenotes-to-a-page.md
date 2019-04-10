---
description: null
seo-description: null
seo-title: Hinzufügen von Zielgruppen zu einer Seite
solution: Experience Manager
title: Hinzufügen von Zielgruppen zu einer Seite
uuid: 6499 c 45 a -3773-4 adb-a 6 c 7-22 a 628309 afd
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Hinzufügen von Zielgruppen zu einer Seite {#adding-sidenotes-to-a-page}

Livefyre bietet verschiedene Konfigurationsoptionen für die Positionierung von Sidenotes auf Ihrer Seite:

* Die Option Selektoren definiert die Elemente, auf denen die Autoren erscheinen sollten.
* Anker stellen Elemente dar, die autorisiert werden können.
* Mit dem benutzerdefinierten Thread-Behälter können Sie festlegen, wo der Thread-Thread im Verhältnis zu den gezählten Inhalten platziert werden soll.
* Mit der Option "Sidenotes" können Sie die Anzahl der am angegebenen Ort hinzugefügten Autoren anzeigen.
* Verwenden Sie mehrere `ConvConfig` Objekte, um mehreren Meldungen auf einer einzigen Seite Zielgruppen hinzuzufügen.

## Selektoren {#section_wyj_4sv_sy}

Mit der Option Selektoren können Autoren Inhalte auf der Seite suchen. Mit dem Wert für diese Option können Sie die verwendeten Elemente dynamisch bestimmen. Es kann sich um eine Auswahlzeichenfolge (z. B. " # content p, # content img" ), ein jquery-Objekt (z. `$(‘#content’)`B.), ein Array von DOM-Elementen oder ein Objekt mit zwei Eigenschaften handeln: einbeziehen und ausschließen. Die DOM-App verwendet dann entweder die angegebenen Elemente oder die übereinstimmenden Elemente auf der Seite. Wenn die Eigenschaften "Einschließen" und" Ausschließen" verwendet werden, analysiert die Seite zunächst die Seite, um alle Elemente in der include-Eigenschaft zu suchen, und entfernt dann alle Elemente, die in der Eigenschaft "exclude" gefunden wurden.

## Anker {#section_ehq_psv_sy}

Anker stellen ein Element dar, dessen Inhalt autorisiert werden kann. Ein Ankerelement kann Text oder ein Bild enthalten. Die Option Selektoren, die während der App-Konstruktion übergeben wird, bestimmt die Ankerelemente.

## Anker-IDs {#section_rsb_rsv_sy}

Anker auf der Seite werden mithilfe von a `data-lf-anchor-id`identifiziert.

Um die ID für einen Anker selbst festzulegen, fügen Sie dem Element das Attribut `data-lf-custom-anchor-id` hinzu, das Sie einem Anker zuordnen möchten. Dies ist hilfreich, wenn die automatische Erkennung von Ankern fehlschlägt.

Wenn Sie beispielsweise eine andere URL für die Desktop- und mobile Versionen eines Bildes verwenden möchten, werden verschiedenen Ankern möglicherweise zwei unterschiedliche urls zugeordnet. Wenn Ihr HTML-Code beispielsweise auf `data-lf-custom-anchor-id` Mobilgeräten und Desktops gleich ist, wird das Bildelement als einzelne Anker behandelt.

Anker verfügen über einen dynamischen Typ, können aber auch explizit mithilfe des `data-lf-custom-anchor-type` Attributs festgelegt werden.

>[!NOTE]
>
>Der Wert der Aufzählungszahl muss verwendet werden.

Verfügbare Typen sind:

* **Text:** 1
* **Bild:** 2
* **Medien:** 3
* **Stark:** 4

Weitere [Informationen zur Verwendung](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) der `updateAnchors` Methode zum dynamischen Hinzufügen von Sidenote-Inhalten zur Seite finden Sie unter updateanchors.

## Benutzerdefinierter Thread-Container {#section_jdh_btv_sy}

Verwenden Sie die `threadContainerEl` Option, um einen Speicherort für einen "Sidenotes" -Thread als die Standardposition anzugeben. Wenn ein Anker aktiviert ist, erscheinen die Autoren standardmäßig neben oder unter dem relevanten Inhalt. Um diesen Standardwert zu ändern, verwenden Sie das `threadContainerEl` Element, in dem der Thread angezeigt werden soll.

Dieser Wert für diese Option funktioniert mit der Option Selektoren, außer dass nur das erste gültige Element verwendet wird.

## Zähleranzahl {#section_pld_ntv_sy}

Verwenden Sie die `numSidenotesEl` Option, um ein optionales Widget "Sidenotes-Zähler" auf Ihrer Seite einzubetten. Diese Option akzeptiert dieselbe Eingabe wie die Option Selektoren, verwendet jedoch nur das erste gültige Element im Eingabearray.

Das Widget dekoriert das bereitgestellte oder übereinstimmende Element und enthält das Eingabesymbol "Sidenotes" , die Anzahl der an dieser Position eingegebenen Alliotes und ein Hilfesymbol.

Durch Klicken auf das Widget wird ein Popover mit einer kurzen Erklärung von Sidenotes und deren Verwendung angezeigt.

Sowohl die Erklärung als auch der Beispieltext sind mithilfe von benutzerdefinierten Zeichenfolgen ( `questionExplanation` bzw. `questionMockText`) konfigurierbar. Das Erscheinungsbild des count-Widgets und der Popover können auch mithilfe von benutzerdefinierten Stilen ( `numSidenotes` bzw. `numSidenotesPopover`) konfiguriert werden.

## Hinzufügen mehrerer Sammlungen für mehrere Gruppen zu einer einzelnen Seite {#section_pjl_ptv_sy}

Mit Livefyre können Sie einer einzelnen Seite mehrere Sammlungen für einzelne Gruppen hinzufügen. Wenn die Seite beispielsweise drei Meldungsmeldungen enthält, möchten Sie möglicherweise drei separate Iterationen der App "Sidenotes" einbeziehen. Dazu müssen Sie für jede Instanz von Autoren, die Sie erstellen möchten, ein separates `ConvConfig` Objekt definieren. Beispiel:

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```
