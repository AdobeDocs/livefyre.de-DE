---
description: Sie können Ihre Videodomäne mit einer Whitelist versehen.
seo-description: Sie können Ihre Videodomäne mit einer Whitelist versehen.
seo-title: Userprivacyvideowhitelist
solution: Experience Manager
title: Userprivacyvideowhitelist
uuid: adfead 18-b 73 b -4 ac 4-97 a 0-d 39 f 528 b 7606
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Userprivacyvideowhitelist{#userprivacyvideowhitelist}

Wenn Sie Ihre eigenen Videos und Player als Teil der Videos verwenden, die in einer Livefyre-Visualisierungsapp angezeigt werden, können Sie Ihre Videodomäne whitelist. Durch die Whitelisting Ihrer Videodomäne wird die Videomaske für Ihre benutzerdefinierten Videos und Player entfernt.

>[!NOTE]
>
>Verwenden Sie spezifische Pfade, um sicherzustellen, dass nur sichere Videos in der Positivliste aufgeführt werden. Wenn Sie einen weit reichenden Pfad bereitstellen (z. B. sampledomain.com), können Sie möglicherweise unsichere Videos verwenden.

* Hinzufügen `userPrivacyVideoWhitelist` nach `userPrivacyOptOut`. Sie können alle Livefyre-Datenschutzmarkierungen gleichzeitig als Teil eines Livefyre-Objekts hinzufügen.
* `userPrivacyVideoWhitelist` gilt nur für Inhalte, die nicht aus sozialen Medien eingebettet werden.

Im folgenden Beispiel werden Videos, die in Apps mit dem `sampledomain.com/cdn/videos` Pfad angezeigt werden, in die Positivliste aufgenommen:

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
