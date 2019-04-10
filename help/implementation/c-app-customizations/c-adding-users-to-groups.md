---
description: Fügen Sie einem Konto ein Benutzertag hinzu, um einer Gruppe einen Benutzer
  hinzuzufügen.
seo-description: Fügen Sie einem Konto ein Benutzertag hinzu, um einer Gruppe einen
  Benutzer hinzuzufügen.
seo-title: Hinzufügen von Benutzern zu Gruppen
solution: Experience Manager
title: Hinzufügen von Benutzern zu Gruppen
uuid: 3633 f 2 df -8 d 60-4 cdd-b 9 a 2-3807218 c 74 a 0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Hinzufügen von Benutzern zu Gruppen{#adding-users-to-groups}

Fügen Sie einem Konto ein Benutzertag hinzu, um einer Gruppe einen Benutzer hinzuzufügen.

Benutzertags können sowohl für proprietäre als auch für Unternehmensprofilsysteme implementiert werden und können auf verschiedene Weise Konten hinzugefügt werden:

* Durch Erstellen von Inhabern und Moderatoren über Studio wird dem Konto das Benutzertag "Moderator" zugewiesen.
* Wenn Sie Benutzergruppen erstellen und Benutzer über Studio hinzufügen, werden automatisch Benutzer Tags mit dem Namen der Gruppe für die ausgewählten Benutzer angewendet.
* Benutzertags können auch mithilfe des [HTTP](https://api.livefyre.com/docs#add-user-tag) -Aufrufs "Benutzer-Tag hinzufügen" oder Ping für Pull direkt auf Konten angewendet werden.

>[!NOTE]
>
>Beide API-Methoden, der HTTP-Aufruf des Benutzertags-Aufrufs und die Ping-Methode für Pull, überschreiben alle zuvor dem Konto zugewiesenen Tags auf andere Weise. Wählen Sie daher eine Methode aus und verwenden Sie diese konsistent im gesamten Prozess.

## Hinzufügen eines Benutzers zu einer Gruppe über die Seite "Benutzer" in Studio {#section_qgq_nbw_xz}

* Klicken Sie **[!UICONTROL Add Group]** auf oder die Gruppenbeschriftung unter einem beliebigen Benutzernamen, um das Menü der Gruppe zu öffnen.
* Blättern Sie durch die Liste und suchen Sie die Gruppe, für die Sie den Benutzer hinzufügen möchten. Sie können in das **[!UICONTROL Search]** Feld oben in der Dropdown-Liste einen Gruppennamen eingeben.
* Klicken Sie auf das Kontrollkästchen neben der bzw. den Gruppe (n), dem der Benutzer hinzugefügt werden soll, und klicken Sie auf "Zurückgeben" .

Das Profil des Benutzers zeigt entweder den Namen der Gruppe (wenn sich der Benutzer nur in einer Gruppe befindet) oder die Anzahl der Gruppen an, denen der Benutzer angehört.

## Benutzer über den Aufruf "Benutzer-Tag hinzufügen" einer Gruppe hinzufügen {#section_kn3_gbw_xz}

Übergeben Sie das lftoken des Benutzers und Ihren ausgewählten Tag-Namen mit der POST-Anforderung.

Beispiel:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Weitere Informationen finden Sie unter API-Referenz > [Benutzertag hinzufügen](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Hinzufügen eines Benutzers zu einer Gruppe mit Ping für Pull {#section_kyj_11w_xz}

Verwenden Sie das Tag-Array, um Benutzern Benutzergruppen zuzuweisen. (Tags können 1-63 alphanumerische Zeichen und Unterstriche enthalten.)

Beispiel:

```
"tags": ["moderator", "brand_advocate"],
```

## Hinzufügen eines Benutzers zu einer Gruppe mithilfe von Remote Profile {#section_uyn_scv_xz}

Fügen Sie dem Remote Profil Benutzertags hinzu, mit denen Benutzerdaten zwischen Ihrem benutzerdefinierten Profilsystem und Livefyre für die jeweiligen Benutzer synchronisiert werden.
