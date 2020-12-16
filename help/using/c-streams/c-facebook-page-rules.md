---
description: Sie können Stream-Regeln erstellen, die Inhalte von Facebook-Seiten abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte von Facebook-Seiten abrufen.
seo-title: Facebook-Seitenregeln
solution: Experience Manager
title: Facebook-Seitenregeln
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Facebook-Seitenregeln{#facebook-page-rules}

Sie können Stream-Regeln erstellen, die Inhalte von Facebook-Seiten abrufen.

Sie können Facebook-Seitenregeln verwenden, um öffentlich veröffentlichte Inhalte von Facebook-Seiten zu streamen. Der Inhalt wird in der gleichen Häufigkeit wie SocialSync in die App oder den Ordner gezogen, was sich je nach Traffic-Mustern auf der Facebook-Seite und im Post-Traffic ändert. Links innerhalb von Facebook-Seiten werden ebenfalls unterstützt und im Stream angezeigt.

Um Facebook-Seitenregeln zu erstellen, mit denen Sie Inhalte aus Facebook-Seiten in Ihre App oder Ihren Ordner ziehen können, können Sie nach Folgendem filtern:

* **[!UICONTROL Facebook Page]**

   * Geben Sie **[!UICONTROL Name]** für die Seite ein. Geben Sie nur den nachgestellten Text für die URL ein. **Beispiel:** Um Inhalte hinzuzufügen,  `https://facebook.com/KellysSuperFunFanPage`geben Sie  ** KellysSuperFunFanPagein in das  **[!UICONTROL Name]** Feld ein.

   * Schalten Sie **[!UICONTROL Include Facebook Comments for each post]** ein, wenn Sie Benutzerkommentare zu Seitenbeiträgen hinzufügen möchten.
   * Schalten Sie **[!UICONTROL Only Show Author Posts]** ein, wenn Sie Beiträge von anderen Benutzern ausschließen möchten.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre ist auf Inhalte beschränkt, die von Facebook empfangen werden, und kann daher nicht garantieren, dass jeder Beitrag auf einer Facebook-Seite in Ihren Stream aufgenommen wird.

>[!NOTE]
>
>Wenn Facebook SocialSync und eine Facebook-Seitenregel für eine bestimmte Facebook-Seite aktiviert sind und Benutzerkommentare für die Facebook-Seitenregel aktiviert sind, setzt die Stream-Regel SocialSync außer Kraft. Inhalte werden nur basierend auf der Facebook-Seitenkuratierungsregel in die App gestreamt, nicht jedoch mit SocialSync.

Folgende Inhaltstypen werden von Facebook-Seitenkurate unterstützt:

* Seiteninhaber oder Administrator

   * Status
   * Fotos
   * Videos als Links

* Standard-Facebook-Benutzer

   * Status
   * Fotos
   * Videos als Links

* Dritte

   * Status

