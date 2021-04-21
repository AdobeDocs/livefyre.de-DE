---
description: Nicht jeder Tweet, der mit einer Regel übereinstimmt, wird in einem Stream angezeigt.
title: Einschränkungen und Häufigkeit von Tweets
exl-id: 6b963f8a-1b61-4252-866b-567d7f556aca
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Einschränkungen und Häufigkeit von Tweets{#throttling-and-frequency-of-tweets}

Nicht jeder Tweet, der mit einer Regel übereinstimmt, wird in einem Stream angezeigt.

Die Einschränkungen von twitter-Regeln und Twitter-Feed-Unterbrechungen können die Anzahl der im Stream sichtbaren Tweets einschränken.

>[!NOTE]
>
>Um sicherzustellen, dass bestimmte Tweets in Ihrem Stream enthalten sind, verwenden Sie die Option &quot;Asset hochladen&quot;auf der Seite &quot;Alle Assets&quot;.

* Twitter erzwingt die Drosselung von Inhalten, wobei alle 5 Sekunden 1 Tweet pro Regel abgerufen wird. Dadurch können Inhalte in Livefyre-Apps ausgeglichener dargestellt werden und nicht mit Tweets überlastet werden. Die Beschränkung eingehender Tweets auf diese Weise trägt auch dazu bei, zu verhindern, dass der Stream während hoher Traffic-Zeiten überschwemmt oder unleserlich wird.

   >[!NOTE]
   >
   >Um sicherzustellen, dass der Inhalt Ihrer hochwertigen Autoren in Ihren Apps angezeigt wird, auch in Streams mit hoher Geschwindigkeit, werden Regeln für bestimmte Autoren nie gedrosselt.

* Twitter-Feed-Unterbrechungen können aus verschiedenen Gründen auftreten. In einigen Fällen veröffentlicht Twitter keine Tweets, daher erhält Livefyre keine Benachrichtigung über die neuen Inhalte und kann nicht angezeigt werden. Serviceunterbrechungen der APIs von Twitter oder Datenverkehr mit Hashtags/Suchbegriffen mit hohem Volumen können auch zu fehlenden Tweets führen.
