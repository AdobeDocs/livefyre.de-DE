---
description: 'null '
seo-description: 'null '
seo-title: Hinzufügen von Sidemarken zu einer Seite
solution: Experience Manager
title: Hinzufügen von Sidemarken zu einer Seite
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# Hinzufügen von Sidemarken zu einer Seite {#adding-sidenotes-to-a-page}

Livefyre bietet mehrere Konfigurationsoptionen, um Simit auf Ihrer Seite zu positionieren:

* Mit der Option "Selektoren"werden die Elemente definiert, auf denen Simit angezeigt werden soll.
* Anker stellen Elemente dar, die als Präsidentenelemente dienen können.
* Mit dem benutzerdefinierten Thread-Container können Sie festlegen, wo sich der Siunterschiedslos positionierte Thread im Verhältnis zum Inhalt befinden soll.
* Mit der Zähloption "Siegels"können Sie die Anzahl der an der angegebenen Position hinzugefügten Siegels anzeigen.
* Verwenden Sie mehrere `ConvConfig` Objekte, um mehreren Textabschnitten auf einer einzelnen Seite Sistat hinzuzufügen.

## Selektoren {#section_wyj_4sv_sy}

Mit der Option "Selektoren"kann Simit Inhalte auf der Seite suchen. Mit dem Wert für diese Option können Sie die zu verwendenden Elemente dynamisch bestimmen. Es kann sich um eine Selektorzeichenfolge (z. B. "#content p, #content img"), ein jQuery-Objekt (z. B. `$(‘#content’)`), ein Array mit DOM-Elementen oder ein Objekt mit zwei Eigenschaften handeln: ein- und ausschließen. Die Siegels-App verwendet dann entweder die angegebenen Elemente oder die entsprechenden Elemente auf der Seite. Wenn die Eigenschaften "Einschließen"und "Ausschließen"verwendet werden, wird die Seite zunächst analysiert, um alle Elemente in der Eigenschaft "Einschließen"zu finden, und dann entfernt das Element, das in der Eigenschaft "Ausschließen"gefunden wurde.

## Anker {#section_ehq_psv_sy}

Anker stellen ein Element dar, dessen Inhalt mit der Ausrichtung versehen werden kann. Ein Ankerelement kann Text oder ein Bild enthalten. Die Ankerelemente werden von der Auswahloption bestimmt, die während der App-Erstellung übergeben wird.

## Anker-IDs {#section_rsb_rsv_sy}

Die Anker auf der Seite werden mit einem `data-lf-anchor-id`gekennzeichnet.

Um die ID für einen Anker selbst festzulegen, fügen Sie das Attribut dem Element hinzu, das Sie einem Anker zuordnen möchten. `data-lf-custom-anchor-id` Dies ist hilfreich, wenn die automatische Erkennung von Ankern fehlschlägt.

Wenn Sie beispielsweise eine andere URL für die Desktop- und Mobilversion eines Bildes verwenden möchten, können zwei verschiedene URLs verschiedenen Ankern zugeordnet werden. Wenn Ihr HTML-Code stattdessen ein `data-lf-custom-anchor-id` ähnliches Element auf dem Mobilgerät und dem Desktop bereitstellt, wird das Bildelement als einzelner Anker behandelt.

Anker haben einen Typ, der dynamisch bestimmt wird, aber auch explizit mithilfe des `data-lf-custom-anchor-type` Attributs festgelegt werden kann.

>[!NOTE]
>
>Der Wert der Aufzählungsnummer muss verwendet werden.

Verfügbare Typen sind:

* **** Text: 1
* **** Bild: 2
* **** Medien: 3
* **** Rich: 4

Weitere Informationen zum dynamischen Hinzufügen von Sidenote-Inhalten zur Seite finden Sie unter [updateAnchors-Methode](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) `updateAnchors` .

## Benutzerdefinierter Thread-Container {#section_jdh_btv_sy}

Verwenden Sie die `threadContainerEl` Option, um eine andere Position als die Standardposition für einen Siunterschiedlichsten Thread festzulegen. Wenn ein Anker aktiviert ist, wird der Sidebar standardmäßig neben oder unter dem relevanten Inhalt angezeigt. Um diese Standardeinstellung zu ändern, verwenden Sie die `threadContainerEl` , um das Element anzugeben, in dem der Thread angezeigt werden soll.

Dieser Wert für diese Option funktioniert genauso wie die Option "Selektoren", außer dass nur das erste gültige Element verwendet wird.

## Zähler {#section_pld_ntv_sy}

Verwenden Sie die `numSidenotesEl` Option zum Einbetten eines optionalen Widgets für die Anzahl der Sidentis auf Ihrer Seite. Diese Option akzeptiert die gleiche Eingabe wie die Selektoroption, verwendet jedoch nur das erste gültige Element im Eingabe-Array.

Das Widget dekoriert das bereitgestellte oder übereinstimmende Element und enthält das Symbol für die Eingabe von Sizilien, die Zahl der an dieser Position eingegebenen Sidemarken und ein Hilfesymbol.

Wenn Sie auf das Widget klicken, wird ein Popup mit einer kurzen Erläuterung von Siegels und deren Verwendung angezeigt.

Sowohl die Erläuterung als auch der Beispieltext können mithilfe von benutzerdefinierten Zeichenfolgen ( `questionExplanation` bzw. `questionMockText`) konfiguriert werden. Das Erscheinungsbild des Zähler-Widgets und des Popup-Fensters kann auch mit benutzerdefinierten Stilen ( `numSidenotes` bzw. `numSidenotesPopover`) konfiguriert werden.

## Hinzufügen mehrerer Sammlungen zu einer einzelnen Seite {#section_pjl_ptv_sy}

Mit Livefyre können Sie einer einzelnen Seite mehrere Siunterschiedlichste Sammlungen hinzufügen. Wenn die Seite z. B. drei Nachrichten enthält, möchten Sie möglicherweise drei separate Iterationen der Sibezeichnet-App hinzufügen. Dazu müssen Sie für jede Instanz von Siegels, die Sie erstellen möchten, ein separates `ConvConfig` Objekt definieren. Beispiel:

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
