---
description: Sie können die Videodomäne zulassen und auflisten.
title: userPrivacyVideoWhitelist
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Wenn Sie Ihre eigenen Videos und Player als Teil der Videos verwenden, die in einer Livefyre-Visualisierungs-App angezeigt werden, können Sie die Videodomäne zulassen und auflisten. Durch Zulassen der Auflistung Ihrer Videodomäne wird die Videomaske für Ihre benutzerspezifischen Videos und Player entfernt.

>[!NOTE]
>
>Verwenden Sie bestimmte Pfade, um sicherzustellen, dass nur die sicheren Videos in der Liste aufgeführt werden können. Wenn Sie einen breiten Pfad angeben (z. B. sampledomain.com), können Sie unsichere Videos zulassen.

* hinzufügen `userPrivacyVideoWhitelist` nach `userPrivacyOptOut`. Sie können alle Livefyre-Datenschutzkennzeichnungen gleichzeitig als Teil eines Livefyre-Objekts hinzufügen.
* `userPrivacyVideoWhitelist` gilt nur für Inhalte, die nicht in sozialen Medien eingebettet sind.

Im folgenden Beispiel sind Videos, die in Apps mit dem Pfad `sampledomain.com/cdn/videos` angezeigt werden, zulässig:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
