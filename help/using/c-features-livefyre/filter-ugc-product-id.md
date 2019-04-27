---
description: Durch das Filtern von UGC nach Produkt-ID können Sie die exakte App auf mehreren Seiten einbetten und gleichzeitig verschiedene produktspezifische UGC für jede Seite anzeigen.
seo-description: Durch das Filtern von UGC nach Produkt-ID können Sie die exakte App auf mehreren Seiten einbetten und gleichzeitig verschiedene produktspezifische UGC für jede Seite anzeigen.
seo-title: FILC nach Produkt-ID filtern
title: FILC nach Produkt-ID filtern
uuid: 98108 ddb -5710-4331-891 b -7 e 1 bbb 106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816

---


# FILC nach Produkt-ID filtern {#filter-ugc-product-id}

Durch das Filtern von UGC nach Produkt-ID können Sie die exakte App auf mehreren Seiten einbetten und gleichzeitig verschiedene produktspezifische UGC für jede Seite anzeigen.

Gehen Sie wie folgt vor, um UGC nach Produkt-ID zu filtern:

1. Navigieren Sie in Livefyre Studio zur **[!UICONTROL Apps]** Registerkarte.

1. Wählen Sie die App aus, die Sie ändern möchten.

1. Wählen Sie in der linken Leiste die Registerkarte &quot;Designer&quot; aus.

1. Enable **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. Wählen Sie die Produktordner der obersten Ebene aus, die das Produkt oder die Produkte enthalten, nach denen Sie UGC filtern möchten.
Verwenden Sie Strg/Befehl + Klicken, um mehrere Ordner auszuwählen.

1. Disable **[!UICONTROL Show related content]**.
Wenn diese Option aktiviert ist, wird der mit dem `data-lf-attr-product` Attribut gefilterte Inhalt zuerst angezeigt, gefolgt von allen anderen Inhalten in der App.

1. Klicken **[!UICONTROL Publish]** Sie auf.

1. Fügen Sie die Produkt-IDs, die Sie filtern möchten, in den resultierenden Code ein.

>[!NOTE]
>
>Navigieren Sie zum Suchen nach Produkt-IDs **[!UICONTROL Settings > Products]** zu. Suchen Sie das gewünschte Produkt und wählen Sie es aus und die ID wird angezeigt.

Der folgende Code wird beispielsweise für eine Media Wall-App generiert:

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published" datalf-
env="prod" data-lf-read-only="" data-lf-attr-product="<product
 1>,<product 2>"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

Um ein Produkt zu taggen, ersetzen `<product 1>` Sie im `data-lf-attr-product` Attribut durch die gewünschte Produkt-ID. Sie können ein Produkt oder mehr taggen, indem Sie zusätzliche kommagetrennte Produkt-IDs hinzufügen. Produkte müssen im Produktordner oder in den in Schritt 5 ausgewählten Ordnern der obersten Ebene enthalten sein.

Das geänderte Codesegment würde wie folgt angezeigt:

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published"
 data-lf-env="prod" data-lf-read-only="" data-lf-attrproduct="
109,47"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

Die App zeigt jetzt nur die mit Tags versehenen Produkt-IDs an.