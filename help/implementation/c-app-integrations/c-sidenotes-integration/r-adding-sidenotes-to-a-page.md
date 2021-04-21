---
title: Hinzufügen von Sidemarken zu einer Seite
description: Hinzufügen von Sidemarken zu einer Seite
exl-id: 3ec089d0-3d51-4918-b510-d30ef645c9c2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Hinzufügen von Sidemarken zu einer Seite {#adding-sidenotes-to-a-page}

Livefyre bietet mehrere Konfigurationsoptionen, um Simit auf Ihrer Seite zu positionieren:

* Mit der Option &quot;Selektoren&quot;werden die Elemente definiert, auf denen Simit angezeigt werden soll.
* Anker stellen Elemente dar, die als Präsidentenelemente dienen können.
* Mit dem benutzerspezifischen Thread-Container können Sie festlegen, wo sich der Siunterschiedslos positionierte Inhalt befindet.
* Mit der Zähloption &quot;Siegels&quot;können Sie die Anzahl der an der angegebenen Position hinzugefügten Siegels anzeigen.
* Verwenden Sie mehrere `ConvConfig`-Objekte, um mehreren Textabschnitten auf einer einzelnen Seite SiMerkmal hinzuzufügen.

## Selektoren {#section_wyj_4sv_sy}

Mit der Option &quot;Selektoren&quot;kann Simit Inhalte auf der Seite suchen. Mit dem Wert für diese Option können Sie die zu verwendenden Elemente dynamisch bestimmen. Dabei kann es sich um eine Selektorzeichenfolge (z. B. &quot;#content p, #content img&quot;), ein jQuery-Objekt (z. B. `$(‘#content’)`), ein Array mit DOM-Elementen oder ein Objekt mit zwei Eigenschaften handeln: ein- und ausschließen. Die Siegels-App verwendet dann entweder die angegebenen Elemente oder die entsprechenden Elemente auf der Seite. Wenn die Eigenschaften &quot;Einschließen&quot;und &quot;Ausschließen&quot;verwendet werden, wird die Seite zunächst analysiert, um alle Elemente in der Eigenschaft &quot;Einschließen&quot;zu finden, und dann entfernt das Element, das in der Eigenschaft &quot;Ausschließen&quot;gefunden wurde.

## Verankerungen {#section_ehq_psv_sy}

Anker stellen ein Element dar, dessen Inhalt mit der Ausrichtung versehen werden kann. Ein Ankerelement kann Text oder ein Bild enthalten. Die Ankerelemente werden von der Auswahloption bestimmt, die während der App-Erstellung übergeben wird.

## Anker-IDs {#section_rsb_rsv_sy}

Anker auf der Seite werden mit einem `data-lf-anchor-id` identifiziert.

Um die ID für einen Anker selbst festzulegen, fügen Sie das Attribut `data-lf-custom-anchor-id` dem Element hinzu, das Sie einem Anker zuordnen möchten. Dies ist hilfreich, wenn die automatische Erkennung von Ankern fehlschlägt.

Wenn Sie beispielsweise eine andere URL für die Desktop- und Mobilversion eines Bildes verwenden möchten, können zwei verschiedene URLs verschiedenen Ankern zugeordnet werden. Wenn Ihr HTML-Code stattdessen ein `data-lf-custom-anchor-id` bereitstellt, das sowohl auf dem Mobilgerät als auch auf dem Desktop gleich ist, wird das Bildelement als einzelner Anker behandelt.

Anker haben einen Typ, der dynamisch bestimmt wird, können aber auch explizit mithilfe des Attributs `data-lf-custom-anchor-type` eingestellt werden.

>[!NOTE]
>
>Der Wert der Auflistung muss verwendet werden.

Verfügbare Typen sind:

* **Text:** 1
* **Bild:** 2
* **Medien:** 3
* **Rich:** 4

Weitere Informationen zum dynamischen Hinzufügen von Sidenote-Inhalten zur Seite finden Sie unter [updateAnchors-Methode](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md).`updateAnchors`

## Benutzerdefinierter Thread-Container {#section_jdh_btv_sy}

Verwenden Sie die Option `threadContainerEl`, um einen anderen Speicherort als die Standardposition für einen Si7-Thread anzugeben. Wenn ein Anker aktiviert ist, wird der Sidebar standardmäßig neben oder unter dem relevanten Inhalt angezeigt. Um diese Standardeinstellung zu ändern, verwenden Sie `threadContainerEl`, um das Element anzugeben, in dem der Thread angezeigt werden soll.

Dieser Wert für diese Option funktioniert genauso wie die Option &quot;Selektoren&quot;, außer dass nur das erste gültige Element verwendet wird.

## Anzahl der Attribute {#section_pld_ntv_sy}

Verwenden Sie die Option `numSidenotesEl`, um ein optionales Widget zur Zählung der Seitenzahl auf Ihrer Seite einzubetten. Diese Option akzeptiert die gleiche Eingabe wie die Option &quot;Selektoren&quot;, verwendet jedoch nur das erste gültige Element im Eingabe-Array.

Das Widget dekoriert das bereitgestellte oder übereinstimmende Element und enthält das Symbol für die Eingabe von Sizilien, die Zahl der an dieser Position eingegebenen Sidemarken und ein Hilfesymbol.

Wenn Sie auf das Widget klicken, wird ein Popup mit einer kurzen Erläuterung von Siegels und deren Verwendung angezeigt.

Sowohl die Erläuterung als auch der Beispieltext können mithilfe von benutzerdefinierten Zeichenfolgen ( `questionExplanation` bzw. `questionMockText`) konfiguriert werden. Das Erscheinungsbild des Zähler-Widgets und des Popup-Fensters kann auch mit benutzerdefinierten Stilen ( `numSidenotes` bzw. `numSidenotesPopover`) konfiguriert werden.

## Hinzufügen mehrerer Sammlungen zu einer einzelnen Seite {#section_pjl_ptv_sy}

Mit Livefyre können Sie einer einzelnen Seite mehrere Siunterschiedlichste Sammlungen hinzufügen. Wenn die Seite z. B. drei Nachrichten enthält, möchten Sie möglicherweise drei separate Iterationen der Sibezeichnet-App hinzufügen. Dazu müssen Sie für jede zu erstellende Instanz von Sibezeichnet ein separates `ConvConfig`-Objekt definieren. Beispiel:

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
