---
description: Sie können Ihre Videodomäne mit der Whitelist .
seo-description: Sie können Ihre Videodomäne mit der Whitelist .
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

Wenn Sie Ihre eigenen Videos und Player als Teil der Videos verwenden, die in einer Livefyre-Visualisierungs-App angezeigt werden, können Sie Ihre Videodomäne auf eine Whitelist setzen. Wenn Sie Ihre Videodomäne freigeben, wird die Videomaske für Ihre benutzerdefinierten Videos und Player entfernt.

>[!NOTE]
>
>Verwenden Sie bestimmte Pfade, um sicherzustellen, dass nur die sicheren Videos in die Positivliste aufgenommen werden. Wenn Sie einen breiten Pfad angeben (z. B. sampledomain.com), können Sie unsichere Videos auf die Whitelist setzen.

* Fügen Sie `userPrivacyVideoWhitelist` nach `userPrivacyOptOut`. Sie können alle Livefyre-Datenschutzkennzeichnungen gleichzeitig als Teil eines Livefyre-Objekts hinzufügen.
* `userPrivacyVideoWhitelist` gilt nur für Inhalte, die nicht in sozialen Medien eingebettet sind.

Im folgenden Beispiel werden Videos, die in Apps mit dem `sampledomain.com/cdn/videos` Pfad angezeigt werden, in die Positivliste aufgenommen:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
