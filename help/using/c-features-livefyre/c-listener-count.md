---
description: Die Anzahl der Listener ist ein Zähler, der die Anzahl der Site-Besucher für eine App auf einer Seite verfolgt und diese Zahl anzeigt.
seo-description: Die Anzahl der Listener ist ein Zähler, der die Anzahl der Site-Besucher für eine App auf einer Seite verfolgt und diese Zahl anzeigt.
seo-title: Listener-Anzahl
solution: Experience Manager
title: Listener-Anzahl
uuid: fdd 7 cfe 4-ae 69-4 d 31-baa 2-8978368 fc 3 e 8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Listener-Anzahl{#listener-count}

Die Anzahl der Listener ist ein Zähler, der die Anzahl der Site-Besucher für eine App auf einer Seite verfolgt und diese Zahl anzeigt.

Die Listener-Anzahl ist die Anzahl der Site-Besucher, die einen Browser geöffnet haben, der auf der Seite geöffnet ist, auf der eine App instanziiert wird. So können Sie erkennen, wie viele Site-Besucher zu jeder Zeit auf der Seite sind, sodass Sie sie verfolgen können, während sie Streaming- oder Live-Inhalte in Echtzeit ansehen.

Die Listener-Anzahl von Livefyre funktioniert wie folgt:

1. Die Site mit Ihrer App pings alle 60 Sekunden einen Livefyre-Server.
1. Der Livefyre-Server antwortet mit der Anzahl der Site-Besucher auf der Seite, die die App anzeigt (definiert als Anzahl der Site-Besucher mit einem auf dieser Seite geöffnet Browser).
1. Die Anzahl der Site-Besucher auf der Seite mit der App wird in der App angezeigt.

Apps, die diese Funktion verwenden:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reviews](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## Listener Avatare {#section_wcn_kxp_vz}

Die Listener-Anzahl zeigt maximal 10 Avatare an und zeigt Avatare nur für die Personen an, die auf die Unterhaltung geklickt haben **[!UICONTROL Follow]** .

>[!NOTE]
>
>Aufgrund von Leerzeichen zeigt die mobile Oberfläche nur die Anzahl der Listener und ein kleines Symbol &quot;Personen&quot; an.

Die Livefyre-Listener-Anzahl zeigt die Anzahl der Personen an, die zu jeder Zeit aktiv auf der Seite auf der Seite sind, sowie die Anzahl der Personen, die nach der Konversation folgen. Wenn sich jemand auf der Seite befindet und der Unterhaltung folgen, wird dieser Benutzer nicht doppelt gezählt. Wenn sich ein Benutzer beispielsweise auf einer Seite und in Klicks **[!UICONTROL Follow]** befindet, wird die Listener-Anzahl nicht erhöht. Wenn dieser Benutzer dann klickt **[!UICONTROL Unfollow]**, wird die Anzahl nicht verringert.

Apps, die diese Funktion verwenden:

* [Chat](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Kommentare](/help/using/c-about-apps/c-comments/c-comments.md)
* [Reviews](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

