---
description: Automatisieren des Prozesses mithilfe der Feature APIs
seo-description: Automatisieren des Prozesses mithilfe der Feature APIs
seo-title: Feature APIs
title: Feature APIs
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Feature APIs{#feature-apis}

Automatisieren des Prozesses mithilfe der Feature APIs

Verwenden Sie die Feature-APIs, um den Prozess zu automatisieren, durch den Inhalte vorgestellt werden. Wenn Sie beispielsweise eine Live-Blog- oder Kommentar-App erstellen, stellen Sie alle Inhalte, die von einem ausgewählten Moderator gepostet werden, bereit, um die Konversation zu steuern und Konsistenz innerhalb des Streams herzustellen.

Livefyre bietet Funktionen- und Unfeature-APIs.

## Funktion {#section_jpw_nqw_xz}

**Ressource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

&#x200B; Geben Sie das Benutzertoken für den ausgewählten Moderator ein.

**Beitragsdaten**

```
{value: <number>} 
```

Der Wert wird verwendet, um speziellen Inhalt zu sortieren, der größte bis der kleinste (10 wird vor 1 in der Liste der speziellen Inhalte angezeigt). Dieser Wert wird standardmäßig **jetzt** in der Epochenzeit verwendet. Daher werden Kommentare mit Sonderzeichen in der Regel vom neuesten zum ältesten sortiert.

**Beispielantwort**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Das Datenfeld wird noch nicht verwendet.

## Rückgängig {#section_knh_mqw_xz}

**Ressource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Geben Sie das Benutzertoken für den ausgewählten Moderator ein.

**Beispielantwort**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Das Datenfeld wird noch nicht verwendet.

