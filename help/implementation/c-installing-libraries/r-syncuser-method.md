---
description: Informiert Livefyre, Benutzerinformationen aus einer zuvor festgelegten
  Synchronisierungsurl abzurufen. Gibt einen Booleschen Wert zurück.
seo-description: Informiert Livefyre, Benutzerinformationen aus einer zuvor festgelegten
  Synchronisierungsurl abzurufen. Gibt einen Booleschen Wert zurück.
seo-title: Syncuser-Netzwerkmethode
solution: Experience Manager
title: Syncuser-Netzwerkmethode
uuid: 2 affb 03 d -3907-4 b 01-9 a 64-02 ba 1 b 6 da 14
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Syncuser-Netzwerkmethode{#syncuser-network-method}

Informiert Livefyre, Benutzerinformationen aus einer zuvor festgelegten Synchronisierungsurl abzurufen. Gibt einen Booleschen Wert zurück.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| Userid | Zeichenfolge | Die Benutzer-ID, die mit Livefyre synchronisiert werden soll. Bevor Sie diese Methode aufrufen können, müssen Sie über eine Benutzersynchronisierung-URL mit Livefyre verfügen. |

## Java-Beispiel {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Beispielausgabe:

```
true
```

## Nodejs-Beispiel {#section_xkd_gds_rz}

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

## Python Example {#section_dwg_gds_rz}

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
