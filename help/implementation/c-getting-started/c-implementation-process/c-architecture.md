---
description: Erfahren Sie mehr über Livefyre-Konventionen und wie Livefyre Inhalte
  organisiert.
seo-description: Erfahren Sie mehr über Livefyre-Konventionen und wie Livefyre Inhalte
  organisiert.
seo-title: Architektur
solution: Experience Manager
title: Architektur
uuid: 94358 e 6 c -954 a -4 a 52-9 bb 2-d 800 b 2933130
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Architektur{#architecture}

Erfahren Sie mehr über Livefyre-Konventionen und wie Livefyre Inhalte organisiert.

Dieser Abschnitt bietet einen Überblick über die Livefyre-Netzwerkarchitektur.

## Übersicht über Netzwerke und Sites

Livefyre organisiert Benutzer und Inhalte nach Netzwerk und Site. Jedem Netzwerk können ein oder mehrere Benutzerkonten zugeordnet sein, und jedes Netzwerk kann mindestens eine Livefyre-Site enthalten. Eine Livefyre-Site ist eine beliebige Gruppierung von Sammlungen. Eine Sammlung wird einer Artikel-ID in Ihrem CMS zugeordnet.

## Netzwerke verstehen {#section_hqt_4m4_xz}

Kunden mit mehreren Domänen können Benutzerkonten über ein einzelnes Livefyre-Netzwerk für alle Domänen freigeben. Kunden, die separate Benutzerkonten für verschiedene Domänen behalten möchten, benötigen separate Livefyre-Netzwerke.

Konfigurationseinstellungen können auf Sites, Netzwerke und Sammlungen angewendet werden (in der Abbildung oben als Unterhaltung bezeichnet).

>[!NOTE]
>
>Einige Einstellungen sind nur auf Netzwerkebene verfügbar (z. B. Voreinstellungen für E-Mail-Benachrichtigungen, E-Mail von Adressen und E-Mail-Logos). Wenn diese Einstellungen für jede Domäne unterschiedlich sein sollen, müssen Sie mehrere Netzwerke verwenden.

## Sites {#section_vjw_nm4_xz}

Eine Site ist eine beliebige Gruppierung von Artikeln. Die Gruppierung ist nützlich, da sie verschiedenen Inhaltsgruppen unterschiedliche Moderatoren zuweisen kann. Moderatoren und Inhaber können eingerichtet werden, um Inhalte moderieren und Admin-Einstellungen entweder auf dem Netzwerk oder auf der Site-Ebene konfigurieren zu können. Wenn einige Moderatoren nur bestimmte Sammlungen sehen sollen, können diese Sammlungen als separate Livefyre-Site eingerichtet werden.

>[!NOTE]
>
>Die Anzahl der Sites, die Sie möglicherweise über Ihr benutzerdefiniertes Netzwerk verfügen, ist unbegrenzt.

## App-Sequenzdiagramm {#section_mw2_lm4_xz}

Unabhängig davon, ob Sie eine benutzerdefinierte Funktion mit Livefyre-Bereitstellungsendpunkten implementieren möchten oder einfach ein Problem debuggen müssen, hilft es Ihnen zu verstehen, wie der Livefyre-App-Anforderungs-/Antwortfluss funktioniert.

![](assets/appsequencediagram.png)

1. Wenn Ihr Client Ihre Site aufruft, instanziieren Sie die Livefyre-App mit der Site-ID und der Artikel-ID.
1. Wenn Sie den Benutzer authentifizieren möchten (sowohl für die Traffic-Bewertung als auch für den Site-Schutz), senden Sie Livefyre die Site-Informationen und das Benutzerprofil-Token.
1. Senden Sie Livefyre die Site-ID und die Artikel-ID, um die App zu initialisieren.

   Livefyre gibt den anfänglichen Inhalt zurück.

   Senden Sie diesen Inhalt an die Seite und zeigen Sie die App an.

1. Um die auf der Seite angezeigten Inhalte zu aktualisieren, senden Sie Livefyre an die neueste Ereignis-ID von Ihrer Seite. Wenn ein neuer Inhalt verfügbar ist, wird er zurückgegeben.

   Laden Sie Ihre Seite mit neuem Inhalt neu und wiederholen Sie den Prozess unbegrenzt.

1. Wenn Sie zulassen, dass Benutzer neue Inhalte posten, lösen Sie ein Ereignis aus, wenn neue Inhalte auf Ihrer Site veröffentlicht werden, um den Inhalt auf Livefyre zu veröffentlichen. Livefyre gibt einen aktualisierten Stream zurück, mit dem Sie Ihre Site aktualisieren können.
