---
description: Erstellen Sie eine neue Sammlung, indem Sie ein collectionMeta-Token erstellen, das an Livefyre übergeben wird.
seo-description: Erstellen Sie eine neue Sammlung, indem Sie ein collectionMeta-Token erstellen, das an Livefyre übergeben wird.
seo-title: Erstellen einer Sammlung mit dem CollectionMeta-Token
solution: Experience Manager
title: Erstellen einer Sammlung mit dem CollectionMeta-Token
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# Erstellen einer Sammlung mit dem CollectionMeta-Token{#create-a-collection-using-the-collectionmeta-token}

Erstellen Sie eine neue Sammlung, indem Sie ein collectionMeta-Token erstellen, das an Livefyre übergeben wird.

1. Erstellen Sie das Token collectionMeta.
1. Erstellen Sie die Prüfsumme.

   Die Prüfsumme ist erforderlich, wenn Sie Livefyre über Änderungen informieren möchten, die Sie an Ihrer Sammlung vorgenommen haben. Livefyre aktualisiert Ihre Sammlung nur, wenn die bereitgestellte Prüfsumme sich von der zuvor gesendeten Prüfsumme unterscheidet. Das Erstellen einer Prüfsumme ist genauso wie das Erstellen eines `collectionMeta` Tokens, anstatt `buildCollectionMetaToken` einen Aufruf auszuführen `buildChecksum`.

Erstellen Sie Benutzertokens zur Authentifizierung bei Livefyre.