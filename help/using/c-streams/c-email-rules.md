---
description: Sie können Stream-Regeln erstellen, die Inhalte aus der E-Mail abrufen.
seo-description: Sie können Stream-Regeln erstellen, die Inhalte aus der E-Mail abrufen.
seo-title: E-Mail-Regeln
solution: Experience Manager
title: E-Mail-Regeln
uuid: 3cd27d28-b7c0-4cbc-bae3-e2ef7beacba9
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# E-Mail-Regeln{#email-rules}

Sie können Stream-Regeln erstellen, die Inhalte aus der E-Mail abrufen.

Mit E-Mail-basierten Streams können Sie Inhalte per E-Mail direkt in einer App oder einem Ordner veröffentlichen.

Verwenden Sie diese Funktion, damit Mitarbeiter von ihrem Computer oder Mobilgerät aus direkt in Ihre Apps oder Asset Library posten können.

Sobald die Regel erstellt wurde, wird jede E-Mail, die ein Bild oder eine Videodatei enthält, die an die angegebene E-Mail-Adresse gesendet wird, wie angegeben direkt in Ihrer App oder Asset-Bibliothek veröffentlicht. E-Mails, die mit mehreren Anlagen gesendet werden, werden alle Dateien an den entsprechenden Speicherort senden. E-Mails, die an die angegebene Adresse gesendet werden, die nur Text enthält, haben nichts zu tun.

Nach dem Senden werden die Felder der E-Mail zum Ausfüllen der folgenden Elemente für den Inhalt verwendet:

* **[!UICONTROL From:]** Wird als Autor des Inhalts verwendet, wenn das Benutzerkonto vorhanden ist. Wenn für den Absender kein Konto vorhanden ist, wird der Autor als anonym aufgeführt.
* **[!UICONTROL Subject:]** Wird für den Titel des Inhalts verwendet.
* **[!UICONTROL Body:]** Dient zum Ausfüllen von Inhaltsdetails in Studio.
* **[!UICONTROL Attachments:]** Mediendateien müssen angehängt werden, sonst wird die E-Mail ignoriert. Zu den unterstützten Dateitypen gehören 3GP, ASF, AVI, DV, GIF, JPG, MOV, MP4, MPEG, MPG, PNG, QT und WMV. Die Gesamtanzahl aller Anlagen muss unter der Dateigröße von 25 MB liegen.

Weitere Stream-Regeloptionen für alle Stream-Regeln finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
