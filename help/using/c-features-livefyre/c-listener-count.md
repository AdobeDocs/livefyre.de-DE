---
description: Die Listener-Anzahl ist ein Zähler, der die Anzahl der Site-Besucher für eine App auf einer Seite verfolgt und diese Zahl anzeigt.
seo-description: Die Listener-Anzahl ist ein Zähler, der die Anzahl der Site-Besucher für eine App auf einer Seite verfolgt und diese Zahl anzeigt.
seo-title: Listener-Anzahl
solution: Experience Manager
title: Listener-Anzahl
uuid: fdd7cfe4-ae69-4d31-baa2-8978368fc3e8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Listener-Anzahl{#listener-count}

Die Listener-Anzahl ist ein Zähler, der die Anzahl der Site-Besucher für eine App auf einer Seite verfolgt und diese Zahl anzeigt.

Die Listener-Anzahl ist die Anzahl der Sitebesucher, die einen Browser haben, der auf der Seite geöffnet ist, auf der eine App instanziiert wird. Auf diese Weise können Sie ermitteln, wie viele Site-Besucher sich zu einem bestimmten Zeitpunkt auf der Seite befinden, sodass Sie sie verfolgen können, während sie Streaming- oder Live-Inhalte in Echtzeit ansehen.

Der Listener-Zähler von Livefyre funktioniert wie folgt:

1. Die Site, die Ihre App enthält, pingt alle 60 Sekunden einen Livefyre-Server.
1. Der Livefyre-Server antwortet mit der Anzahl der Site-Besucher auf der Seite, auf der die App angezeigt wird (definiert als die Anzahl der Site-Besucher mit einem Browser, der auf dieser Seite geöffnet ist).
1. Die Anzahl der Site-Besucher auf der Seite mit der App wird in der App angezeigt.

Apps, die diese Funktion verwenden:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reviews](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Listener Avatar {#section_wcn_kxp_vz}

Die Listener-Anzahl zeigt maximal 10 Avatare an und zeigt nur Avatare für diejenigen Personen an, die **[!UICONTROL Follow]** für die Konversation geklickt haben.

>[!NOTE]
>
>Aufgrund von Platzbeschränkungen zeigt die mobile Oberfläche nur die Anzahl der Listener und ein kleines "Personensymbol"an.

Der Livefyre-Listener-Zähler zeigt die Anzahl der Personen an, die zu einem bestimmten Zeitpunkt aktiv auf der Seite sind, sowie die Anzahl der Personen, die der Konversation folgen. Wenn sich jemand auf der Seite befindet und der Unterhaltung folgt, wird dieser Benutzer nicht doppelt gezählt. Wenn sich ein Benutzer beispielsweise auf einer Seite befindet und klickt **[!UICONTROL Follow]**, wird die Listener-Anzahl nicht erhöht. Wenn der Benutzer dann klickt **[!UICONTROL Unfollow]**, wird die Anzahl nicht verringert.

Apps, die diese Funktion verwenden:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reviews](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

