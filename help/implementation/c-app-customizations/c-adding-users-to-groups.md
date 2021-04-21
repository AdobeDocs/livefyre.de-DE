---
description: hinzufügen einem Konto ein Benutzer-Tag, um einen Benutzer zu einer Gruppe hinzuzufügen.
title: Hinzufügen von Benutzern zu Gruppen
exl-id: 6e799c77-e815-40c2-ae06-bbd076df9fe7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# Hinzufügen von Benutzern zu Gruppen{#adding-users-to-groups}

hinzufügen einem Konto ein Benutzer-Tag, um einen Benutzer zu einer Gruppe hinzuzufügen.

Benutzer-Tags können sowohl für proprietäre als auch für Enterprise Profil-Systeme implementiert werden und Konten auf verschiedene Weise hinzugefügt werden:

* Beim Erstellen von Inhabern und Moderatoren über Studio wird dem Konto das &quot;Moderator&quot;-Benutzer-Tag zugewiesen.
* Beim Erstellen von Benutzergruppen und dem Hinzufügen von Benutzern zu diesen mithilfe von Studio werden automatisch Benutzer-Tags mit dem Namen der Gruppe auf die ausgewählten Benutzer angewendet.
* Benutzer-Tags können auch direkt auf Konten angewendet werden, indem der [Hinzufügen-Tag HTTP](https://api.livefyre.com/docs#add-user-tag)-Aufruf oder Ping for Pull verwendet wird.

>[!NOTE]
>
>Beide API-Methoden, der HTTP Hinzufügen User Tag-Aufruf und die Ping for Pull-Methode, überschreiben alle Tags, die dem Konto zuvor auf andere Weise zugewiesen wurden. Bitte wählen Sie daher eine Methode aus und verwenden Sie sie während des gesamten Prozesses konsistent.

## hinzufügen eines Benutzers über die Seite &quot;Benutzer&quot;in Studio {#section_qgq_nbw_xz} zu einer Gruppe

* Klicken Sie auf **[!UICONTROL Add Group]** oder die Gruppenbeschriftung unter einem beliebigen Benutzernamen, um das Gruppenmenü zu öffnen.
* Blättern Sie durch die Liste und suchen Sie die Gruppe, der Sie den Benutzer hinzufügen möchten. Sie können einen Gruppennamen in das Feld **[!UICONTROL Search]** oben in der Dropdownliste eingeben.
* Markieren Sie das Kontrollkästchen neben der Gruppe(n), der/denen der Benutzer hinzugefügt werden soll, und klicken Sie auf &quot;Zurück&quot;.

Das Profil des Benutzers zeigt entweder den Gruppennamen (wenn der Benutzer nur in einer Gruppe besteht) oder die Anzahl der Gruppen an, denen der Benutzer angehört.

## hinzufügen eines Benutzers zu einer Gruppe mithilfe des Hinzufügen-Tag-Aufrufs {#section_kn3_gbw_xz}

Übergeben Sie den LFToken-Benutzernamen und den markierten Tag-Namen an die POST.

Beispiel:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Weitere Informationen finden Sie unter API-Referenz > [Hinzufügen Benutzertag](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## hinzufügen eines Benutzers zu einer Gruppe mit Ping für Pull {#section_kyj_11w_xz}

Verwenden Sie das Tag-Array, um Benutzer Benutzergruppen zuzuweisen. (Tags können 1-63 alphanumerische Zeichen und Unterstriche enthalten.)

Beispiel:

```
"tags": ["moderator", "brand_advocate"],
```

## hinzufügen eines Benutzers mit Remote-Profilen {#section_uyn_scv_xz}

hinzufügen Benutzer-Tags mit dem Remote-Profil, die zur Synchronisierung von Benutzerdaten zwischen Ihrem benutzerdefinierten Profil- und Livefyre-System für bestimmte Benutzer verwendet werden.
