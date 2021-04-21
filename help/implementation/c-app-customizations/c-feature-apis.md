---
description: Automatisieren des Prozesses mithilfe der Feature APIs
title: Feature APIs
exl-id: 765e47fe-a406-44e6-b4fb-b2e85fc83c01
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# Feature APIs{#feature-apis}

Automatisieren des Prozesses mithilfe der Feature APIs

Verwenden Sie die Feature-APIs, um den Prozess zu automatisieren, durch den Inhalte vorgestellt werden. Wenn Sie beispielsweise eine Live-Blog- oder Kommentar-App erstellen, stellen Sie alle Inhalte, die von einem ausgewählten Moderator gepostet werden, bereit, um die Konversation zu steuern und Konsistenz innerhalb des Streams herzustellen.

Livefyre-Angebot sowohl Feature- als auch Unfeature-APIs.

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

Der Wert wird verwendet, um spezielle Inhalte zu sortieren, die am größten oder am kleinsten sind (10 werden in der Liste mit speziellen Inhalten vor 1 angezeigt). Dieser Wert wird standardmäßig in Epochenzeit auf **now** gesetzt, daher werden Kommentare mit Hinweisen in der Regel vom neuesten zum ältesten sortiert.

**Beispielantwort**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Das Datenfeld wird noch nicht verwendet.

## Funktion {#section_knh_mqw_xz} aufheben

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
