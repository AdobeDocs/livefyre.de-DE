---
description: 'null '
seo-description: 'null '
seo-title: Verwenden des Wohltätigkeitsfilters
solution: Experience Manager
title: Verwenden des Wohltätigkeitsfilters
uuid: b0b1fbae-c88c-403c-9b91-df6620675f39
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 1%

---


# Verwenden des Wohlstandsfilters{#using-the-profanity-filter}

Alle Inhalte, die in einer Livefyre-App veröffentlicht wurden, werden auf ihre Rentabilität geprüft. Wenn ein in der Liste &quot;Fließtext&quot;enthaltenes Wort im Inhalt oder im Anzeigenamen eines Benutzers gefunden wird, wird dieser Inhalt mit &quot;Profitabilität&quot;gekennzeichnet, sodass Sie ihn nach Vorgabe, Regeln, ModQ oder allgemeinen Suchen in App-Inhalten filtern können.

>[!NOTE]
>
>Der Inhalt von Studio-Administratoren und -Manager unterliegt nicht der Profitabilität-Regel-Prüfung, und Inhalte, die von einem Moderator gepostet werden, werden nicht markiert.

Livefyre bietet eine standardmäßige Liste der Rentabilität. Sie können diese Liste auf Netzwerkebene anwenden, Ihre eigene Liste angeben oder ein Aggregat der beiden verwenden. Einzelne Sites innerhalb Ihres Netzwerks können die Netzwerk-Profanity-Liste übernehmen oder eine Liste verwenden, die auf Site-spezifische Anforderungen angepasst wurde.

Um Ihre eigene, benutzerdefinierte Liste als Netzwerkstandard bereitzustellen, senden Sie diese bitte an Ihren Livefyre-Kundenbetreuer.

## Aktivieren der Profanity-Filterung {#section_yqc_qsk_f1b}

Aktivieren und konfigurieren Sie den Rentabilitätsfilter sowohl auf Netzwerk- als auch auf Site-Ebene. Deaktivieren Sie den Profilfilter auf Netzwerkebene, um den Abstandsfilter für alle Sites, die vom Netzwerk erben, automatisch zu deaktivieren.

>[!NOTE]
>
>Der gesamte Inhalt, der durch Livefyre fließt, wird auf Unannehmlichkeit überprüft. Wenn Inhalt gefunden wird, der Wörter enthält, die in der standardmäßigen SAFE-Liste oder in Ihrer benutzerdefinierten Profanity-Liste enthalten sind, wird er mit &quot;Profitabilität&quot;gekennzeichnet. Um festzulegen, dass Livefyre automatisch Aktionen für diese Elemente ausführt, schalten Sie **[!UICONTROL Enable Profanity Checking]** auf **[!UICONTROL ON]** um.

## Aktivieren Sie den Profanitätsfilter für ein Netzwerk {#section_twd_ssk_f1b}

1. Wählen Sie **[!UICONTROL Network]** aus dem Netzwerk-Pulldown-Menü.
1. Gehe zu **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Blättern Sie nach unten zu **[!UICONTROL Profanity List]** und setzen Sie **[!UICONTROL Enable Profanity Checking]** auf **[!UICONTROL ON]**.

1. Verwenden Sie das Feld **[!UICONTROL Update Network Profanity List]**, um der Liste Wörter hinzuzufügen, oder klicken Sie auf ein Wort, um es aus der Liste zu entfernen.

>[!NOTE]
>
>Die Bearbeitung der Profanity-Liste auf Netzwerkebene hat keine Auswirkungen auf bereits bestehende Listen auf Site-Ebene. Um sicherzustellen, dass Änderungen vom Netzwerk an der Site vorgenommen werden, wählen Sie **[!UICONTROL Restore Network List]** für die Site aus, nachdem die Änderungen vorgenommen wurden.

## Aktivieren Sie den Wohlstandsfilter für eine Site {#section_fld_wsk_f1b}

1. Wählen Sie die Site aus dem Pulldown-Menü des Netzwerks.
1. Gehe zu **[!UICONTROL Settings > Site Settings > Moderation]**.
1. Blättern Sie nach unten zum **[!UICONTROL Profanity List]** und setzen Sie **[!UICONTROL Enable Profanity Checking]** auf **[!UICONTROL ON]**.

1. Wählen Sie eine der folgenden Optionen:

   * Um die Profanity-Liste vom Netzwerk zu übernehmen (dies ist nicht üblich), setzen Sie **[!UICONTROL Use Site Profanity List]** auf **[!UICONTROL OFF]**.

   * Um die Profanity-Liste speziell für die Site zu bearbeiten, setzen Sie **[!UICONTROL Use Site Profanity List]** auf **[!UICONTROL On]**, um das **[!UICONTROL Update Profanity List]**-Feld zu öffnen, in dem Sie die Liste bearbeiten können:

      * Um ein Wort zu entfernen, klicken Sie auf das Wort.
      * Um ein Wort hinzuzufügen, geben Sie das Wort in das Feld **[!UICONTROL Add new word]** ein und klicken Sie auf **[!UICONTROL Return]**.

      * Um zu sehen, ob ein Wort in der Liste enthalten ist, geben Sie das Wort in das Feld **[!UICONTROL Test profanity filter]** ein.
   * Um die Netzwerk-Profanity-Liste erneut zu importieren und sie auf die Site anzuwenden, klicken Sie auf **[!UICONTROL Restore Network List]**.
   * Klicken Sie auf **[!UICONTROL Clear List]**, um den gesamten Inhalt aus der Liste und dem Beginn zu entfernen.


## Arbeiten mit Inhalten, die Profitabilität {#section_epy_dtk_f1b} enthalten

Verwenden Sie die Profanity-Liste, um Ihre Inhaltssuche zu filtern und Vormoderationsregeln für ModQ zu erstellen.

Um nach Inhalten zu suchen, die Wohlstand enthalten, gehen Sie zu **[!UICONTROL Library > App Content]**, **[!UICONTROL Filter by Flags]** und markieren Sie das Kontrollkästchen **[!UICONTROL Profanity]**. Alle Inhalte, die vom Profanity-Filter für die ausgewählte Site oder das ausgewählte Netzwerk erfasst wurden, werden angezeigt. Diese Liste umfasst Inhalte, die mit SocialSync und Streams in die App gezogen werden.

Um Vormoderationsregeln zu erstellen, wählen Sie in Studio **[!UICONTROL Settings > Network Settings > Moderation]** aus. Sobald der Bereichsfilter aktiviert wurde, wird eine neue Regel angezeigt, mit der Sie Inhalte mit Rentabilität kennzeichnen oder vormoderieren können. Standardmäßig aktiviert diese Regel &quot;**[!UICONTROL Premoderate]**&quot;für profanen Inhalt, der entweder in **[!UICONTROL Trash it]** oder **[!UICONTROL Bozo it]** geändert werden kann.

>[!NOTE]
>
>Wenn für ein einzelnes Inhaltselement mehrere Regeltypen gelten (wie SAFE- und Flag-Regeln), werden strengere Regeln angewendet. Beispiel: Wenn Ihre Vormoderationsregel besagt, dass ein Inhalt vormoderiert werden soll, eine SAFE-Regel jedoch den Papierkorb anzeigt, wird er als Papierkorb markiert.

## Ansicht und Aktualisierung der Profanity-Liste für ein Netzwerk {#section_qdb_btk_f1b}

1. Gehe zu **[!UICONTROL Settings > Network Settings > Moderation]**.
1. Blättern Sie nach unten zum Abschnitt **[!UICONTROL Profanity List]**.
1. Setzen Sie **[!UICONTROL Enable Profanity Checking]** auf **[!UICONTROL On]**, um die für Ihr Netzwerk aktivierte Liste anzuzeigen (Livefyre-Standard oder Ihre hochgeladene benutzerdefinierte Liste) und sie zu bearbeiten. Sie können die Liste wie folgt bearbeiten:
   * Um ein Wort zu entfernen, klicken Sie auf das Wort.
   * Um ein Wort hinzuzufügen, geben Sie das Wort in das Feld **[!UICONTROL Add new word]** ein und klicken Sie auf **[!UICONTROL Return]**.
   * Um zu sehen, ob ein Wort in der Liste enthalten ist, geben Sie das Wort in das Feld **[!UICONTROL Test profanity filter]** ein.

>[!NOTE]
>
>Nur Studio-Administratoren und -Moderatoren können Profanity-Listen bearbeiten.

