---
description: Informiert Livefyre, Benutzerinformationen von einer zuvor festgelegten URL für die Benutzersynchronisierung abzurufen. Gibt einen booleschen Wert zurück.
seo-description: Informiert Livefyre, Benutzerinformationen von einer zuvor festgelegten URL für die Benutzersynchronisierung abzurufen. Gibt einen booleschen Wert zurück.
seo-title: syncUser-Netzwerkmethode
solution: Experience Manager
title: syncUser-Netzwerkmethode
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# syncUser Network Method{#syncuser-network-method}

Informiert Livefyre, Benutzerinformationen von einer zuvor festgelegten URL für die Benutzersynchronisierung abzurufen. Gibt einen booleschen Wert zurück.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| userId | Zeichenfolge | Die Benutzer-ID, die mit Livefyre synchronisiert werden soll. Sie müssen eine URL für die Benutzersynchronisierung mit Livefyre festlegen, bevor Sie diese Methode aufrufen können. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Beispielausgabe:

```
true
```

## NodeJS-Beispiel {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Beispielausgabe:

```
true
```

## PHP-Beispiel {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Beispielausgabe:

```
true
```

## Python-Beispiel {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Beispielausgabe:

```
True
```

## Ruby-Beispiel {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Beispielausgabe:

```
True
```
