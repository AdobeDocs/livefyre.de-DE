---
description: Auf der Registerkarte "Moderation" können Sie Vormoderationsregeln für
  eingehende Inhalte festlegen, einschließlich Abruf-Listen, Kennzeichnungsregeln
  und eingeschränkte IP-Adressen.
seo-description: Auf der Registerkarte "Moderation" können Sie Vormoderationsregeln
  für eingehende Inhalte festlegen, einschließlich Abruf-Listen, Kennzeichnungsregeln
  und eingeschränkte IP-Adressen.
seo-title: Einrichten der Moderation
solution: Experience Manager
title: Einrichten der Moderation
uuid: 0 ec 53 fdb -08 c 2-4058-88 cb -2 f 6 f 4 b 56 a 95 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Einrichten der Moderation{#setting-up-moderation}

Auf der Registerkarte "Moderation" können Sie Vormoderationsregeln für eingehende Inhalte festlegen, einschließlich Abruf-Listen, Kennzeichnungsregeln und eingeschränkte IP-Adressen.

## Funktionsweise von Moderation {#section_kyf_gvc_t1b}

Sie können Inhalte wie folgt moderieren:

* Automatisches Moderieren von Inhalten, um unerwünschter Inhalt basierend auf Regeln zu filtern, die Sie vor der Veröffentlichung des Inhalts eingerichtet haben.
* Löschen Sie manuell Inhalte, die mithilfe der automatischen Premoderation mithilfe der modq- oder App-Inhalte in der Bibliothek gekennzeichnet wurden.
* Identifizieren Sie Site-Besucher, die wiederholte Inhalte veröffentlichen, um sie von der Veröffentlichung zu halten, indem Sie bestimmte Livefyre-Benutzer, Social-Benutzer oder IP-Adressen verbieten.
* Identifizieren Sie Personen und Inhalte, die immer durch die Eingabe von Benutzern oder das Deaktivieren von Filtern für bestimmte Streams, Sites oder Netzwerke angezeigt werden können.

Sie können Inhalte auf folgende Weise automatisch vorab moderieren:

* Richten Sie Regeln ein, um bestimmte Inhaltstypen automatisch zu kennzeichnen:

   * Richten Sie Kennzeichnungsregeln für Inhalte ein, die von Besuchern der Site gekennzeichnet werden. Unter Verwendung dieser Kennzeichnung wird **[!UICONTROL Settings > Moderation > Rules]**
   * Einrichten von SAFE-Regeln mithilfe von **[!UICONTROL Settings > Moderation > Rules]**
   * Spezifischen Twitter-Benutzern die Verwendung von **[!UICONTROL Settings > Streams]**
   * IP-Adressen mithilfe von **[!UICONTROL Settings > Bans]**
   * Sperren Sie IP-Regionen nach Ländercode nach Anforderung. Verbotener Inhalt wird als SPAM markiert.

* Erstellen Sie eine Liste von Wörtern, die Sie in der Gewinn-Liste Ihres **[!UICONTROL Settings > Moderation > Rules]** Netzwerks oder Ihrer Site als Gewinn betrachten.
* Whitelist-Benutzer (zulassen, dass Inhalte von diesen Benutzern angezeigt werden), indem Sie Filter für bestimmte Streams, Sites oder Netzwerke verwenden oder deaktivieren.

Nachdem Sie Ihre Gewinnspiellisten, SAFE-Filter und Regeln eingerichtet haben, können Sie festlegen, ob Sie Inhalte vorab moderieren und die SAFE Filter in Streams anwenden möchten. Weitere Informationen finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](/help/using/c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

Livefyre markiert Inhalte als **[!UICONTROL Approved]****[!UICONTROL Pending]**, **[!UICONTROL Junk]**usw. abhängig davon, woher der Inhalt kommt, wo er veröffentlicht wird und welche Regeln Sie in Ihrem System eingerichtet haben. In der folgenden Tabelle werden die Aktionen, die Livefyre ausführt, im Detail beschrieben.

## Funktionsweise von Moderation

| Inhalt aus: | Inhalt senden an: | Genehmigungsstatus |
|--- |--- |--- |
| Bibliothek | App | Inhalt genehmigt |
| Social Search | App | Inhalt genehmigt |
| Stream-Regel | App | Ist der als "Unk" markierte Inhalt nach dem Filter" SAFE" gekennzeichnet? <br><ul><li>Nein - Stream-to-App-Moderationsarbeitsablauf</li><li>Ja - Inhalt umgebrochen</li></ul> |
| Bibliothek | Ordner | Kein Status (im Ordner, nicht veröffentlicht, nicht beschädigt) |
| Social Search | Ordner | Kein Status (im Ordner, nicht veröffentlicht, nicht beschädigt) |
| Stream-Regel | Ordner | Ist der als "Unk" markierte Inhalt nach dem Filter" SAFE" gekennzeichnet? <br><ul><li>Nein - Kein Status (im Ordner, nicht veröffentlicht, nicht umgebrochen)</li><li>Ja - Inhalt umgebrochen</li></ul> |
| App-Beitrag | App | Ist der als "Unk" markierte Inhalt nach dem Filter" SAFE" gekennzeichnet? <br><ul><li>Nein - Post-to-App-Moderationsarbeitsablauf</li><li>Ja - Inhalt umgebrochen</li></ul> |

## Stream-to-App-Moderationsarbeitsablauf {#section_z5z_w4d_t1b}

![](assets/stream_to_app_workflow.png)

Bevor der Inhalt eines Stream auf einer App veröffentlicht wird, führt Livefyre die folgenden Prüfungen durch, um festzulegen, wie mit dem Inhalt zu verfahren ist:

1. Wenn SAFE den Inhalt als unbrauchbar oder ablegt kennzeichnen, wird der Inhalt von Livefyre abgeschnitten.
1. Wenn SAFE den Inhalt nicht als unbrauchbar markiert, prüft Livefyre, ob die Premoderation aktiviert ist.
1. Wenn die Premoderation aktiviert ist, markiert Livefyre den Inhalt als ausstehend.
1. Wenn Sie modq-Regeln einrichten, sendet Livefyre den Inhalt an das modq.
1. Wenn die Premoderation nicht aktiviert ist, überprüft Livefyre, ob der Inhalt mit SAFE gekennzeichnet wurde.
1. Wenn SAFE den Inhalt markiert hat, genehmigt Livefyre den Inhalt und veröffentlicht den Inhalt der App.
1. Wenn SAFE den Inhalt markiert und Sie keine SAFE-Regeln eingerichtet haben, genehmigt Livefyre den Inhalt und veröffentlicht den Inhalt der App.
1. Wenn SAFE den Inhalt KENNZEICHNET und Sie SAFE-Regeln einrichten, prüft Livefyre, ob Sie SAFE-Regeln für den Stream einrichten.
1. Wenn Sie SAFE-Regeln für den Stream einrichten, genehmigt Livefyre den Inhalt und veröffentlicht den Inhalt der App. Wenn Sie SAFE-Regeln für den Stream nicht eingerichtet haben, verwendet Livefyre die SAFE-Regeln für die Moderation, um zu bestimmen, wie der Inhalt verarbeitet wird (senden an modq, Papierkorb usw.).

## Moderations-Workflow für Post-to-App {#section_fwn_w4d_t1b}

![](assets/post_to_app_workflow.png)

Bevor der Inhalt eines App-Beitrags in einer App veröffentlicht wird, führt Livefyre die folgenden Prüfungen durch, um festzulegen, wie mit dem Inhalt zu verfahren ist:

1. Wenn der Filter SAFE den Inhalt als Drop kennzeichnet, wird der Inhalt von Livefyre entfernt.
1. Wenn SAFE den Inhalt nicht als Drop markiert, überprüft Livefyre, ob die Premoderation aktiviert ist. Wenn die Premoderation aktiviert ist, markiert Livefyre den Inhalt als ausstehend. Wenn Sie modq-Regeln einrichten, sendet Livefyre den Inhalt als ausstehend an das modq. Falls nicht, bleibt der Inhalt in einem ausstehenden Status in der App-Inhalte in der Bibliothek.
1. Wenn die Premoderation nicht aktiviert ist, überprüft Livefyre, ob der Inhalt mit SAFE gekennzeichnet wurde. Falls nicht, genehmigt Livefyre den Inhalt und veröffentlicht den Inhalt der App.
1. Wenn SAFE den Inhalt und Sie SAFE-Regeln einrichten, verwendet Livefyre die SAFE-Regel, um zu bestimmen, wie der Inhalt verarbeitet wird (senden an modq, Papierkorb usw.). Wenn SAFE den Inhalt markiert und Sie keine SAFE-Regeln eingerichtet haben, genehmigt Livefyre den Inhalt und veröffentlicht den Inhalt der App.

## Massenfilter {#section_lyk_ktx_vy}

Der Massenfilter sucht nach wiederholten Inhalten, die in allen Livefyre-Netzwerken innerhalb eines kurzen Zeitrahmens gepostet werden. Wenn dieser Inhalt erkannt wird, wird er als Massen gekennzeichnet und standardmäßig abgeschnitten. Während Masseninhalte vom Benutzer generiert werden können (z. B. "Touchdown! » wiederholt in einem Chat während eines beliebten Football-Spiels veröffentlicht werden), werden die meisten mit Spam-Kampagnen gefüllt. Dieser Filter ist sprachunabhängig und funktioniert mit jeder Sprache. Um den Massenfilter anzupassen, müssen Sie sich an den Livefyre-Support wenden.

## Regeln {#section_gqz_ksk_f1b}

Verwenden Sie den Abschnitt Regeln, um Vorab-Moderationsregeln basierend auf SAFE- und User Applied-Flags zu erstellen. Dieses Bedienfeld bietet zwei Regeltypen:

* **[!UICONTROL Flag Rules:]** Geben Sie eine Aktion an, die bei einem von Benutzern festgelegten Kommentar für eine festgelegte Anzahl von Malen durchgeführt werden soll.
* ****[!UICONTROL SAFE Rules:]Kombinieren Sie SAFE-Flags mit Aktionen, die für den gekennzeichneten Inhalt ausgeführt werden sollen.

Um Kennzeichnungsregeln zu erstellen, markieren Sie das Flag ("Beleidigend" ," Aus Thema" , "Nicht zustimmen" oder" Spam" ), geben Sie an, wie oft es auf einen Inhalt angewendet werden soll, und wählen Sie die gewünschte Aktion aus. Sie können eine Flag-Regel für jede Flag-Option festlegen (Beleidigend, Aus-Thema, Nicht zustimmen oder Spam).

Sie können Regeln auf Netzwerk-, Site- und Stream-Ebenen erstellen. Regeln auf Site-Ebene übernehmen Netzwerkregeln, es sei denn, Sie konfigurieren Site-Regeln unterschiedlich. Stream-Regeln übernehmen Site-Regeln, es sei denn, Sie konfigurieren sie unterschiedlich.

Verfügbare Aktionen:

* ****[!UICONTROL Trash it:]sendet den gekennzeichneten Kommentar an den Papierkorb.
* **[!UICONTROL Bozo it:]** verbirgt den markierten Kommentar von allen Benutzern mit Ausnahme des Autors, der sichtbar bleibt.
* **[!UICONTROL Pending:]** legt den Inhalt als ausstehend fest. Wenn Sie die Option "Premoderation" unter aktivieren, **[!UICONTROL Settings > ModQ]**wird sie im modq angezeigt. Andernfalls wird es nur in App-Inhalten angezeigt.

>[!NOTE]
>
>Livefyre empfiehlt, Regeln für Bozo-Kommentare zu erstellen, die von fünf Benutzern als Spam oder Offensive gekennzeichnet werden.

## Moderationsempfehlungen {#section_ec3_vr3_2cb}

Sie können Moderationsempfehlungen verwenden, um zu bestimmen, wie Sie Inhalte moderieren, die von Site-Besuchern in Livefyre-Apps gepostet werden. Der Indikator für die Moderation empfiehlt, dass ein Inhaltselement basierend auf den Aktionen, die Sie zuvor bei ähnlichen Inhalten ausgeführt haben, umgangen wird. So verwenden Sie Moderationsempfehlungen:

1. Aktivieren Sie die Funktion Moderation Recommendations, indem Sie sich an Ihren Adobe Livefyre-Support wenden.
1. Richten Sie Moderationsempfehlungen in den Netzwerkeinstellungen ein.

   Richten Sie die Moderationsempfehlungen unter Verwendung der **[!UICONTROL Livefyre Recommends Trash]** Einstellung unter ein **[!UICONTROL Network Settings]**.

   ![](assets/image_mod_reco_trash.png)

1. Richten Sie eine SAFE-Regel ein, um Livefyre anzugeben, was mit Inhalten geschehen soll, die die Moderationsempfehlung als Inhalt bezeichnet, der wahrscheinlich umgebrochen wird. Weitere Informationen zum Einrichten einer SAFE-Regel für die **[!UICONTROL Livefyre Recommends Trash]** Option finden Sie unter [Moderation](/help/using/c-features-livefyre/c-about-moderation/c-moderation.md#c_moderation).

   ![](assets/modreco4.png)

1. Verwenden Sie das **[!UICONTROL Moderation Recommendation Indicator]** Modul "modq" oder" App-Inhalt" , um Inhalte zu filtern, die die Moderationsempfehlung so häufig vertrastet.

   In modq sieht der Indikator wie folgt aus: ![](assets/mod_reco1.png)

   Weitere Informationen zur Verwendung von Moderationsempfehlungen zum Moderieren von Inhalten in modq finden Sie unter [modq](/help/using/c-features-livefyre/c-about-moderation/c-modq.md#c_modq).

   In App-Inhalten sehen Moderationsempfehlungen wie folgt aus: ![](assets/modreco3.png)

   Weitere Informationen zur Verwendung von Moderationsempfehlungen in App Content finden Sie unter [Moderieren von Inhalten mit App-Inhalten](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).
