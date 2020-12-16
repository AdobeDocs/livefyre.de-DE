---
description: 'null '
seo-description: 'null '
seo-title: Smart-Tags
title: Smart-Tags
uuid: f978fa83-e79b-46ae-bb3e-0f9449bd0440
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Smart Tags{#smart-tags}

Livefyre verwendet die Adobe Sensei-Computer-Vision-Technologie, um automatisch Bilder und Videos zu taggen, die Sie in der Bibliothek speichern oder hochladen.

Mit intelligenten Tags sparen Sie Zeit, verwalten, suchen und kuratieren Inhalte. Mit intelligenten Tags können Sie:

* Suchen Sie gespeicherte und hochgeladene Bilder und Videos nach genauem Inhalt basierend auf dem Bild- und Videoinhalt und nicht nur nach Text
* Erfassen von Inhalten in Streams basierend auf genauen Suchbegriffen, die das Bild oder Video analysieren, statt nur Text

Wenn Sie ein Bild oder Video speichern oder hochladen, prüft Adobe Sensei den Inhalt automatisch und markiert ihn mit 135.000 Klassifizierern in drei Kategorien:

* Funktionen (z. B. Katzen, Hunde, Pyramiden, Wahrzeichen)
* Kategorien (z. B. Reisen, Tourismus, Schönheit)
* Ästhetische Eigenschaften (z. B. Bildqualität, Drittanbieter-Regeln)
* SFW/NSFW (damit können Sie automatisch NSFW Bilder filtern, um die Sicherheit Ihrer Streams und UGC-Bibliothek zu verbessern.

Der Rang-Algorithmus für intelligente Tags Filter Inhalte mit einem intelligenten Tag-Konfidenzwert, wie neu der Inhalt ist und wie viele Sterne ein Benutzer den Inhalt gegeben hat.

**Smart-Tags für Videos**

Funktionsdetails:

* Intelligente Tags werden auf die Videoformate MP4, .avi und .mov angewendet.
* Die maximale Dauer für unterstützte Videos beträgt 60 Sekunden oder 50 MB
* Smart-Tags stehen in der Social-Suche, in Streams und in der Bibliothek in der Bibliothek zur Verfügung.

Tagtypen:

* Feature-Tags: Funktioniert genauso wie Feature-Tags für Bilder (z. B. Katzen, Hunde, Pyramiden, Landmarks).
* Action-Tags: Identifizieren Sie Funktionen, die über mehrere Frames hinweg auftreten, anstatt nur eine. Diese sind bei der Zusammenfassung des Videoinhalts effektiver.

Weitere Informationen zu intelligenten Tags finden Sie unter [Stream-Regeloptionen für alle Stream-Regeln](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
