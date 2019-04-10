---
description: null
seo-description: null
seo-title: Verwenden des Gewinnspielfilters
solution: Experience Manager
title: Verwenden des Gewinnspielfilters
uuid: b 0 b 1 fbae-c 88 c -403 c -9 b 91-df 6620675 f 39
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Verwenden des Gewinnspielfilters{#using-the-profanity-filter}

Der gesamte in einer Livefyre-App gepostete Inhalt wird auf Gewinn überprüft. Wenn ein in der Gewinnspielliste enthaltenes Wort im Inhalt oder im Anzeigenamen eines Benutzers gefunden wird, wird dieser Inhalt als "Gewinn" gekennzeichnet, sodass Sie ihn für Premoderation, Regeln, modq oder allgemeine Suchen in App-Inhalten filtern können.

>[!NOTE]
>
>Inhalte von Studio-Administratoren und -manager unterliegen nicht der Prüfung von Gewinnspielregeln und der von einem Moderator veröffentlichte Inhalt wird nicht markiert.

Livefyre stellt eine standardgewinnbare Liste bereit. Sie können diese Liste auf Netzwerkebene anwenden, eine eigene Liste bereitstellen oder eine Zusammenfassung der beiden Elemente verwenden. Einzelne Sites innerhalb Ihres Netzwerks übernehmen möglicherweise die Netzwerkaufstand-Liste oder verwenden eine Liste, die spezifisch für die Site spezifisch ist.

Um Ihre eigene benutzerspezifische Gewinnspielliste als Standard-Netzwerk bereitzustellen, senden Sie diese bitte an Ihren Livefyre-Kundenbetreuer.

## Aktivieren von Profit-Filtern {#section_yqc_qsk_f1b}

Aktivieren und konfigurieren Sie den Gewinn-Filter sowohl auf dem Netzwerk als auch auf der Site-Ebene. Deaktivieren Sie den Gewinn-Filter auf Netzwerkebene, um den Gewinn-Filter für alle Sites automatisch zu deaktivieren, die vom Netzwerk erben.

>[!NOTE]
>
>Alle Inhalte, die über Livefyre übergeben werden, werden auf Gewinn überprüft. Wenn Inhalt gefunden wird, der Wörter enthält, die in der standardmäßigen SAFE Profit-Liste enthalten sind, oder in Ihrer benutzerspezifischen Gewinn-Liste, wird er als "Gewinn" gekennzeichnet. » Um Livefyre so einzustellen, dass automatisch Aktionen für diese Elemente ausgeführt werden, aktivieren **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**Sie.

## Aktivieren des Gewinnspielfilters für ein Netzwerk {#section_twd_ssk_f1b}

1. Wählen **[!UICONTROL Network]** Sie aus dem Pulldown-Menü.
1. Gehe **[!UICONTROL Settings > Network Settings > Moderation]**zu.
1. Blättern Sie nach unten **[!UICONTROL Profanity List]**und legen **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**Sie fest.

1. Verwenden Sie das **[!UICONTROL Update Network Profanity List]** Feld, um der Liste Wörter hinzuzufügen, oder klicken Sie auf ein Wort, um es aus der Liste zu entfernen.

>[!NOTE]
>
>Die Bearbeitung der Netzwerklauflisten-Liste wirkt sich nicht auf Listen auf Site-Ebene aus, die bereits vorhanden sind. Um sicherzustellen, dass Änderungen am Netzwerk auf der Site vorgenommen werden, wählen **[!UICONTROL Restore Network List]** Sie die Site aus, nachdem die Änderungen vorgenommen wurden.

## Aktivieren des Gewinnspielfilters für eine Site {#section_fld_wsk_f1b}

1. Wählen Sie die Site aus dem Pulldown-Menü.
1. Gehe **[!UICONTROL Settings > Site Settings > Moderation]**zu.
1. Blättern Sie nach unten zu und **[!UICONTROL Profanity List]** setzen **[!UICONTROL Enable Profanity Checking]****[!UICONTROL ON]**Sie sie auf.

1. Wählen Sie eine der folgenden Optionen aus:

   * Wenn Sie die Gewinnspielliste vom Netzwerk übernehmen möchten (dies ist nicht üblich), setzen **[!UICONTROL Use Site Profanity List]****[!UICONTROL OFF]**Sie auf.

   * Um die Gewinnspielliste speziell für die Site zu bearbeiten, müssen Sie **[!UICONTROL Use Site Profanity List]****[!UICONTROL On]** das **[!UICONTROL Update Profanity List]** Feld öffnen, in dem Sie die Liste bearbeiten können:

      * Klicken Sie auf das Wort, um ein Wort zu entfernen.
      * Um ein Wort hinzuzufügen, geben Sie das Wort in das **[!UICONTROL Add new word]** Feld ein und treffen **[!UICONTROL Return]**Sie es.

      * Um zu sehen, ob ein Wort in der Liste enthalten ist, geben Sie das Wort in das **[!UICONTROL Test profanity filter]** Feld ein.
   * Klicken **[!UICONTROL Restore Network List]**Sie auf, um die Netzwerkaufstand-Liste erneut aufzurufen und auf die Site anzuwenden.
   * Klicken **[!UICONTROL Clear List]**Sie auf, um den gesamten Inhalt aus der Liste zu löschen und von Grund auf neu zu beginnen.


## Arbeiten mit Inhalten, die Gewinn enthalten {#section_epy_dtk_f1b}

Verwenden Sie die Gewinnspielliste, um Ihre Inhaltssuchen zu filtern und Premoderationsregeln für modq zu erstellen.

Um nach Inhalten zu suchen, die Gewinn enthalten, rufen **[!UICONTROL Library > App Content]****[!UICONTROL Filter by Flags]** Sie das Kontrollkästchen auf und markieren **[!UICONTROL Profanity]** Sie das Kontrollkästchen. Es wird der gesamte Inhalt angezeigt, der vom Gewinn-Filter für die Site oder das ausgewählte Netzwerk erfasst wurde. Diese Liste enthält Inhalte, die mit socialsync und Streams in die App gezogen werden.

Um Premoderationsregeln zu erstellen, wählen **[!UICONTROL Settings > Network Settings > Moderation]**Sie aus Studio. Sobald der Gewinn-Filter aktiviert wurde, wird eine neue Regel angezeigt, die Ihnen das Kennzeichnen oder Vormoderieren von Inhalten mit Gewinn ermöglicht. Standardmäßig aktiviert **[!UICONTROL Premoderate]** diese Regel automatisch Gewinn-Inhalte, die entweder in **[!UICONTROL Trash it]** oder **[!UICONTROL Bozo it]**.

>[!NOTE]
>
>Wenn ein einzelner Inhalt mehreren Regeltypen unterliegt (z. B. SAFE- und Flag-Regeln), werden die strengeren Regeln angewendet. Beispiel: Wenn Ihre Premoderation-Regel sagt, dass ein Inhaltselement vormoderiert wird, aber eine SAFE-Regel den Papierkorb enthält, wird sie umgebrochen.

## Gewinnspiel-Liste für ein Netzwerk anzeigen und aktualisieren {#section_qdb_btk_f1b}

1. Gehe **[!UICONTROL Settings > Network Settings > Moderation]**zu.
1. Blättern Sie nach unten zum **[!UICONTROL Profanity List]** Abschnitt.
1. Legen **[!UICONTROL Enable Profanity Checking]** Sie **[!UICONTROL On]** fest, ob die Liste für Ihr Netzwerk aktiviert werden soll ("Livefyre-Standard" oder" Hochgeladene benutzerdefinierte Liste" ) und bearbeiten Sie sie. Sie können die Liste wie folgt bearbeiten:
   * Klicken Sie auf das Wort, um ein Wort zu entfernen.
   * Um ein Wort hinzuzufügen, geben Sie das Wort in das **[!UICONTROL Add new word]** Feld ein und treffen **[!UICONTROL Return]**Sie es.
   * Um zu sehen, ob ein Wort in der Liste enthalten ist, geben Sie das Wort in das **[!UICONTROL Test profanity filter]** Feld ein.

>[!NOTE]
>
>Bearbeitungslisten können nur von Studio-Administratoren und Moderatoren bearbeitet werden.

