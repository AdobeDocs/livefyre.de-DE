---
description: Automatisieren des Prozesses mit den Funktionen-apis
seo-description: Automatisieren des Prozesses mit den Funktionen-apis
seo-title: Funktions-apis
title: Funktions-apis
uuid: eac 3 a 156-0 b 60-4 ffa -8 b 6 f-e 451 eb 03 da 77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Funktions-apis{#feature-apis}

Automatisieren des Prozesses mit den Funktionen-apis

Verwenden Sie die Funktion apis, um den Prozess zu automatisieren, mit dem Inhalte dargestellt werden. Wenn Sie beispielsweise eine Live-Blog- oder Kommentar-App erstellen, können Sie alle Inhalte, die von einem ausgewählten Moderator veröffentlicht werden, zur Steuerung der Unterhaltung und zur Konsistenz innerhalb des Streams verwenden.

Livefyre bietet sowohl Funktionen für Funktion als auch Unfunktionen.

## Funktion {#section_jpw_nqw_xz}

**Ressource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

Geben Sie das Benutzertoken für Ihren ausgewählten Moderator ein.

**Beitragsdaten**

```
{value: <number>} 
```

Der Wert wird verwendet, um spezielle Inhalte zu sortieren, die größte bis am kleinsten (10 wird vor 1 in der Liste der speziellen Inhalte angezeigt). Dieser Wert wird standardmäßig **jetzt** in der Epoche der Epoche verwendet. Daher werden hervorgehobene Kommentare in der Regel ganz oben in den ältesten sortiert.

**Beispielantwort**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Das Datenfeld wird noch nicht verwendet.

## Unfeature {#section_knh_mqw_xz}

**Ressource**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Geben Sie das Benutzertoken für Ihren ausgewählten Moderator ein.

**Beispielantwort**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Das Datenfeld wird noch nicht verwendet.

