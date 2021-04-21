---
description: Die Listener-Anzahl ist ein Zähler, der die Anzahl der Site-Besucher für eine App auf einer Seite verfolgt und diese Anzahl anzeigt.
title: Listener-Anzahl
exl-id: a07e83c2-7465-42ec-9d24-821aac5ab74b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---

# Listener-Anzahl{#listener-count}

Die Listener-Anzahl ist ein Zähler, der die Anzahl der Site-Besucher für eine App auf einer Seite verfolgt und diese Anzahl anzeigt.

Listener Count ist die Anzahl der Site-Besucher, auf denen ein Browser geöffnet ist, um die Seite zu öffnen, auf der eine App instanziiert wird. Auf diese Weise können Sie ermitteln, wie viele Site-Besucher sich zu einem bestimmten Zeitpunkt auf der Seite befinden, sodass Sie sie verfolgen können, während sie Streaming- oder Live-Inhalte in Echtzeit ansehen.

Der Listener-Zähler von Livefyre funktioniert wie folgt:

1. Die Site, die Ihre App enthält, pingt alle 60 Sekunden einen Livefyre-Server.
1. Der Livefyre-Server antwortet mit der Anzahl der Site-Besucher auf der Seite, auf der die App angezeigt wird (definiert als die Anzahl der Site-Besucher mit einem Browser, der auf dieser Seite geöffnet ist).
1. Die Anzahl der Site-Besucher auf der Seite mit der App wird in der App angezeigt.

Apps, die diese Funktion verwenden:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reviews](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Listener Avatars {#section_wcn_kxp_vz}

Der Listener-Zähler zeigt maximal 10 Avatare an und zeigt nur Avatare für diejenigen Personen an, die für die Konversation auf **[!UICONTROL Follow]** geklickt haben.

>[!NOTE]
>
>Aufgrund von Platzbeschränkungen zeigt die mobile Oberfläche nur die Anzahl der Listener und ein kleines &quot;Personensymbol&quot;an.

Der Livefyre-Listener-Zähler zeigt die Anzahl der Personen an, die zu einem bestimmten Zeitpunkt aktiv auf der Seite sind, sowie die Anzahl der Personen, die der Konversation folgen. Wenn sich jemand auf der Seite befindet und der Unterhaltung folgt, wird dieser Benutzer nicht als Dublette gezählt. Wenn sich ein Benutzer beispielsweise auf einer Seite befindet und auf **[!UICONTROL Follow]** klickt, wird die Listener-Anzahl nicht erhöht. Wenn der Benutzer dann auf **[!UICONTROL Unfollow]** klickt, wird die Anzahl nicht verringert.

Apps, die diese Funktion verwenden:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reviews](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)
