---
description: Nicht jeder Tweet, der mit einer Regel übereinstimmt, wird in einem Stream
  angezeigt.
seo-description: Nicht jeder Tweet, der mit einer Regel übereinstimmt, wird in einem
  Stream angezeigt.
seo-title: Einschränken und Frequenz von Tweets
solution: Experience Manager
title: Einschränken und Frequenz von Tweets
uuid: b 9 edfb 1 e-e 6 cf -4 a 48-8756-05 f 5 f 18 d 8799
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Einschränken und Frequenz von Tweets{#throttling-and-frequency-of-tweets}

Nicht jeder Tweet, der mit einer Regel übereinstimmt, wird in einem Stream angezeigt.

Einschränkungen von Twitter-Regeln und Twitter-Feeds können die Anzahl der Tweets beschränken, die im Stream sichtbar sind.

>[!NOTE]
>
>Um sicherzustellen, dass bestimmte Tweets in Ihren Stream aufgenommen werden, verwenden Sie die Option "Asset hochladen" auf der Seite" Alle Assets" .

* Twitter-Regeln drosseln Inhalte und ziehen 1 Tweets pro Regel alle 5 Sekunden. Dadurch können Inhalte, die in Livefyre-Apps angezeigt werden, ausgewogener sein und nicht mit Tweets überfordert werden. Wenn Sie eingehende Tweets auf diese Weise einschränken, wird auch verhindert, dass der Stream während hohem Traffic-Zeitraum überschwemmt oder unlesbar wird.

   >[!NOTE]
   >
   >Um sicherzustellen, dass Ihre Inhalte mit hohem Wert in Ihren Apps auch in Hochgeschwindigkeits-Streams angezeigt werden, werden Regeln für bestimmte Autoren nie gedrosselt.

* Twitter-Feed-Unterbrechungen können aus mehreren Gründen auftreten. In einigen Fällen führt Twitter Tweets nicht aus, weshalb Livefyre keine Benachrichtigungen über den neuen Inhalt erhält und es nicht angezeigt werden kann. Dienstunterbrechungen von Twitter-apis oder Traffic auf hohen Hashtags/Keywords mit hohem Volumen führen möglicherweise auch zu fehlenden Tweets.

