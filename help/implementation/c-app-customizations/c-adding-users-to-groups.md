---
description: Fügen Sie einem Konto ein Benutzer-Tag hinzu, um einer Gruppe einen Benutzer hinzuzufügen.
seo-description: Fügen Sie einem Konto ein Benutzer-Tag hinzu, um einer Gruppe einen Benutzer hinzuzufügen.
seo-title: Hinzufügen von Benutzern zu Gruppen
solution: Experience Manager
title: Hinzufügen von Benutzern zu Gruppen
uuid: 3633f2df-8d60-4cdd-b9a2-3807218c74a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Adding Users to Groups{#adding-users-to-groups}

Fügen Sie einem Konto ein Benutzer-Tag hinzu, um einer Gruppe einen Benutzer hinzuzufügen.

Benutzer-Tags können sowohl für proprietäre als auch für Unternehmensprofil-Systeme implementiert werden und auf verschiedene Weise zu Konten hinzugefügt werden:

* Beim Erstellen von Inhabern und Moderatoren über Studio wird dem Konto das "Moderator"-Benutzer-Tag zugewiesen.
* Beim Erstellen von Benutzergruppen und dem Hinzufügen von Benutzern zu diesen über Studio werden automatisch Benutzer-Tags mit dem Namen der Gruppe auf die ausgewählten Benutzer angewendet.
* Benutzer-Tags können auch direkt auf Konten angewendet werden, indem Sie den HTTP[ -Aufruf " ](https://api.livefyre.com/docs#add-user-tag)Tag hinzufügen"oder "Ping für Pull"verwenden.

>[!NOTE]
>
>Beide API-Methoden, der HTTP-Aufruf zum Hinzufügen eines Benutzertags und die Ping-Methode zum Ziehen, überschreiben alle Tags, die dem Konto zuvor auf andere Weise zugewiesen wurden. Wählen Sie daher eine Methode aus und verwenden Sie sie durchgängig in Ihrem gesamten Prozess.

## Hinzufügen eines Benutzers zu einer Gruppe über die Seite "Benutzer"in Studio {#section_qgq_nbw_xz}

* Klicken Sie auf **[!UICONTROL Add Group]** oder die Gruppenbeschriftung unter einem beliebigen Benutzernamen, um das Gruppenmenü zu öffnen.
* Blättern Sie durch die Liste und suchen Sie die Gruppe, der Sie den Benutzer hinzufügen möchten. Sie können einen Gruppennamen in das **[!UICONTROL Search]** Feld oben im Dropdownmenü eingeben.
* Markieren Sie das Kontrollkästchen neben der Gruppe(n), der/denen der Benutzer hinzugefügt werden soll, und klicken Sie auf "Zurück".

Das Benutzerprofil zeigt entweder den Namen der Gruppe (wenn sich der Benutzer nur in einer Gruppe befindet) oder die Anzahl der Gruppen, zu denen der Benutzer gehört.

## Hinzufügen eines Benutzers zu einer Gruppe mithilfe des Aufrufs "Tag hinzufügen" {#section_kn3_gbw_xz}

Übergeben Sie den LFToken-Code des Benutzers und Ihren ausgewählten Tag-Namen mit der POST-Anforderung

Beispiel:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Weitere Informationen finden Sie unter API-Referenz &gt; [Benutzertag](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post)hinzufügen.

## Hinzufügen eines Benutzers zu einer Gruppe mit Ping für Pull {#section_kyj_11w_xz}

Verwenden Sie das Tag-Array, um Benutzer Benutzergruppen zuzuweisen. (Tags können 1-63 alphanumerische Zeichen und Unterstriche enthalten.)

Beispiel:

```
"tags": ["moderator", "brand_advocate"],
```

## Hinzufügen eines Benutzers zu einer Gruppe mithilfe von Remote-Profilen {#section_uyn_scv_xz}

Fügen Sie dem Remote-Profil Benutzer-Tags hinzu, mit denen die Benutzerdaten für bestimmte Benutzer zwischen Ihrem benutzerdefinierten Profilsystem und Livefyre synchronisiert werden.
