---
description: Nicht jeder Tweet, der mit einer Regel übereinstimmt, wird in einem Stream angezeigt.
seo-description: Nicht jeder Tweet, der mit einer Regel übereinstimmt, wird in einem Stream angezeigt.
seo-title: Einschränkungen und Häufigkeit von Tweets
solution: Experience Manager
title: Einschränkungen und Häufigkeit von Tweets
uuid: b9edfb1e-e6cf-4a48-8756-05f5f18d8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Einschränkungen und Häufigkeit von Tweets{#throttling-and-frequency-of-tweets}

Nicht jeder Tweet, der mit einer Regel übereinstimmt, wird in einem Stream angezeigt.

Durch Einschränkungen bei Twitter-Regeln und Unterbrechungen bei Twitter-Feeds kann die Anzahl der im Stream sichtbaren Tweets eingeschränkt werden.

>[!NOTE]
>
>Um sicherzustellen, dass bestimmte Tweets in Ihrem Stream enthalten sind, verwenden Sie die Option "Asset hochladen"auf der Seite "Alle Assets".

* Twitter-Regeln drosseln Inhalte, wobei alle 5 Sekunden ein Tweet pro Regel abgerufen wird. Dadurch können Inhalte in Livefyre-Apps ausgeglichener dargestellt werden und nicht mit Tweets überlastet werden. Die Beschränkung eingehender Tweets auf diese Weise trägt auch dazu bei, zu verhindern, dass der Stream während hoher Traffic-Zeiten überschwemmt oder unleserlich wird.

   >[!NOTE]
   >
   >Um sicherzustellen, dass der Inhalt Ihrer hochwertigen Autoren in Ihren Apps angezeigt wird, auch in Streams mit hoher Geschwindigkeit, werden Regeln für bestimmte Autoren nie gedrosselt.

* Twitter-Feed-Unterbrechungen können aus verschiedenen Gründen auftreten. In einigen Fällen sendet Twitter keine Tweets, daher erhält Livefyre keine Benachrichtigung über den neuen Inhalt und kann nicht angezeigt werden. Serviceunterbrechungen von Twitter-APIs oder Datenverkehr mit Hashtags/Suchbegriffen mit hohem Volumen können ebenfalls zu fehlenden Tweets führen.

