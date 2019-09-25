---
description: Auf der Registerkarte "Moderation"können Sie Vormoderationsregeln für eingehende Inhalte festlegen, einschließlich Profitabilität, Flag-Regeln und verbotenen IP-Adressen.
seo-description: Auf der Registerkarte "Moderation"können Sie Vormoderationsregeln für eingehende Inhalte festlegen, einschließlich Profitabilität, Flag-Regeln und verbotenen IP-Adressen.
seo-title: Einrichten der Moderation
solution: Experience Manager
title: Einrichten der Moderation
uuid: 0ec53fdb-08c2-4058-88cb-2f6f4b56a95b
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Einrichten der Moderation{#setting-up-moderation}

Auf der Registerkarte "Moderation"können Sie Vormoderationsregeln für eingehende Inhalte festlegen, einschließlich Profitabilität, Flag-Regeln und verbotenen IP-Adressen.

## Funktionsweise der Moderation {#section_kyf_gvc_t1b}

Sie können Inhalte wie folgt moderieren:

* Automatisches Vormoderieren von Inhalten, um unerwünschte Inhalte basierend auf Regeln auszufiltern, die Sie vor der Veröffentlichung des Inhalts eingerichtet haben.
* Löschen oder genehmigen Sie Inhalte, die mit der automatischen Vormoderation unter Verwendung von ModQ- oder App-Inhalten in der Bibliothek gekennzeichnet wurden.
* Identifizieren Sie Site-Besucher, die wiederholt anstößige Inhalte veröffentlichen, um zu verhindern, dass diese veröffentlicht werden, indem Sie bestimmte Livefyre-Benutzer, soziale Benutzer oder IP-Adressen verbieten.
* Identifizieren Sie Personen und Inhalte, die immer angezeigt werden können, indem Sie Benutzer in der Positivliste registrieren oder Filter für bestimmte Streams, Sites oder Netzwerke deaktivieren.

Sie können Inhalte wie folgt automatisch vormoderieren:

* Richten Sie Regeln ein, um bestimmte Inhaltstypen automatisch zu kennzeichnen:

   * Richten Sie Flag-Regeln für Inhalte ein, die durch das Flag der Site-Besucher mit **[!UICONTROL Settings > Moderation > Rules]**
   * Einrichten von SAFE-Regeln mithilfe von **[!UICONTROL Settings > Moderation > Rules]**
   * Verbieten Sie bestimmten Twitter-Benutzern die Verwendung von **[!UICONTROL Settings > Streams]**
   * IP-Adressen mit **[!UICONTROL Settings > Bans]**
   * IP-Regionen nach Ländercode auf Anfrage verbieten Verbotene Inhalte werden als SPAM gekennzeichnet.

* Erstellen Sie eine Liste der Wörter, die Sie als gewinnbringend erachten, in der Liste "Profitabilität"unter **[!UICONTROL Settings > Moderation > Rules]** Netzwerk oder Site.
* Whitelist-Benutzer (erlauben Sie immer, dass Inhalte von diesen Benutzern angezeigt werden), indem Sie Filter für bestimmte Streams, Sites oder Netzwerke verwenden oder deaktivieren.

Nachdem Sie Ihre Profillisten, SAFE-Filter und Regeln eingerichtet haben, können Sie festlegen, ob Inhalte vormoderiert werden sollen, und die SAFE-Filter in Streams anwenden. Weitere Informationen finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](/help/using/c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

Livefyre kennzeichnet Inhalt als **[!UICONTROL Approved]**, **[!UICONTROL Pending]**, **[!UICONTROL Junk]** usw. abhängig davon, woher der Inhalt stammt, wo er veröffentlicht wird und welche Regeln Sie in Ihrem System eingerichtet haben. Die folgende Tabelle beschreibt ausführlich die Aktionen, die Livefyre je nach diesen Faktoren ausführt.

## Funktionsweise der Moderation

| Inhalt stammt aus: | Senden von Inhalten an: | Genehmigungsstatus |
|--- |--- |--- |
| Bibliothek | App | Genehmigte Inhalte |
| Social-Suche | App | Genehmigte Inhalte |
| Stream-Regel | App | Ist Inhalt durch den SAFE-Filter als unbrauchbar markiert? <br><ul><li>Nein - Arbeitsablauf für die Aktualisierung von Stream zu App</li><li>Ja - Inhalte als Papierkorb</li></ul> |
| Bibliothek | Ordner | Kein Status (im Ordner, nicht veröffentlicht, nicht abgeschnitten) |
| Social-Suche | Ordner | Kein Status (im Ordner, nicht veröffentlicht, nicht abgeschnitten) |
| Stream-Regel | Ordner | Ist Inhalt durch den SAFE-Filter als unbrauchbar markiert? <br><ul><li>Nein - Kein Status (im Ordner, nicht veröffentlicht, nicht abgeschnitten)</li><li>Ja - Inhalte als Papierkorb</li></ul> |
| App-Beitrag | App | Ist Inhalt durch den SAFE-Filter als unbrauchbar markiert? <br><ul><li>Nein - Moderationsarbeitsablauf nach der App</li><li>Ja - Inhalte als Papierkorb</li></ul> |

## Arbeitsablauf für die Aktualisierung von Stream zu App {#section_z5z_w4d_t1b}

![](assets/stream_to_app_workflow.png)

Bevor der Inhalt eines Streams in einer App veröffentlicht wird, führt Livefyre die folgenden Prüfungen durch, um festzustellen, was mit dem Inhalt zu tun ist:

1. Wenn SAFE den Inhalt als Junk oder Drop kennzeichnet, wird der Inhalt von Livefyre abgeschnitten.
1. Wenn SAFE den Inhalt nicht als "junk"kennzeichnet, prüft Livefyre, ob die Vormoderation aktiviert ist.
1. Ist die Vormoderation aktiviert, markiert Livefyre den Inhalt als ausstehend.
1. Wenn Sie ModQ-Regeln einrichten, sendet Livefyre den Inhalt an ModQ.
1. Ist die Vormoderation nicht aktiviert, prüft Livefyre, ob der Inhalt mit SAFE gekennzeichnet wurde.
1. Wenn SAFE den Inhalt markiert hat, genehmigt Livefyre den Inhalt und veröffentlicht ihn in der App.
1. Wenn SAFE den Inhalt kennzeichnet und Sie keine SAFE-Regeln eingerichtet haben, genehmigt Livefyre den Inhalt und veröffentlicht ihn in der App.
1. Wenn SAFE den Inhalt kennzeichnet und Sie SAFE-Regeln einrichten, prüft Livefyre, ob Sie SAFE-Regeln für den Stream eingerichtet haben.
1. Wenn Sie SAFE-Regeln für den Stream einrichten, genehmigt Livefyre den Inhalt und veröffentlicht ihn in der App. Wenn Sie keine SAFE-Regeln für den Stream eingerichtet haben, verwendet Livefyre die Moderations-SAFE-Regeln, um zu bestimmen, wie der Inhalt zu behandeln ist (Senden an ModQ, Papierkorb usw.).

## Moderationsarbeitsablauf nach der App {#section_fwn_w4d_t1b}

![](assets/post_to_app_workflow.png)

Bevor der Inhalt eines App-Beitrags in einer App veröffentlicht wird, führt Livefyre die folgenden Prüfungen durch, um festzustellen, was mit dem Inhalt zu tun ist:

1. Wenn der SAFE-Filter den Inhalt als Dropdown kennzeichnet, wird der Inhalt von Livefyre abgelegt.
1. Wenn SAFE den Inhalt nicht als "drop"kennzeichnet, prüft Livefyre, ob die Vormoderation aktiviert ist. Ist die Vormoderation aktiviert, markiert Livefyre den Inhalt als ausstehend. Wenn Sie ModQ-Regeln einrichten, sendet Livefyre den Inhalt als ausstehend an ModQ. Ist dies nicht der Fall, bleibt der Inhalt in der Bibliothek in einem ausstehenden Status in App-Inhalt.
1. Ist die Vormoderation nicht aktiviert, prüft Livefyre, ob der Inhalt mit SAFE gekennzeichnet wurde. Andernfalls genehmigt Livefyre den Inhalt und veröffentlicht ihn in der App.
1. Wenn SAFE den Inhalt kennzeichnet und Sie SAFE-Regeln einrichten, verwendet Livefyre die SAFE-Regel, um zu bestimmen, wie der Inhalt zu behandeln ist (Senden an ModQ, Papierkorb usw.). Wenn SAFE den Inhalt kennzeichnet und Sie keine SAFE-Regeln eingerichtet haben, genehmigt Livefyre den Inhalt und veröffentlicht ihn in der App.

## Massenfilter {#section_lyk_ktx_vy}

Der Massenfilter sucht innerhalb kurzer Zeit nach wiederholten Inhalten, die in allen Livefyre-Netzwerken veröffentlicht werden. Wenn dieser Inhalt erkannt wird, wird er standardmäßig als "Massen"gekennzeichnet und anschließend als Absturz verwendet. Masseninhalte können vom Benutzer generiert werden (z. B. "Touchdown!") wiederholt in einem Chat während eines beliebten Fußballspiels veröffentlicht), entstehen die meisten mit Spam-Kampagnen. Dieser Filter ist sprachunabhängig und funktioniert in jeder Sprache. Um den Massenfilter anzupassen, müssen Sie sich an den Livefyre-Support wenden.

## Regeln {#section_gqz_ksk_f1b}

Verwenden Sie den Abschnitt Regeln, um Vormoderationsregeln basierend auf SAFE und vom Benutzer angewendeten Flags zu erstellen. Dieses Bedienfeld bietet zwei Regeltypen:

* **[!UICONTROL Flag Rules:]** Geben Sie eine Aktion an, die für einen Kommentar ausgeführt werden soll, der von Benutzern mit einer bestimmten Anzahl von Malen gekennzeichnet wird.
* **[!UICONTROL SAFE Rules:]** SAFE-Flags mit Aktionen kombinieren, die für den gekennzeichneten Inhalt durchgeführt werden.

Um Flaggenregeln zu erstellen, wählen Sie das Flag (Offensiv, Off Topic, Uneinigkeit oder Spam), geben Sie an, wie oft es auf einen Inhalt angewendet werden muss, und wählen Sie die gewünschte Aktion aus. Sie können für jede Flag-Option eine Flag-Regel festlegen (Offensive, Off-Thema, Uneinigkeit oder Spam).

Sie können Regeln auf Netzwerk-, Site- und Stream-Ebene erstellen. Regeln auf Site-Ebene übernehmen Netzwerkregeln, es sei denn, Sie konfigurieren Site-Regeln anders. Stream-Regeln übernehmen Site-Regeln, es sei denn, Sie konfigurieren sie anders.

Verfügbare Aktionen:

* **[!UICONTROL Trash it:]**sendet den markierten Kommentar zum Papierkorb.
* **[!UICONTROL Bozo it:]** Blendet den gekennzeichneten Kommentar für alle Benutzer mit Ausnahme des Autors aus, für den er sichtbar bleibt.
* **[!UICONTROL Pending:]** stellt den Inhalt als ausstehend ein. Wenn Sie unter "Vormoderation"auf "ON"einstellen **[!UICONTROL Settings > ModQ]**, wird sie im ModQ angezeigt. Andernfalls wird es nur in App-Inhalten angezeigt.

>[!NOTE]
>
>Livefyre empfiehlt, Regeln für Bozo-Kommentare zu erstellen, die von fünf Benutzern als Spam oder Offensive gekennzeichnet werden.

## Moderationsempfehlungen {#section_ec3_vr3_2cb}

Sie können Moderationsempfehlungen verwenden, um festzustellen, wie Inhalte von Site-Besuchern in Livefyre-Apps moderiert werden. Der Indikator für die Moderationsempfehlung empfiehlt, dass ein Inhaltselement basierend auf den Aktionen, die Sie zuvor zu ähnlichen Inhalten durchgeführt haben, wahrscheinlich abgeschnitten wird. So verwenden Sie Moderationsempfehlungen:

1. Schalten Sie die Moderation Recommendations-Funktion ein, indem Sie sich an Ihren Adobe Livefyre-Supportmitarbeiter wenden.
1. Richten Sie Moderationsempfehlungen in den Netzwerkeinstellungen ein.

   Richten Sie Moderationsempfehlungen mit der **[!UICONTROL Livefyre Recommends Trash]** Einstellung unter **[!UICONTROL Network Settings]**.

   ![](assets/image_mod_reco_trash.png)

1. Richten Sie eine SAFE-Regel ein, um Livefyre mitzuteilen, was mit Inhalten zu tun ist, die von der Moderationsempfehlung als Inhalt identifiziert werden, der wahrscheinlich abgeschnitten wird. Weitere Informationen zum Einrichten einer SAFE-Regel für die **[!UICONTROL Livefyre Recommends Trash]** Option finden Sie unter [Moderation](/help/using/c-features-livefyre/c-about-moderation/c-moderation.md#c_moderation).

   ![](assets/modreco4.png)

1. Verwenden Sie die **[!UICONTROL Moderation Recommendation Indicator]** im ModQ oder im App-Inhalt, um Inhalte zu filtern, die von der Moderationsempfehlung als mit Abstürzen wahrscheinlich identifiziert werden.

   In ModQ sieht der Indikator wie folgt aus:  ![](assets/mod_reco1.png)

   Weitere Informationen zur Verwendung von Moderationsempfehlungen zum Moderieren von Inhalten in ModQ finden Sie unter [ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md#c_modq).

   In App-Inhalten sehen Moderationsempfehlungen wie folgt aus:  ![](assets/modreco3.png)

   Weitere Informationen zur Verwendung von Moderationsempfehlungen in App-Inhalten finden Sie unter [Moderieren von Inhalten mit App-Inhalten](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).
