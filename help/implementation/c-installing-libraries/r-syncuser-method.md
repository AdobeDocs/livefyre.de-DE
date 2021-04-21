---
description: Informiert Livefyre, Benutzerinformationen von einer zuvor festgelegten URL für die Benutzersynchronisierung abzurufen. Gibt einen booleschen Wert zurück.
title: syncUser-Netzwerkmethode
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

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
