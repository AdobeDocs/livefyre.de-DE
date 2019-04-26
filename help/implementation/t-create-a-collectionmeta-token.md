---
description: Erstellen Sie eine neue Sammlung, indem Sie ein collectionmeta-Token
  erstellen, das an Livefyre übergeben wird.
seo-description: Erstellen Sie eine neue Sammlung, indem Sie ein collectionmeta-Token
  erstellen, das an Livefyre übergeben wird.
seo-title: Erstellen einer Sammlung mit dem collectionmeta-Token
solution: Experience Manager
title: Erstellen einer Sammlung mit dem collectionmeta-Token
uuid: 5 a 3 e 18 e 8-8568-45 bb -9070-d 0 fa 43 dd 819 b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Erstellen einer Sammlung mit dem collectionmeta-Token{#create-a-collection-using-the-collectionmeta-token}

Erstellen Sie eine neue Sammlung, indem Sie ein collectionmeta-Token erstellen, das an Livefyre übergeben wird.

1. Erstellen Sie das collectionmeta-Token.
1. Erstellen Sie die Prüfsumme.

   Die Prüfsumme ist erforderlich, wenn Sie Livefyre von Änderungen an Ihrer Sammlung benachrichtigen möchten. Livefyre aktualisiert Ihre Sammlung nur, wenn die angegebene Prüfsumme sich von der zuvor gesendeten Prüfsumme unterscheidet. Das Erstellen einer Prüfsumme ähnelt dem Erstellen eines `collectionMeta` Tokens, nicht jedoch dem Aufruf `buildCollectionMetaToken` von Call `buildChecksum`.

Erstellen Sie Benutzer-Token zur Authentifizierung in Livefyre.