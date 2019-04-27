---
description: Erfassen Sie die Gezählungs- und Kommentarzahlen für bestimmte Sammlungen, die auf Ihren Indexseiten angezeigt werden sollen.
seo-description: Erfassen Sie die Gezählungs- und Kommentarzahlen für bestimmte Sammlungen, die auf Ihren Indexseiten angezeigt werden sollen.
seo-title: Anzahl der Kommentare anzeigen
solution: Experience Manager
title: Anzahl der Kommentare anzeigen
uuid: 0 f 39 b 25 e -11 e 0-4945-be 71-55 fb 4798 b 6 c 7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# Anzahl der Kommentare anzeigen{#display-comment-count}

Erfassen Sie die Gezählungs- und Kommentarzahlen für bestimmte Sammlungen, die auf Ihren Indexseiten angezeigt werden sollen.

Mit Livefyre `CommentCount.js` können Sie die Inhaltszählungen für Sammlungen auf Ihrer Site abrufen. Obwohl Apps den Kommentarzähler für die aktuelle Sammlung anzeigen, kann es hilfreich sein, diese Zähler auf Ihrer Site zu synchronisieren. Diese Funktion ist besonders hilfreich, wenn Sie Inhalte in Ihrer Datenbank nicht beibehalten (oder wenn Ihre CMS-Datenbank nicht mit Livefyre synchronisiert wird).

1. Laden Sie das javascript.

   Sie können `CommentCount.js`die javascript-Datei zunächst in den `<head>` Abschnitt der Seite oder Vorlage einbetten, wo sie sie verwenden möchten.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Binden Sie das HTML-Element.

   Sobald das Skript geladen wurde, versucht er, andere Elemente auf der Seite mit einem Klassennamen zu `livefyre-commentcount`finden. Für jedes dieser Elemente sucht das Skript nach den Attributen `data-lf-site-id` und `data-lf-article-id` HTML-Attribute und verwendet diese, um Inhalte von Livefyre abzurufen und jedes Element mit dem neuesten Wert zu aktualisieren.

   Das folgende Element würde beispielsweise aktualisiert:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {important = &quot;high&quot;}
   >
   >Der `CommentCount.js` Code prüft, ob ein numerischer Wert mit der tatsächlichen Anzahl aktualisiert wird. Achten Sie darauf, einen numerischen Wert zwischen den Tags einzufügen.

   **Beispiel 1** (Verwenden der URL als Artikel-ID):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Beispiel 2** (Verwenden eines nummerierten Systems als Artikel-ID):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Optionen konfigurieren.

   Um zu steuern, wie die Inhaltszähler ersetzt werden, rufen `LF.CommentCount()` Sie ein Objekt auf und übergeben Sie es mit den Konfigurationsoptionen. Rufen Sie die Funktion auf, nachdem alle Elemente, die ersetzt werden müssen, im DOM vorhanden sind. Der beste Ort, um diese Methode aufzurufen, erfolgt in der Fußzeile. Dies geschieht, wenn das DOM geladen wird, jedoch vor dem Dokument und den fertigen Ereignissen.

   Wir erlauben die folgenden Konfigurationsoptionen:

* **replacer:** Funktion oder Regex, mit der der Text der einzelnen Inhaltszähler ersetzt wird.

* **Funktion:** Wird für die Ersetzung auf jedem Element verwendet. Die Argumente der Funktion lauten:

   **Element:** Das HTML-Element, das aktualisiert wird.
   **count:** Die Inhaltszahl für dieses Element.

* **regex:** Wird verwendet, um zu bestimmen, welcher Teil des Elementtexts durch die Anzahl ersetzt werden soll.

   **Beispiel**:

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >Verwenden Sie den Replacer, um die Nachrichtenanzahl anzupassen oder zu internationalisieren.
