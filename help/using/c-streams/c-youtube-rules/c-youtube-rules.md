---
description: Sie können Stream-Regeln erstellen, die Inhalte aus youtube-Regeln abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte aus youtube-Regeln abrufen.
seo-title: Youtube-Regeln
solution: Experience Manager
title: Youtube-Regeln
uuid: ec 6 a 3780-7119-45 c 3-8 ab 2-fb 0 f 9803 d 161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b

---


# Youtube-Regeln {#youtube-rules}

Sie können Stream-Regeln erstellen, die Inhalte aus youtube-Regeln abrufen.

Erstellen Sie youtube-Regeln basierend auf User, Channel oder Playlist.

Um youtube-Regeln zum Abrufen von Inhalten von youtube in Ihre App oder Ihren Ordner zu erstellen, können Sie nach Folgendem Filtern nach:

* **[!UICONTROL User]**
   * Geben Sie die Vanity-Zeichenfolge **[!UICONTROL User]** ein, um Videos vom Benutzer im Stream aufzunehmen.
   * Wenn beispielsweise die URL des Benutzerfeeds, den Sie eingeben möchten, eingeben soll, `https://www.youtube.com/user/livefyresupport`geben `livefyresupport`Sie einfach ein.

* **[!UICONTROL Channel]**
   * Geben Sie die Vanity-Zeichenfolge **[!UICONTROL Channel]** ein, um Videos aus einem Kanal im Stream einzuschließen.
   * Wenn Sie z. B. die URL des Kanalfeeds eingeben möchten, geben `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg``UCeNZlh03MyUkjRlLFpVQxsg`Sie einfach ein.

* **[!UICONTROL Playlist]**
   * Geben Sie die Vanity-Zeichenfolge **[!UICONTROL Playlist]** ein, um Videos aus einer Playlist im Stream einzuschließen.
   * Wenn die URL des Playlist-Feeds, den Sie eingeben möchten, `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`beispielsweise lautet, geben Sie `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Wenn dies festgelegt ist:
   * **[!UICONTROL Enabled]**, fügt Livefyre die ersten 15 Inhaltselemente im Feed unabhängig vom Veröffentlichungsdatum in den Stream ein.
   * **[!UICONTROL Disabled]**, fügt Livefyre die ersten 15 Inhaltselemente in Ihrem Feed mit einem Veröffentlichungsdatum hinzu, der mit dem Erstellungsdatum des Stream-Regels oder höher übereinstimmt.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
