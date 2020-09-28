---
description: Erfahren Sie mehr über die Lebenszykluskonventionen und die Organisation von Inhalten in Livefyre.
seo-description: Erfahren Sie mehr über die Lebenszykluskonventionen und die Organisation von Inhalten in Livefyre.
seo-title: Architektur
solution: Experience Manager
title: Architektur
uuid: 94358e6c-954a-4a52-9bb2-d800b2933130
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Architektur{#architecture}

Erfahren Sie mehr über die Lebenszykluskonventionen und die Organisation von Inhalten in Livefyre.

Dieser Abschnitt bietet einen Überblick über die Livefyre-Netzwerkarchitektur.

## Übersicht über Netzwerke und Sites

Livefyre organisiert Benutzer und Inhalte nach Netzwerk und Website. Jedem Netzwerk kann ein oder mehrere Benutzerkonten zugeordnet sein, und jedes Netzwerk kann eine oder mehrere Livefyre-Sites umfassen. Eine Livefyre-Site ist eine beliebige Gruppierung von Sammlungen. Eine Sammlung ist einer Artikel-ID in Ihrem CMS zugeordnet.

## Netzwerke verstehen {#section_hqt_4m4_xz}

Kunden mit mehreren Domänen können Benutzerkonten über ein einziges Livefyre-Netzwerk für alle Domänen freigeben. Kunden, die separate Benutzerkonten für verschiedene Domänen führen möchten, benötigen separate Livefyre-Netzwerke.

Konfigurationseinstellungen können auf Sites, Netzwerke und Sammlungen angewendet werden (in der Abbildung oben als Konversation bezeichnet).

>[!NOTE]
>
>Einige Einstellungen stehen nur auf Netzwerkebene zur Verfügung (z. B. Voreinstellungen für E-Mail-Benachrichtigungen, E-Mail-Adresse und benutzerdefinierte E-Mail-Logos). Wenn diese Einstellungen für jede Domäne unterschiedlich sein sollen, müssen Sie mehrere Netzwerke verwenden.

## Sites verstehen {#section_vjw_nm4_xz}

Eine Site ist eine beliebige Gruppierung von Artikeln. Die Gruppierung ist nützlich, da Sie verschiedene Moderatoren verschiedenen Inhaltsgruppen zuweisen können. Moderatoren und Eigentümer können so eingerichtet werden, dass Inhalte moderiert und die Admin-Einstellungen entweder auf Netzwerk- oder Site-Ebene konfiguriert werden. Wenn Sie möchten, dass einige Moderatoren nur bestimmte Sammlungen sehen, können diese Sammlungen als separate Livefyre-Site eingerichtet werden.

>[!NOTE]
>
>Die Anzahl der Sites, die Sie unter Ihrem benutzerspezifischen Netzwerk haben, ist unbegrenzt.

## App-Sequenzdiagramm {#section_mw2_lm4_xz}

Unabhängig davon, ob Sie benutzerdefinierte Funktionen mit Livefyre-bereitgestellten Endpunkten implementieren möchten oder einfach ein Problem debuggen müssen, hilft es, zu verstehen, wie der Livefyre-App-Anforderungs-/Antwortfluss funktioniert.

![](assets/appsequencediagram.png)

1. Wenn Ihr Kunde Ihre Site aufruft, instanziieren Sie die Livefyre-App mit der Site-ID und der Artikel-ID.
1. Wenn Sie den Benutzer authentifizieren möchten (nützlich für die Traffic-Auswertung sowie für den Site-Schutz), senden Sie Livefyre die Site-Informationen und das Benutzerprofil-Token.
1. Senden Sie Livefyre die Site-ID und die Artikel-ID, um die App zu initialisieren.

   Livefyre gibt den anfänglichen Inhalt zurück.

   Senden Sie diesen Inhalt an die Seite und zeigen Sie die App an.

1. Um auf der Seite angezeigte Inhalte zu aktualisieren, senden Sie Livefyre die neueste Ereignis-ID von Ihrer Seite. Wenn neue Inhalte verfügbar sind, werden sie zurückgegeben.

   Laden Sie Ihre Seite mit neuem Inhalt neu und wiederholen Sie den Vorgang unbegrenzt.

1. Wenn Sie zulassen, dass Benutzer neue Inhalte posten, lösen Sie ein Ereignis aus, wenn neue Inhalte auf Ihrer Site veröffentlicht werden, um die Inhalte an Livefyre zu veröffentlichen. Livefyre gibt einen aktualisierten Stream zurück, den Sie zur Aktualisierung Ihrer Site verwenden können.
