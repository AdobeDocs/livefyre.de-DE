---
description: Erfassen Sie die Anzahl der Beiträge und Kommentare für bestimmte Sammlungen, die auf Ihren Indexseiten angezeigt werden sollen.
seo-description: Erfassen Sie die Anzahl der Beiträge und Kommentare für bestimmte Sammlungen, die auf Ihren Indexseiten angezeigt werden sollen.
seo-title: Anzahl angezeigter Kommentare
solution: Experience Manager
title: Anzahl angezeigter Kommentare
uuid: 0f39b25e-11e0-4945-be71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c2594f919f153d1230b3dc0370f31d64cb698146
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Anzahl angezeigter Kommentare{#display-comment-count}

Erfassen Sie die Anzahl der Beiträge und Kommentare für bestimmte Sammlungen, die auf Ihren Indexseiten angezeigt werden sollen.

Mit Livefyre `CommentCount.js` können Sie die Inhaltszählung für Sammlungen auf Ihrer Site abrufen. Obwohl Apps die Anzahl der Kommentare für die aktuelle Sammlung anzeigen, kann es nützlich sein, diese Zahlen auf Ihrer Website zu synchronisieren. Diese Funktion ist besonders hilfreich, wenn Sie keine Inhalte in Ihrer Datenbank beibehalten (oder wenn Ihre CMS-Datenbank nicht mit Livefyre synchronisiert wird).

1. Laden Sie das JavaScript.

   Betten Sie `CommentCount.js`die JavaScript-Datei zunächst in den `<head>` Abschnitt der Seite oder Vorlage ein, in der Sie sie verwenden möchten.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Binden Sie das HTML-Element.

   Nach dem Laden des Skripts wird versucht, andere Elemente auf der Seite mit dem Klassennamen `livefyre-commentcount`zu finden. Für jedes dieser Elemente sucht das Skript nach `data-lf-site-id` und `data-lf-article-id` HTML-Attributen und verwendet diese zum Abrufen von Inhalten aus Livefyre und zur Aktualisierung jedes Elements mit dem neuesten Wert.

   Beispielsweise würde das folgende Element aktualisiert:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >Der `CommentCount.js` Code sucht nach einem numerischen Wert, der mit der tatsächlichen Anzahl aktualisiert werden soll. Achten Sie darauf, zwischen den Tags einen numerischen Wert einzufügen.

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

   Um mehr Kontrolle darüber zu erhalten, wie die Inhaltszählung ersetzt wird, rufen Sie ein Objekt mit den Konfigurationsoptionen auf `LF.CommentCount()` und übergeben Sie es. Achten Sie darauf, die Funktion aufzurufen, nachdem sich alle zu ersetzenden Elemente im DOM befinden. Am besten rufen Sie diese Methode in der Fußzeile auf. Dies passiert, wenn das DOM geladen wird, aber vor Dokument- und Fensterbereitstellungen.

   Folgende Konfigurationsoptionen sind zulässig:

* **Ersatz:** Funktion oder Regex, mit der der Text der einzelnen Inhaltszähler ersetzt wird.

* **Funktion:** Wird verwendet, um den Austausch für jedes Element durchzuführen. Die Argumente der Funktion lauten:

   **element:** Das HTML-Element, das aktualisiert wird.
   **count:** Die Inhaltszählung für dieses Element.

* **regex:** Wird verwendet, um festzulegen, welcher Teil des Elementtextes durch die Anzahl ersetzt werden soll.

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
   >Verwenden Sie den Ersatz, um die Meldung zur Anzahl der Kommentare anzupassen oder zu internationalisieren.
