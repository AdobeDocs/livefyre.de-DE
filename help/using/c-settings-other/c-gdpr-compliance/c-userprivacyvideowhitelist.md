---
description: Sie können die Liste Ihrer Videodomäne zulassen.
seo-description: Sie können die Liste Ihrer Videodomäne zulassen.
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Wenn Sie Ihre eigenen Videos und Player als Teil der Videos verwenden, die in einer Livefyre-Visualisierungs-App angezeigt werden, können Sie die Liste Ihrer Videodomäne zulassen. Durch Zulassen der Auflistung Ihrer Videodomäne wird die Videomaske für Ihre benutzerspezifischen Videos und Player entfernt.

>[!NOTE]
>
>Verwenden Sie bestimmte Pfade, um sicherzustellen, dass nur die sicheren Videos aufgelistet werden können. Wenn Sie einen breiten Pfad angeben (z. B. sampledomain.com), können Sie unsichere Listen zulassen.

* Hinzufügen `userPrivacyVideoWhitelist` nach `userPrivacyOptOut`. Sie können alle Livefyre-Datenschutzkennzeichnungen gleichzeitig als Teil eines Livefyre-Objekts hinzufügen.
* `userPrivacyVideoWhitelist` gilt nur für Inhalte, die nicht in sozialen Medien eingebettet sind.

Im folgenden Beispiel sind Videos, die in Apps mit dem `sampledomain.com/cdn/videos` Pfad angezeigt werden, zulässig:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
