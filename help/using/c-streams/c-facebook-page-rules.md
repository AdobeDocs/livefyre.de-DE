---
description: Sie können Stream-Regeln erstellen, die Inhalte aus Facebook-Seiten abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte aus Facebook-Seiten abrufen.
seo-title: Facebook-Seitenregeln
solution: Experience Manager
title: Facebook-Seitenregeln
uuid: 2 be be be 63476-1 a 92-409 d-a 22 f-e 1 ec 66 b 6 dcc 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Facebook-Seitenregeln{#facebook-page-rules}

Sie können Stream-Regeln erstellen, die Inhalte aus Facebook-Seiten abrufen.

Sie können Facebook-Seitenregeln verwenden, um öffentlich gepostete Inhalte aus Facebook-Seiten zu streamen. Der Inhalt wird in der App oder dem Ordner mit derselben Frequenz wie socialsync abgerufen, die sich auf der Grundlage von Facebook-Seiten- und Post-Traffic-Mustern ändert. Links innerhalb von Facebook-Seiten werden ebenfalls unterstützt und werden im Stream angezeigt.

Um Facebook-Seitenregeln zu erstellen, um Inhalte von Facebook-Seiten in Ihre App oder Ihren Ordner abzurufen, können Sie nach Folgendem Filtern nach:

* **[!UICONTROL Facebook Page]**

   * Geben Sie die **[!UICONTROL Name]** Seite ein. Geben Sie nur den nachfolgenden Text für die URL ein. **Beispiel:** Um Inhalt hinzuzufügen `https://facebook.com/KellysSuperFunFanPage`, geben Sie *kellyssuperfunfanpassungen kellyssuperfunfanpage* in das **[!UICONTROL Name]** Feld ein.

   * Schalten **[!UICONTROL Include Facebook Comments for each post]** Sie ein, wenn Sie Benutzerkommentare an Seitenbeiträge einbeziehen möchten.
   * Schalten **[!UICONTROL Only Show Author Posts]** Sie ein, wenn Sie Beiträge von anderen Benutzern ausschließen möchten.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre ist auf Inhalte beschränkt, die von Facebook empfangen wurden, und kann daher nicht garantieren, dass jeder Beitrag auf einer Facebook-Seite in Ihren Stream aufgenommen wird.

>[!NOTE]
>
>Wenn Facebook socialsync und eine Facebook-Seitenregel für eine bestimmte Facebook-Seite aktiviert sind und Benutzerkommentare für die Facebook-Seitenregel aktiviert sind, setzt die Stream-Regel socialsync außer Kraft. Inhalte werden auf der Grundlage der Regel Nur für Facebook-Seiten und nicht mit socialsync in die App gestreamt.

Zu den von Facebook-Seiten-Kuratierungen unterstützten Inhalten gehören:

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

