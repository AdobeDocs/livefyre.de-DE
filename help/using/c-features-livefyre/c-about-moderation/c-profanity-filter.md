---
description: 'null '
seo-description: 'null '
seo-title: Verwenden des Wohltätigkeitsfilters
solution: Experience Manager
title: Verwenden des Wohltätigkeitsfilters
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Verwenden des Wohltätigkeitsfilters{#using-the-profanity-filter}

Alle Inhalte, die in einer Livefyre-App veröffentlicht werden, werden auf ihre Rentabilität geprüft. Wenn ein Wort aus der Liste "Fließeigenschaften"im Inhalt oder im Anzeigenamen eines Benutzers gefunden wird, wird dieser Inhalt mit "Profitabilität"gekennzeichnet, sodass Sie ihn nach Vormoderation, Regeln, ModQ oder allgemeinen Suchen in App-Inhalten filtern können.

>[!NOTE]
>
>Der Inhalt von Studio-Administratoren und -Manager unterliegt nicht der Profitabilität-Regel-Prüfung, und Inhalte, die von einem Moderator gepostet werden, werden nicht markiert.

Livefyre bietet eine Standardgewinnungsliste. Sie können diese Liste auf Netzwerkebene anwenden, eine eigene Liste angeben oder ein Aggregat der beiden verwenden. Einzelne Sites innerhalb Ihres Netzwerks übernehmen möglicherweise die Netzwerk-Profanity-Liste oder verwenden eine Liste, die auf Site-spezifisch angepasst ist.

Um eine eigene, benutzerdefinierte Liste der Gewinne als Standard für Ihr Netzwerk bereitzustellen, senden Sie diese bitte an Ihren Livefyre-Kundenbetreuer.

## Aktivieren der Profanity-Filterung {#section_yqc_qsk_f1b}

Aktivieren und konfigurieren Sie den Profilfilter sowohl auf Netzwerk- als auch auf Site-Ebene. Deaktivieren Sie den Profilfilter auf Netzwerkebene, um den Abstandsfilter für alle Sites, die vom Netzwerk erben, automatisch zu deaktivieren.

>[!NOTE]
>
>Der gesamte Inhalt, der durch Livefyre fließt, wird auf Unannehmlichkeit überprüft. Wenn Inhalt gefunden wird, der Wörter enthält, die in der Standardliste der SAFE-Sicherheit oder in Ihrer benutzerdefinierten Liste der Wohltätigkeitseinrichtungen enthalten sind, wird er mit "Profitabilität"gekennzeichnet. Um Livefyre so einzurichten, dass es automatisch Aktionen für diese Elemente ausführt, gehen Sie **[!UICONTROL Enable Profanity Checking]** zu **[!UICONTROL ON]**.

## Aktivieren des Wohlstandsfilters für ein Netzwerk {#section_twd_ssk_f1b}

1. Wählen Sie **[!UICONTROL Network]** aus dem Pulldown-Menü des Netzwerks.
1. Gehe zu **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Führen Sie einen Bildlauf nach unten **[!UICONTROL Profanity List]** durch und legen Sie **[!UICONTROL Enable Profanity Checking]** den Wert **[!UICONTROL ON]** fest.

1. Verwenden Sie das **[!UICONTROL Update Network Profanity List]** Feld, um der Liste Wörter hinzuzufügen, oder klicken Sie auf ein Wort, um es aus der Liste zu entfernen.

>[!NOTE]
>
>Die Bearbeitung der Profanity-Liste auf Netzwerkebene hat keine Auswirkungen auf bereits vorhandene Listen auf Site-Ebene. Um sicherzustellen, dass Änderungen vom Netzwerk an der Site vorgenommen werden, wählen Sie **[!UICONTROL Restore Network List]** die Site aus, nachdem die Änderungen vorgenommen wurden.

## Aktivieren des Wohlstandsfilters für eine Site {#section_fld_wsk_f1b}

1. Wählen Sie die Site aus dem Pulldown-Menü des Netzwerks.
1. Gehe zu **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Blättern Sie nach unten zum **[!UICONTROL Profanity List]** und legen Sie **[!UICONTROL Enable Profanity Checking]** den Wert **[!UICONTROL ON]** fest.

1. Wählen Sie eine der folgenden Optionen:

   * Um die Profanity-Liste vom Netzwerk zu übernehmen (dies ist nicht üblich), setzen Sie **[!UICONTROL Use Site Profanity List]** auf **[!UICONTROL OFF]**.

   * Um die Profanitätsliste speziell für die Site zu bearbeiten, öffnen Sie **[!UICONTROL Use Site Profanity List]** das Feld, in dem Sie die Liste bearbeiten können, **[!UICONTROL On]** um das **[!UICONTROL Update Profanity List]** Feld zu öffnen:

      * Um ein Wort zu entfernen, klicken Sie auf das Wort.
      * Um ein Wort hinzuzufügen, geben Sie das Wort in das **[!UICONTROL Add new word]** Feld ein und klicken Sie auf **[!UICONTROL Return]**.

      * Um zu sehen, ob ein Wort in der Liste enthalten ist, geben Sie das Wort in das **[!UICONTROL Test profanity filter]** Feld ein.
   * Klicken Sie auf **[!UICONTROL Restore Network List]**, um die Netzwerkgewinnungsliste erneut zu importieren und sie auf die Site anzuwenden.
   * Klicken Sie auf **[!UICONTROL Clear List]**, um alle Inhalte aus der Liste zu löschen und von vorne zu beginnen.


## Arbeiten mit Inhalten, die Wohlstand beinhalten {#section_epy_dtk_f1b}

Verwenden Sie die Profitabilität-Liste, um Ihre Inhaltssuche zu filtern und Vormoderationsregeln für ModQ zu erstellen.

Um nach Inhalten zu suchen, die Höflichkeit enthalten, gehen Sie zu **[!UICONTROL Library > App Content]** und **[!UICONTROL Filter by Flags]** aktivieren Sie das **[!UICONTROL Profanity]** Kontrollkästchen. Alle Inhalte, die vom Profanity-Filter für die ausgewählte Site oder das ausgewählte Netzwerk erfasst wurden, werden angezeigt. Diese Liste enthält Inhalte, die mit SocialSync und Streams in die App gezogen werden.

Wählen Sie zum Erstellen von Vormoderationsregeln in Studio **[!UICONTROL Settings > Network Settings > Moderation]**. Sobald der Bereichsfilter aktiviert wurde, wird eine neue Regel angezeigt, mit der Sie Inhalte mit Rentabilität kennzeichnen oder vormoderieren können. Standardmäßig aktiviert diese Regel automatisch **[!UICONTROL Premoderate]** für profane Inhalte, die entweder in **[!UICONTROL Trash it]** oder **[!UICONTROL Bozo it]** geändert werden können.

>[!NOTE]
>
>Wenn für ein einzelnes Inhaltselement mehrere Regeltypen gelten (wie SAFE- und Flag-Regeln), werden strengere Regeln angewendet. Beispiel: Wenn Ihre Vormoderationsregel besagt, dass ein Inhalt vormoderiert werden soll, eine SAFE-Regel jedoch den Papierkorb anzeigt, wird er als Papierkorb markiert.

## Anzeigen und Aktualisieren der Wohlfahrtsliste für ein Netzwerk {#section_qdb_btk_f1b}

1. Gehe zu **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Blättern Sie nach unten zum **[!UICONTROL Profanity List]** Abschnitt.
1. Legen Sie **[!UICONTROL Enable Profanity Checking]** fest, **[!UICONTROL On]** dass die für Ihr Netzwerk aktivierte Liste (Livefyre-Standard oder Ihre hochgeladene benutzerdefinierte Liste) angezeigt und bearbeitet werden soll. Sie können die Liste wie folgt bearbeiten:
   * Um ein Wort zu entfernen, klicken Sie auf das Wort.
   * Um ein Wort hinzuzufügen, geben Sie das Wort in das **[!UICONTROL Add new word]** Feld ein und klicken Sie auf **[!UICONTROL Return]**.
   * Um zu sehen, ob ein Wort in der Liste enthalten ist, geben Sie das Wort in das **[!UICONTROL Test profanity filter]** Feld ein.

>[!NOTE]
>
>Nur Studio-Administratoren und -Moderatoren können Profanity-Listen bearbeiten.

