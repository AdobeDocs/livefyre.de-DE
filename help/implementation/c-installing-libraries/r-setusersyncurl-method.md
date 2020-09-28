---
description: Informiert Livefyre, die URL für die Benutzersynchronisierung auf die angegebene URL zu aktualisieren. Gibt einen booleschen Wert zurück.
seo-description: Informiert Livefyre, die URL für die Benutzersynchronisierung auf die angegebene URL zu aktualisieren. Gibt einen booleschen Wert zurück.
seo-title: setUserSyncUrl-Netzwerkmethode
solution: Experience Manager
title: setUserSyncUrl-Netzwerkmethode
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setUserSyncUrl-Netzwerkmethode{#setusersyncurl-network-method}

Informiert Livefyre, die URL für die Benutzersynchronisierung auf die angegebene URL zu aktualisieren. Gibt einen booleschen Wert zurück.

| Variable | Typ | Beschreibung |
|--- |--- |--- |
| urlTemplate | Zeichenfolge | Die URL, die bei Livefyre zum Synchronisieren von Benutzer-IDs registriert werden soll. Erfordert, dass "`{id}`"Teil der angegebenen URL-Zeichenfolge ist. |

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
