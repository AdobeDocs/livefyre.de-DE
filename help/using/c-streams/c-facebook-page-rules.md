---
description: Sie können Stream-Regeln erstellen, die Inhalte von Facebook-Seiten abrufen.
title: Facebook-Seitenregeln
exl-id: 1dc728c6-81fa-4c6c-acba-d9a4aea71ed2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# Facebook-Seitenregeln{#facebook-page-rules}

Sie können Stream-Regeln erstellen, die Inhalte von Facebook-Seiten abrufen.

Sie können Facebook-Seitenregeln verwenden, um öffentlich veröffentlichte Inhalte von Facebook-Seiten zu streamen. Der Inhalt wird in der gleichen Häufigkeit wie SocialSync in die App oder den Ordner gezogen, was sich je nach Facebook-Seiten- und Post-Traffic-Mustern ändert. Links innerhalb von Facebook-Seiten werden ebenfalls unterstützt und im Stream angezeigt.

Um Facebook-Seitenregeln zu erstellen, mit denen Inhalte von Facebook-Seiten in Ihre App oder Ihren Ordner gezogen werden, können Sie nach Folgendem filtern:

* **[!UICONTROL Facebook Page]**

   * Geben Sie **[!UICONTROL Name]** für die Seite ein. Geben Sie nur den nachgestellten Text für die URL ein. **Beispiel:** Um Inhalte hinzuzufügen,  `https://facebook.com/KellysSuperFunFanPage`geben Sie  ** KellysSuperFunFanPagein in das  **[!UICONTROL Name]** Feld ein.

   * Schalten Sie **[!UICONTROL Include Facebook Comments for each post]** ein, wenn Sie Benutzerkommentare zu Seitenbeiträgen hinzufügen möchten.
   * Schalten Sie **[!UICONTROL Only Show Author Posts]** ein, wenn Sie Beiträge von anderen Benutzern ausschließen möchten.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre ist auf Inhalte beschränkt, die von Facebook empfangen werden, und kann daher nicht garantieren, dass jeder Beitrag auf einer Facebook-Seite in Ihren Stream eingeschlossen wird.

>[!NOTE]
>
>Wenn Facebook SocialSync und eine Facebook-Seitenregel für eine bestimmte Facebook-Seite aktiviert sind und Benutzerkommentare für die Facebook-Seitenregel aktiviert sind, setzt die Stream-Regel SocialSync außer Kraft. Inhalte werden nur auf Grundlage der Facebook-Seitenkuratierungsregel in die App gestreamt, nicht jedoch mit SocialSync.

Folgende Inhaltstypen werden von der Facebook-Seitenkurate unterstützt:

* Seiteninhaber oder Administrator

   * Status
   * Fotos
   * Videos als Links

* Facebook Standard-Benutzer

   * Status
   * Fotos
   * Videos als Links

* Dritte

   * Status
