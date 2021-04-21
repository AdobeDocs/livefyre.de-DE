---
description: Informiert Livefyre, die URL für die Benutzersynchronisierung auf die angegebene URL zu aktualisieren. Gibt einen booleschen Wert zurück.
title: setUserSyncUrl-Netzwerkmethode
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# setUserSyncUrl-Netzwerkmethode{#setusersyncurl-network-method}

Informiert Livefyre, die URL für die Benutzersynchronisierung auf die angegebene URL zu aktualisieren. Gibt einen booleschen Wert zurück.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| urlTemplate | Zeichenfolge | Die URL, die bei Livefyre für die Synchronisierung von Benutzer-IDs registriert werden soll. Erfordert &quot;`{id}`&quot;als Teil der angegebenen URL-Zeichenfolge. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Beispielausgabe:

```
true
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Beispielausgabe:

```
true
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Beispielausgabe:

```
true
```

## Python-Beispiel {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Beispielausgabe:

```
True
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Beispielausgabe:

```
True
```
