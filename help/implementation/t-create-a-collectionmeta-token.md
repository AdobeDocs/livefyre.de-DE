---
description: Erstellen Sie eine neue Sammlung, indem Sie ein collectionMeta-Token erstellen, das an Livefyre übergeben wird.
title: Erstellen einer Sammlung mit dem CollectionMeta-Token
exl-id: d2dafc90-de21-4998-8e85-83f970524329
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Erstellen einer Sammlung mit dem CollectionMeta-Token{#create-a-collection-using-the-collectionmeta-token}

Erstellen Sie eine neue Sammlung, indem Sie ein collectionMeta-Token erstellen, das an Livefyre übergeben wird.

1. Erstellen Sie das Token collectionMeta.
1. Erstellen Sie die Prüfsumme.

   Die Prüfsumme ist erforderlich, wenn Sie Livefyre über Änderungen informieren möchten, die Sie an Ihrer Sammlung vorgenommen haben. Livefyre aktualisiert Ihre Sammlung nur, wenn die bereitgestellte Prüfsumme sich von der zuvor gesendeten Prüfsumme unterscheidet. Das Erstellen einer Prüfsumme ist genau wie das Erstellen eines `collectionMeta`-Tokens, aber anstatt `buildCollectionMetaToken` aufzurufen, rufen Sie `buildChecksum` auf.

Erstellen Sie Benutzertokens zur Authentifizierung bei Livefyre.
